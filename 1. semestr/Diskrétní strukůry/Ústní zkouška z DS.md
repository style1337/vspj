## Teorie množin
### Co je množina, podmnožina, univerzum? Jak se dokáže rovnost množin?
- **Množina** je matematický koncept, který představuje **sbírku objektů**, které jsou nazývány prvky této množiny. Prvky mohou být cokoli - **čísla, písmena, geometrické tvary nebo jiné matematické objekty**. Množiny jsou obvykle zapisovány v závorkách, například $\{1, 2, 3\}$.
- **Podmnožina** je množina, která obsahuje pouze prvky, které jsou také prvky jiné množiny. Symbolicky se podmnožina zapisuje jako $⊆$. 
	- Například, pokud máme množinu $A = \{1, 2\}$ a množinu $B = \{1, 2, 3\}$, pak množina $A$ je podmnožinou množiny $B (A ⊆ B)$.
- **Univerzum** *(nebo také univerzální množina)* je množina, která obsahuje všechny prvky, o kterých diskutujeme v daném kontextu. Symbolicky je často reprezentována písmenem $U$. Univerzum může být například všechna přirozená čísla, reálná čísla nebo něco jiného podle kontextu.
- **Rovnost množin** je zjišťována tím, zda dvě množiny obsahují stejné prvky. Množina $A$ je rovna množině $B$, pokud mají tyto množiny stejné prvky. Symbolicky se to zapisuje jako $A = B$. 
	- Například, pokud máme množinu $C = \{1, 2, 3\}$ a množinu $D = \{3, 2, 1\}$, pak jsou tyto množiny rovny, protože obsahují stejné prvky, i když jsou zapsány v jiném pořadí ($C = D$).
### Definujte množinové operace – doplněk, průnik, sjednocení, rozdíl.

- **Doplněk** 
    - **Definice**: Doplněk množiny $A$ vzhledem k univerzální množině $U$ obsahuje všechny prvky univerzální množiny, které nejsou v množině A.
    - Symbolická reprezentace: Doplněk množiny $A$ se značí jako $A'$ nebo $A‾A$.
- **Průnik:**
    - **Definice**: Průnik dvou množin $A$ a $B$ obsahuje všechny prvky, které jsou současně obsaženy v obou množinách $A$ i $B$.
    - Symbolická reprezentace: Průnik množin $A$ a $B$ se značí jako $A ∩ B$.
- **Sjednocení:**
    - **Definice**: Sjednocení dvou množin $A$ a $B$ obsahuje všechny prvky, které jsou obsaženy alespoň v jedné z množin $A$ nebo $B$ *(nebo v obou)*.
    - Symbolická reprezentace: Sjednocení množin $A$ a $B$ se značí jako $A$ $∪$ $B$.
- Rozdíl: 
    - **Definice**: Rozdíl dvou množin $A$ a $B$ obsahuje všechny prvky množiny $A$, které nejsou obsaženy v množině $B$.
    - Symbolická reprezentace: Rozdíl množin $A$ a $B$ se značí jako $A - B$.
3. Co je kartézský součin, jak pracuje, co je výsledkem?
   - **Kartézský součin** je matematická operace, která vytváří novou množinu tím, že kombinuje všechny možné páry prvků ze dvou (nebo více) **množin**
   - Pokud máme dvě množiny $A$ a $B$, pak kartézský součin $A x B$ je definován jako množina všech možných uspořádaných dvojic *(a, b)*, kde a je prvek z množiny $A$ a $b$ je prvek z množiny $B$.
  - Symbolicky se kartézský součin zapisuje jako $A×B$ nebo $A x B$.
### Co je charakteristická funkce, k čemu se používá?
- Charakteristická funkce, také nazývaná indikátorová funkce, je matematická funkce, která přiřazuje každému prvku množiny hodnotu 0 nebo 1 v závislosti na tom, zda prvek patří nebo nepatří do dané množiny. Tato funkce se často používá v teorii pravděpodobnosti, statistice a dalších oblastech matematiky.

### Ukažte de Morganovy zákony s využitím doplňku a universa, můžete použít Vennův diagram.
- De Morganovy zákony jsou matematické vztahy mezi doplňky množin, které popisují vztahy mezi operacemi sjednocení a průniku.
- 1. **První De Morganův zákon:** $A∪B‾=A‾∩B‾$
	
    To znamená, že doplněk sjednocení dvou množin je roven průniku jejich doplňků.
    
2. **Druhý De Morganův zákon:** $A∩B‾=A‾∪B‾$
    
    To znamená, že doplněk průniku dvou množin je roven sjednocení jejich doplňků.
    

- Na Vennových diagramech je modrá oblast množina $A$, oranžová oblast množina $B$, šedá oblast doplněk množiny $A$, a zelená oblast doplněk množiny $B$. Červená oblast na prvním diagramu reprezentuje doplněk sjednocení $A∪B‾$, a na druhém diagramu reprezentuje doplněk průniku $A∩B‾$.

###  Co je mohutnost množiny? Jaká je mohutnost kartézského součinu dvou množin?
- **Mohutnost** *(nebo také kardinalita)* množiny měří počet prvků v této množině.
- **Mohutnost kartézského součinu dvou množin** je tedy rovna mohutnosti první množiny krát mohutnost druhé množiny.

### Jak se porovnává mohutnost dvou nekonečných množin?
- V jednoduchosti lze říci, že nekonečné množiny jsou velké různými způsoby, a matematikové používají kardinální čísla k vyjádření těchto různých stupňů nekonečnosti. Mohutnost se porovnává pomocí pojmu bijekce, která říká, zda lze každému prvku v jedné množině přiřadit právě jeden prvek v druhé množině, a naopak.

### Co je (binární, n-ární) relace?
#### Binární relace
- **Binární relace** je speciální typ relace, která spojuje **dva prvky**, jeden z první množiny a druhý z druhé množiny. Formálně, relace $R$ nad množinami $A$ a $B$ je binární relací, pokud každý prvek $a$ z $A$ a každý prvek $b$ z $B$ platí, že buď $aRb$ *(prvek $a$ je v relaci s prvkem $b$), nebo neplatí $aRb$ (prvek $a$ není v relaci s prvkem $b$)*.
#### N-árni relace
- N-ární relace se obecně vztahuje k vztahům mezi n-ticemi prvků z několika množin. Relace může spojovat více než dva prvky najednou.

### Co je inverzní relace? Nakreslete příklad.
- **Inverzní relace** je v matematice relace, která je vytvořena prohazováním prvků vstupní relace. 
- Jinými slovy, inverzní relace obsahuje všechny páry, které jsou vstupní relací otočené.

### Co je složená relace? Uveďte příklad.
- Složená relace je operace, která kombinuje dva nebo více relace tak, že výsledná relace obsahuje prvky, které jsou ve vstupních relacích spojeny. Operace složení relací se nazývá také kompozice relací.
#### TODO PŘÍKLAD

### Co je relace ekvivalence? Jaké má vlastnosti?
- Relace ekvivalence je speciální druh binární relace, která splňuje tři hlavní vlastnosti: reflexivitu, symetrii a tranzitivitu. Tyto vlastnosti jsou klíčové pro definování ekvivalence mezi prvky množiny.
- **Reflexivita:** Relace $R$ na množině $A$ je reflexivní, pokud pro každý prvek aa v množině $A$ platí $(a,a)∈R$.
- **Symetrie:** Relace $R$ na množině $A$ je symetrická, pokud pro každý prvek $a$ a $b$ platí, že pokud $(a,b)∈R$, pak $(b,a)∈R$.
- **Tranzitivita:** Relace $R$ na množině $A$ je tranzitivní, pokud pro každé $a,b,c$ platí, že pokud $(a,b)∈R$ a $(b,c)∈R$, pak $(a,c)∈R$.
### Co je relace uspořádání? Jaké má vlastnosti?
- Relace uspořádání je binární relace na množině, která splňuje tři základní vlastnosti: reflexivitu, antisymetrii a tranzitivitu. Tyto vlastnosti definují uspořádání prvků v množině vzhledem k dané relaci.
### Porovnejte lexikografické uspořádání čísel a běžné uspořádání čísel. 
Lexikografické uspořádání a běžné uspořádání čísel jsou dvě odlišné koncepce, které se používají k porovnání prvků, v tomto případě čísel, v různých kontextech.

1. **Běžné uspořádání čísel:**
    - Běžné uspořádání čísel je založeno na velikosti čísel samotných.
    - Čísla jsou uspořádána od nejmenšího po největší (nebo naopak) na základě jejich numerických hodnot.
    - Například v běžném uspořádání jsou čísla 1, 2, 3, 4, 5 uspořádána postupně podle jejich velikosti.
2. **Lexikografické uspořádání čísel:**
    - Lexikografické uspořádání se často používá k porovnání n-tic (uspořádaných souborů) nebo slov v abecedním pořadí.
    - Pokud máme n-tice čísel nebo slova, jsou uspořádány postupně podle hodnot jednotlivých složek n-tice.
    - Například při lexikografickém uspořádání čísel 11, 2, 3, 21 by byly uspořádány jako 2, 3, 11, 21, protože se nejprve porovnávají první číslice (2 a 1) a pak teprve druhé číslice.

Běžné uspořádání čísel se zakládá na jejich numerických hodnotách, zatímco lexikografické uspořádání čísel se zaměřuje na postupné porovnávání hodnot jednotlivých číslic. Lexikografické uspořádání se často používá v algoritmech, které pracují s textovými nebo symbolickými daty, zatímco běžné uspořádání je běžné při porovnávání čísel v aritmetických operacích.

### Co je zobrazení, jak souvisí s relací?
- Zobrazení je matematický pojem, který popisuje přiřazování prvků z jedné množiny do druhé množiny tak, že každý prvek z první množiny má právě jednoho partnera v druhé množině. Zobrazení tedy definuje, jak jsou prvky jedné množiny spojeny s prvky druhé množiny.
- Relace a zobrazení tedy souvisejí tak, že zobrazení může být reprezentováno pomocí relace, která zachycuje, jak jsou prvky jedné množiny spojeny s prvky druhé množiny.
###  Nakreslete příklad surjektivního/injektivního/bijektivního zobrazení a okomentujte.
#### TODO
###  Co je inverzní zobrazení a kdy existuje?
- Inverzní zobrazení je zobrazení, které **"vrací"** původní hodnoty z obrázku zobrazení.
1. **Injektivita (do):** Zobrazení musí být injektivní *(do)*. To znamená, že různým prvkům z $A$ jsou přiřazeny různé prvky v $B$. Pokud by existovaly dva různé prvky $a_1$​ a $a_2$​ v $A$ tak, že $f(a_1)=f(a_2)$, inverzní zobrazení by nebylo jednoznačně definováno.
    
2. **Surjektivita (na):** Zobrazení musí být surjektivní *(na)*. To znamená, že každý prvek v $B$ má alespoň jednoho předchůdce v $A$. Pokud některé prvky v $B$ nemají předchůdce, inverzní zobrazení nemůže být jednoznačně definováno pro všechny prvky v $B$.
### Definujte bijektivní zobrazení. Nakreslete příklad.
- Bijektivní zobrazení je speciální typ zobrazení mezi dvěma množinami, které je jak injektivní *(do)*, tak surjektivní *(na)*. Jinými slovy, bijektivní zobrazení zachovává jedinečnost prvků a zároveň obsahuje všechny prvky z množiny obrázku *(cílové množiny)*.

## Logika a indukce
1. Co je výrok a pravdivostní ohodnocení?
2. Co je výroková formule a její pravdivostní ohodnocení?
3. Co to je tautologie a kontradikce? Uveďte příklady.
4. Ukažte deMorganovy zákony, použijte pravdivostní tabulku.
5. Jak se negují složité formule pomocí principu duality?
6. Co je sémantický důsledek (konsekvent) a jak funguje?
7. Co je úplný systém logických spojek?
8. Co je CNF a DNF? K čemu se dají prakticky využít?
9. Jaký je princip důkazu matematickou indukcí?
10. Uveďte rozdíly mezi výrokovou a predikátovou logikou.
11. Z jakých symbolů se skládají formule predikátové logiky?
12. Co je term, formule, sentence?
13. Jak vypadá správně utvořená formule? Uveďte příklad.
14. Na co je lze aplikovat funkční symbol a na co predikátový symbol?
15. Vysvětlete, co to je sémantika a interpretace predikátové logiky.

## Grafy
1. Definujte neorientovaný a orientovaný graf?
2. Co je úplný graf? Co je úplný symetricky orientovaný graf?
3. Definujte stupeň uzlu u orientovaného/neorientovaného grafu.
4. Co je isomorfismus? Jak se zjišťuje?
5. Co je sled, tah, cesta, kružnice?
6. Co je souvislý neorientovaný graf a komponenta grafu?
7. Co je strom? Co je kostra grafu?
8. Co je spojení, orientovaný tah, orientovaná cesta, cyklus?
9. Co je silně souvislý graf, silná komponenta?
10. Co je kondenzace grafu? Jak ji vytvoříme?
11. Definujte list a kořen, předchůdce a následníka v orientovaném grafu.
12. Jak se zjistí, kolika tahy lze pokrýt neorientovaný graf?
13. Kdy lze neorientovaný/orientovaný graf pokrýt jedním uzavřeným tahem?
14. Co to je vzdálenost uzlů neohodnoceného grafu a jaké má vlastnosti?
15. Definujte kořenový strom, hloubku uzlu, hloubku stromu.
16. Jaké jsou základní způsoby reprezentace grafů?
17. Popište algoritmus pro nalezení nejkratší cesty mezi dvěma uzly grafu.
18. Popište algoritmus pro nalezení minimální kostry grafu.
19. Popište algoritmus pro rozklad grafu na silné komponenty.
20. Co to je topologické uspořádání uzlů grafu?
21. V čem se liší Jarníkův a Dijkstrův algoritmus?
22. Jaký je princip Huffmanova kódování a k čemu se využívá?