> [!warning] Upozornění
> Tyto výsledky jsem tvořil sám a nebo pomocí **ChatGPT** nějaké jsou vyzkoušené na **Postgress databázi** co se přístupná na školní server. 
## První zadání
Mějme tabulky (primární klíč označen <u>podrtženě</u>, cizí klíč *kurzívou*)
 ZÁKÁZNÍK (<u>id-z</u>, jméno, kredit),
 SPOJ (<u>kod</u>, dopravce, start, cíl),
 JÍZDENKA(<u>id-j</u>, *kod*, *id-z*, datum, odkud, kam,cena),

 všechny atributy jsou **NOT NULL**, význam a typy některých atributů:
 kredit - kredit, za který si zákazník může kupovat jízdenky *(int);*
 start, cíl - odkud kam jezdí daný spoj *(varchar);*
 odkud, kam - odkud kam jel daný zákazník na danou jízdenku *(varchar);*

Zapište v SQL dotazy
1. Vypište všechny zákazníky s nenulovým kreditem
```sql
SELECT * FROM ZÁKAZNÍK
WHERE kredit > 0; 
```
2. Vypište zákazníky, kteří jeli spojem v celé jeho trase
```sql
SELECT * FROM ZÁKAZNÍK
INNER JOIN JÍZDENKA ON JÍZDENKA.id-z = ZÁKANZÍK.id-z
INNER JOIN SPOJ ON JÍZDENKA.kod = SPOJ.kod
WHERE JÍZDENKA.odkud = SPOJ.start AND JÍZDENKA.kam = SPOJ.cíl;
```
3. Vypište počet cestujících, kteří jeli včera s Regiojetem z Brna do Prahy *(Počítame, že dneska je 06.07.2023)*
Řešení 1:
```sql
SELECT COUNT(*) FROM JÍZDENKA
INNER JOIN SPOJ ON JÍZDENKA.kod = SPOJ.kod
WHERE JÍZDENKA.datum="2023-07-05" AND SPOJ.dopravce="Regiojet" AND SPOJ.odkud="Brno" AND SPOJ.kam="Praha";
```
Řešení 2:
```sql
SELECT COUNT(*) AS počet_cestujících 
FROM JÍZDENKA
INNER JOIN SPOJ ON JÍZDENKA.kod = SPOJ.kod
WHERE JÍZDENKA.datum="2023-07-05" AND SPOJ.dopravce="Regiojet" AND SPOJ.odkud="Brno" AND SPOJ.kam="Praha";
```
4. Vypište jména zákazníku, kteří nikdy nejeli do Ostravy.
```sql
SELECT ZÁKAZNÍK.jména FROM ZÁKAZNÍK
LEFT JOIN JÍZDENKA ON JÍZDENKA.id-z = ZÁKAZNÍK.id-z
WHERE NOT JÍZDENKA.kam="Ostrava";
```
5. Vypište kódy spojů do Telče s počty cestujících, v nichž jelo včera víc než 40 lidí. *(Počítame, že dneska je 06.07.2023)*
```sql
SELECT SPOJ.kod, COUNT(JÍZDENKA.id-j) FROM SPOJ
INNER JOIN JÍZDENKA on JÍZDENKA.kod = SPOJ.kod
WHERE JÍZDENKA.datum="2023-07-05" AND JÍZDENKA.kam="Telč"
GROUP BY SPOJ.kod
HAVING COUNT(JÍZDENKA.id-j)>40;
```
6. Přidejte k tabulce `Spoj` nový datumový sloupce `Jezdí-od`, který bude NOT NULL. *Nezapomeňte reflektovat možný konflikt v případě, že* tabulka již obsahuje nějaké data
```sql
ALTER TABLE SPOJ ADD COLUMN `Jezdí-od` DATE NOT NULL DEFAULT CURRENT_DATE;
```
7. Odstraňte ze sloupce `dopravce` v tabulce `Spoj` integritní omezení NOT NULL
```sql
DELETE from SPOJ WHERE dopravce IS NOT NULL;
```

```sql
ALTER TABLE SPOJ ALTER COLUMN dopravce DROP NOT NULL;
```
## Druhé zadání
Mějme tabulky (primární klíč označen <u>podrtženě</u>, cizí klíč *kurzívou*)
 KLIENT (<u>id-klient</u>, jméno-klient, kredit),
 KURS (<u>název-kurs</u>, popis, trvání),
 LEKTOR(<u>id-lektor</u>, jméno-lektor, kvalifikace),
 TRÉNINK(<u>id-trénink</u>, *id-lektor*, *název-kurs*, datum,čas),
 ÚČAST(<u><i>id-trénink</i></u> ,<u><i>id-klient</i></u>, cena).

Zapište v SQL dotazy
8. Vypište všechny klienty, jejichž jméno končí na "ová".
```sql
SELECT * FROM KLIENT
WHERE jméno-klient LIKE "%ová";
```
9. Vypište tréninky *(pouze atributy tréninků)*, které odcvičili včera lektoři s kvalifikací "Fyzioterapeut". *(Počítame, že dneska je 06.07.2023)*
```sql
SELECT TRÉNINK.název-kurs, TRÉNINK.čas FROM TRÉNINK
INNER JOIN LEKTOR ON LEKTOR.id-lektor = TRÉNINK.id-lektor
WHERE TRÉNINK.datum = "2023-07-05" AND LEKTOR.kvalifikace="Fyzioterapeut";
```
10. Vypište celkovou cenu tréninků jógy tento týden.
```sql
SELECT SUM(ÚČAST.cena) AS celková_cena FROM ÚČAST
INNER JOIN TRÉNINK ON TRÉNINK.id-trénink = ÚČAST.id-trénink
INNER JOIN KURS ON KURS.název-kurs = TRÉNINK.název-kurs
WHERE KURS.název-kurs = 'jóga' AND TRÉNINK.datum >= DATE_SUB(CURDATE(), INTERVAL WEEKDAY(CURDATE()) DAY);
```
11. Vypište názvy kursů a pro každý z nich celkový počet v minulosti odcvičených tréninků a jejich celkovou cenu, seřaďte sestupně podle počtu tréninků.
```sql
SELECT TRÉNINK.název-kurs, COUNT(*) AS počet_tréninků, SUM(ÚČAST.cena) AS celková_cena
FROM TRÉNINK
INNER JOIN ÚČAST ON ÚČAST.id-trénink = TRÉNINK.id-trénink
GROUP BY TRÉNINK.název-kurs
ORDER BY COUNT(*) DESC;
```
12. Vypište `id` a `jména lektorů` spolu s počtem odcvičených klientů *(různých: každý klient se zde počítá jen jednou),* kteří mají tento počet vyšší než 50.
```sql
SELECT LEKTOR.id-lektor, LEKTOR.jméno-lektor, COUNT(DISTINCT ÚČAST.id-klient) AS počet_klientů
FROM LEKTOR
INNER JOIN TRÉNINK ON TRÉNINK.id-lektor = LEKTOR.id-lektor
INNER JOIN ÚČAST ON ÚČAST.id-trénink = TRÉNINK.id-trénink
GROUP BY LEKTOR.id-lektor, LEKTOR.jméno-lektor
HAVING COUNT(DISTINCT ÚČAST.id-klient) > 50;
```
13. Vypište jména klientů, kteří se zůčastnili všech tréninků krav-magy, které se kdy konaly.
```sql
SELECT KLIENT.jméno-klient
FROM KLIENT
INNER JOIN ÚČAST ON ÚČAST.id-klient = KLIENT.id-klient
INNER JOIN TRÉNINK ON TRÉNINK.id-trénink = ÚČAST.id-trénink
WHERE TRÉNINK.název-kurs = 'krav maga'
GROUP BY KLIENT.id-klient, KLIENT.jméno-klient
HAVING COUNT(DISTINCT TRÉNINK.id-trénink) = (SELECT COUNT(*) FROM TRÉNINK WHERE název-kurs = 'krav maga');
```
14. Vypište všechny kursy, trvající méně než dvě hodiny
```sql
SELECT * FROM KURS
WHERE čas < "120";
```
15. Vypište jména a kredit klientů, kteří v minulém týdnu cvičil s lektorkou Janou
```sql
SELECT KLIENT.jméno-klient, KLIENT.kredit
FROM KLIENT
INNER JOIN ÚČAST ON ÚČAST.id-klient = KLIENT.id-klient
INNER JOIN TRÉNINK ON TRÉNINK.id-trénink = ÚČAST.id-trénink
INNER JOIN LEKTOR ON LEKTOR.id-lektor = TRÉNINK.id-lektor
WHERE LEKTOR.jméno-lektor = 'Jana' AND TRÉNINK.datum >= DATE_SUB(CURDATE(), INTERVAL 1 WEEK);
```
16. Přidejte k tabulce Klient nový textový sloupec Bydliště, který bude NOT NULL. Nezapomeňte reflektovat možný konflikt v případě, že tabulka již obsahuje nějaká data.
```sql
ALTER TABLE KLIENT ADD COLUMN Bydliště VARCHAR(255) NOT NULL;
```
17. Vypište id a jména klientů a pro každého z nich celkový počet absolvovaných tréniků a jejich celkovou cenu, seřaďte sestupně podle počtu tréninků. Správně ošetřete případy klientů, kteří zatím neabsolvovali žádný trénink.
```sql
SELECT KLIENT.id-klient, KLIENT.jméno-klient, COALESCE(COUNT(ÚČAST.id-trénink), 0) AS počet_tréninků, COALESCE(SUM(ÚČAST.cena), 0) AS celková_cena
FROM KLIENT
LEFT JOIN ÚČAST ON ÚČAST.id-klient = KLIENT.id-klient
GROUP BY KLIENT.id-klient, KLIENT.jméno-klient
ORDER BY počet_tréninků DESC;
```
18. Vypište jména lektorů spolu s počtem odcvičených klientů (různých: každý klient se zde počítá jen jednou) v kursu "krav maga", kteří mají tento počet vyšší než 100.
```sql
SELECT LEKTOR.jméno-lektor, COUNT(DISTINCT ÚČAST.id-klient) AS počet_klientů
FROM LEKTOR
INNER JOIN TRÉNINK ON TRÉNINK.id-lektor = LEKTOR.id-lektor
INNER JOIN ÚČAST ON ÚČAST.id-trénink = TRÉNINK.id-trénink
INNER JOIN KURS ON KURS.název-kurs = TRÉNINK.název-kurs
WHERE KURS.název-kurs = 'krav maga'
GROUP BY LEKTOR.id-lektor, LEKTOR.jméno-lektor
HAVING COUNT(DISTINCT ÚČAST.id-klient) > 100;
```
19. Zvyšte ceny tréninků s id=11 o 20%.
```sql
UPDATE TRÉNINK
SET cena = cena * 1.2
WHERE id-trénink = 11;
```

## Třetí zadání

Mějme následující tabulky pro evidenci studentů, předmětů a jejich přihlášek (primární klíče označeny <u>podtržením</u>, cizí klíče _kurzívou_):

STUDENT (<u>id_student</u>, jméno, příjmení, rok_narození) 
PŘEDMĚT (<u>id_předmět</u>, název, kredity) 
PŘIHLÁŠKA (<u><i>id_student</i></u>, <u><i>id_předmět</i></u>, datum_přihlášení)

Vytvořte SQL dotazy pro následující úkoly:

20. Vypište všechny studenty z tabulky "STUDENT".
```sql
```
21. Vypište názvy všech předmětů.
```sql
```
22. Vypište jména a příjmení studentů, kteří jsou přihlášeni k předmětu s názvem "Matematika".
```sql
```
23. Vypište počet přihlášek na každý předmět.
```sql
```
24. Vypište studenty, kteří jsou přihlášeni alespoň ke třem předmětům.
```sql
```
25. Vypište předměty, které mají více než 5 kreditů.
```sql
```
26. Vypište studenty, kteří se přihlásili k předmětu alespoň před rokem 2020.
```sql
```

## Čtvrté zadání

Mějme následující tabulky pro evidenci zaměstnanců, oddělení, projektů a jejich propojení (primární klíče označeny <u>podtržením</u>, cizí klíče _kurzívou_):

ZAMĚSTNANCI (<u>id_zaměstnanec</u>, jméno, příjmení, pozice) 
ODDĚLENÍ (<u>id_oddělení</u>, název, vedoucí_oddělení) 
PROJEKTY (<u>id_projekt</u>, název, popis) 
PROPIS (<u><i>id_zaměstnanec</i></u>, <u><i>id_oddělení</i></u>, <u><i>id_projekt</i></u>, datum_nástupu)

Vytvořte SQL dotazy pro následující úkoly:

27. Vypište všechny zaměstnance z tabulky "ZAMĚSTNANCI".
```sql
```
28. Vypište názvy všech oddělení.
```sql
```
29. Vypište názvy všech projektů.
```sql
```
30. Vypište zaměstnance, kteří jsou vedoucími oddělení.
```sql
```
31. Vypište zaměstnance, kteří pracují na projektu s názvem "Nový produkt".
```sql
```
32. Vypište počet zaměstnanců v každém oddělení.
```sql
```
33. Vypište názvy projektů, na kterých pracuje alespoň 3 zaměstnanci.
```sql
```

## Páté zadání
Mějme následující tabulky pro evidenci filmů, herců, žánrů, režisérů, ocenění a jejich propojení (primární klíče označeny <u>podtržením</u>, cizí klíče _kurzívou_):

FILMY (<u>id_film</u>, název, rok, <i>id_režisér</i>, <i>id_žánr</i>) 
HEREC (<u>id_herec</u>, jméno, příjmení) 
ŽÁNR (<u>id_žánr</u>, název)
REŽISÉR (<u>id_režisér</u>, jméno, příjmení) 
OCENĚNÍ (<u>id_ocenění</u>, název, rok) 
HEREC_FILM (<u><i>id_herec</i></u>, <u><i>id_film</i></u>) 
FILM_OCENĚNÍ (<u><i>id_film</i></u>, <u><i>id_ocenění</i></u>)

Vytvořte SQL dotazy pro následující úkoly:

34. Vypište všechny filmy z tabulky "FILMY".
```sql
```
35. Vypište jména všech herců.
```sql
```
36. Vypište názvy všech žánrů.
```sql
```
37. Vypište jména všech režisérů.
```sql
```
38. Vypište filmy, ve kterých hrál herec s jménem "Tom" a příjmením "Hanks".
```sql
```
39. Aktualizujte rok filmu s názvem "Titanic" na 1997.
```sql
```
40. Vytvořte nový záznam v tabulce "OCENĚNÍ" pro film s názvem "Pulp Fiction" a rokem 1994.
```sql
```
41. Smažte záznam z tabulky "HEREC_FILM", který propojuje herce s ID 3 a film s ID 7.
```sql
```
42. Vypište filmy, které získaly ocenění v roce 2020.
```sql
```
43. Vypište počet ocenění, které získal film s názvem "Titanic".
```sql
```