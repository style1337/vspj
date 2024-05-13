## První zadání
Mějme tabulky (primární klíč označen <u>podrtženě</u>, cizí klíč *kurzívou*)
 ZÁKÁZNÍK (<u>id-z</u>, jméno, kredit),
 SPOJ (<u>kod</u>, dopravce, start, cíl),
 JÍZDENKA(<u>id-j</u>, *kod*, *id-z*, datum, odkud, kam, cena)

 všechny atributy jsou **NOT NULL**, význam a typy některých atributů:
 kredit - kredit, za který si zákazník může kupovat jízdenky *(int);*
 start, cíl - odkud kam jezdí daný spoj *(varchar);*
 odkud, kam - odkud kam jel daný zákazník na danou jízdenku *(varchar);*

Zapište v SQL dotazy
1. Vypište všechny zákazníky s nenulovým kreditem
2. Vypište zákazníky, kteří jeli spojem v celé jeho trase
3. Vypište počet cestujících, kteří jeli včera s Regiojetem z Brna do Prahy
4. Vypište jména zákazníku, kteří nikdy nejeli do Ostravy.
5. Vypište kódy spojů do Telče s počty cestujících, v nichž jelo včera víc než 40 lidí,
6. Přidejte k tabulce Spoj nový datumový sloupce Jezdí-od, který bude NOT NULL. *Nezapomeňte reflektovat možný konflikt v případě, že* tabulka již obsahuje nějaké data
7. Odstraňte ze sloupce `dopravce` v tabulce `Spoj` integritní omezení NOT NULL

## Druhé zadání
Mějme tabulky (primární klíč označen <u>podrtženě</u>, cizí klíč *kurzívou*)
 KLIENT (<u>id-klient</u>, jméno-klient, kredit),
 KURS (<u>název-kurs</u>, popis, trvání),
 LEKTOR(<u>id-lektor</u>, jméno-lektor, kvalifikace),
 TRÉNINK(<u>id-trénink</u>, *id-lektor*, *název-kurs*, datum,čas),
 ÚČAST(<u><i>id-trénink</i></u> ,<u><i>id-klient</i></u>, cena).

Zapište v SQL dotazy
8. Vypište všechny klienty, jejichž jméno končí na "ová".
9. Vypište tréninky *(pouze atributy tréninků)*, které odcvičili včera lektoři s kvalifikací "Fyzioterapeut".
10. Vypište celkovou cenu tréninků jógy tento týden.
11. Vypište názvy kursů a pro každý z nich celkový počet v minulosti odcvičených tréninků a jejich celkovou cenu, seřaďte sestupně podle počtu tréninků.
12. Vypište `id` a `jména lektorů` spolu s počtem odcvičených klientů *(různých: každý klient se zde počítá jen jednou),* kteří mají tento počet vyšší než 50.
13. Vypište jména klientů, kteří se zůčastnili všech tréninků krav-magy, které se kdy konaly.
14. Vypište všechny kursy, trvající méně než dvě hodiny
15. Vypište jména a kredit klientů, kteří v minulém týdnu cvičil s lektorkou Janou
16. Přidejte k tabulce Klient nový textový sloupec Bydliště, který bude NOT NULL. Nezapomeňte reflektovat možný konflikt v případě, že tabulka již obsahuje nějaká data.
17. Vypište id a jména klientů a pro každého z nich celkový počet absolvovaných tréniků a jejich celkovou cenu, seřaďte sestupně podle počtu tréninků. Správně ošetřete případy klientů, kteří zatím neabsolvovali žádný trénink.
18. Vypište jména lektorů spolu s počtem odcvičených klientů (různých: každý klient se zde počítá jen jednou) v kursu "krav maga", kteří mají tento počet vyšší než 100.
19. Zvyšte ceny tréninků s id=11 o 20%.

## Třetí zadání

Mějme následující tabulky pro evidenci studentů, předmětů a jejich přihlášek (primární klíče označeny <u>podtržením</u>, cizí klíče _kurzívou_):

STUDENT (<u>id_student</u>, jméno, příjmení, rok_narození) 
PŘEDMĚT (<u>id_předmět</u>, název, kredity) 
PŘIHLÁŠKA (<u><i>id_student</i></u>, <u><i>id_předmět</i></u>, datum_přihlášení)

Vytvořte SQL dotazy pro následující úkoly:

20. Vypište všechny studenty z tabulky "STUDENT".
21. Vypište názvy všech předmětů.
22. Vypište jména a příjmení studentů, kteří jsou přihlášeni k předmětu s názvem "Matematika".
23. Vypište počet přihlášek na každý předmět.
24. Vypište studenty, kteří jsou přihlášeni alespoň ke třem předmětům.
25. Vypište předměty, které mají více než 5 kreditů.
26. Vypište studenty, kteří se přihlásili k předmětu alespoň před rokem 2020.

## Čtvrté zadání

Mějme následující tabulky pro evidenci zaměstnanců, oddělení, projektů a jejich propojení (primární klíče označeny <u>podtržením</u>, cizí klíče _kurzívou_):

ZAMĚSTNANCI (<u>id_zaměstnanec</u>, jméno, příjmení, pozice) 
ODDĚLENÍ (<u>id_oddělení</u>, název, vedoucí_oddělení) 
PROJEKTY (<u>id_projekt</u>, název, popis) 
PROPIS (<u><i>id_zaměstnanec</i></u>, <u><i>id_oddělení</i></u>, <u><i>id_projekt</i></u>, datum_nástupu)

Vytvořte SQL dotazy pro následující úkoly:

27. Vypište všechny zaměstnance z tabulky "ZAMĚSTNANCI".
28. Vypište názvy všech oddělení.
29. Vypište názvy všech projektů.
30. Vypište zaměstnance, kteří jsou vedoucími oddělení.
31. Vypište zaměstnance, kteří pracují na projektu s názvem "Nový produkt".
32. Vypište počet zaměstnanců v každém oddělení.
33. Vypište názvy projektů, na kterých pracuje alespoň 3 zaměstnanci.

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
35. Vypište jména všech herců.
36. Vypište názvy všech žánrů.
37. Vypište jména všech režisérů.
38. Vypište filmy, ve kterých hrál herec s jménem "Tom" a příjmením "Hanks".
39. Aktualizujte rok filmu s názvem "Titanic" na 1997.
40. Vytvořte nový záznam v tabulce "OCENĚNÍ" pro film s názvem "Pulp Fiction" a rokem 1994.
41. Smažte záznam z tabulky "HEREC_FILM", který propojuje herce s ID 3 a film s ID 7.
42. Vypište filmy, které získaly ocenění v roce 2020.
43. Vypište počet ocenění, které získal film s názvem "Titanic".