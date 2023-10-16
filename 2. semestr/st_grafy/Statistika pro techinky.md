## Info k testu

"*Test můžeme psát na svém pc, zápočty jsou **29.5. a 30.5. je předtermín**, ofc **nemůžeme mít svoje pomůcky**, ale logicky to půjde ojebat, všechny pomocné výpočty do excelu a ten excel taky odevzdáváme, test bude mí 23b a potřebujeme min 50%, přečtěte si pořádně zadání kvůli zaokrouhlování. Naběhl na mě Ondřej Liška a řekl mi ať to sem napíšu*" - scrxtch *(16.05.2023 15:40)*

----

## Kontigenční tabulky 
## Četnosti
## Čtvercová kontigence
## Vypočtěte všechny Vám známé koeficienty kontingence a výsledek se pokuste slovně interpretovat. 

----
# Relativní četnost
$$p_i=\frac{n_i}{n} $$
Tento vzorec počítá relativní četnost jednotlivých jevů vzhledem k celkovému počtu jevů. Zde je vysvětlení jednotlivých symbolů:

- $p_i$ je relativní četnost jevu $i$. Vyjadřuje, jaký podíl jevu $i$ tvoří v celkovém počtu jevů.
- $n_i$ je počet výskytů jevu $i$.
- $n$ je celkový počet jevů (tj. součet počtů všech jevů).

# Kumulativní četnost
$$kn_{i}= \sum_{j=1}^{i}n_j$$
V tomto vzorci se počítá kumulativní frekvence nebo kumulativní četnost. Zde je vysvětlení jednotlivých symbolů:

- $kn_i$ je kumulativní frekvence nebo kumulativní četnost jevu $i$. Vyjadřuje součet frekvencí (či četností) jevů od prvního jevu až po jev $i$ včetně.
- $n_j$ je frekvence (či četnost) jevu $j$.
- $i$ je index posledního jevu, pro který se počítá kumulativní frekvence.

Vzorec sumuje frekvence (či četnosti) jevů od prvního jevu až po jev $i$ (včetně něj), což poskytuje kumulativní frekvenci nebo kumulativní četnost pro daný jev. Tento vzorec se často používá při analýze četností jevů nebo při tvorbě kumulativních distribučních funkcí.

Pro lepší pochopení uvádím příklad: Představte si, že máte sadu dat, která zaznamenává počet výskytů různých slov ve větě. Pokud byste měli několik slov a jejich frekvence, můžete použít tento vzorec ke kumulativnímu sčítání frekvencí jednotlivých slov, abyste získali kumulativní frekvence pro každé slovo v pořadí.

Například, pokud máme následující frekvence slov: $n_1 = 3$, $n_2 = 2$, $n_3 = 4$, potom:

$k n_1 = n_1 = 3$

$k n_2 = n_1 + n_2 = 3 + 2 = 5$

$k n_3 = n_1 + n_2 + n_3 = 3 + 2 + 4 = 9$

V tomto příkladu jsme získali kumulativní frekvence pro každé slovo v pořadí. První slovo má frekvenci 3, druhé slovo má frekvenci 2 a celkem 5 výskytů (součet frekvence prvního a druhého slova), třetí slovo má frekvenci 4 a celkem 9 výskytů (součet frekvence prvního, druhého a třetího slova).

# Kumulativní relativní četnost
$$kp_{i}= \sum_{j=1}^{i}p_j$$

-----
# Typy grafů
1. Sloupcový graf:
 - Sloupcový graf je jedním z nejčastěji používaných typů grafů v statistice.
 - Používá se k vizualizaci diskrétních dat a porovnávání hodnot mezi různými kategoriemi.
 - Na vodorovné ose jsou zobrazeny kategorie a na svislé ose jsou zobrazeny hodnoty.
 ![Obrazek1](2.%20semestr/st_grafy/sloupcovy_graf.png)
2. Histogram:
 - Histogram je grafické zobrazení spojitých dat rozdělených do skupin (binů).
 - Slouží k vizualizaci frekvencí nebo relativních četností jednotlivých hodnot v datové sadě.
 - Na vodorovné ose jsou zobrazeny hodnoty a na svislé ose jsou zobrazeny frekvence nebo relativní četnosti.
![Obrazek1](2.%20semestr/st_grafy/histogram.png)
3. Liniový graf:
 - Liniový graf se používá pro zobrazení trendů a změn v čase.
- Používá se pro vizualizaci spojitých dat, například časových řad.
- Bodové hodnoty jsou propojeny linií, které ukazují trend v datové sadě.
![Obrazek1](2.%20semestr/st_grafy/liniovy_graf.png)
4. Bodový graf:
- Bodový graf je používán k zobrazení vztahu mezi dvěma spojitými proměnnými.
- Každý bod na grafu reprezentuje jeden pár hodnot z datové sady.
- Pomocí bodového grafu lze analyzovat korelaci mezi proměnnými nebo identifikovat vzory ve vztahu.
![Obrazek1](2.%20semestr/st_grafy/bodovy_graf.png)
5. Kruhový graf: 
- Kruhový graf se používá pro zobrazení složení celku nebo procentuálního rozložení kategorií.
 - Každá kategorie je zobrazena jako část kruhu, která reprezentuje její podíl na celku.
![Obrazek1](2.%20semestr/st_grafy/kruhovy_graf.png)
6. Krabicový graf (Boxplot):
- Krabicový graf je grafická metoda pro zobrazení souboru dat a statistických ukazatelů.
- Zobrazuje rozložení datové sady pomocí kvartilů, mediánu, extrémů a případně i odlehlých hodnot.
![Obrazek1](2.%20semestr/st_grafy/boxovy_graf.png)
7. Scatterplot (Rozptylový graf): 
- Scatterplot je grafická metoda pro zobrazení vztahu mezi dvěma spojitými proměnnými.
- Každý bod na grafu reprezentuje jednu hodnotu páru proměnných.
- Scatterplot se používá k analýze korelace a identifikaci vzorů ve vztahu.
![Obrazek1](2.%20semestr/st_grafy/scattlerplot.png)


