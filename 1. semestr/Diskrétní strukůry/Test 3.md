1. **Množina přirozených čísel (N):**
    
    - Příklad: ($N = {0, 1, 2, 3, 4, \ldots}$)

2. **Množina celých čísel (Z):**
    
    - Příklad: ($Z = {\ldots, -3, -2, -1, 0, 1, 2, 3, \ldots}$)
    

3. **Množina racionálních čísel (Q):**
    
    - Příklad: ($Q = {\frac{1}{2}, -\frac{3}{4}, 3, 0, \frac{7}{1}, \ldots}$) (kde čísla mohou být zlomky nebo celá čísla)
    

4. **Množina reálných čísel (R):**
    
    - Příklad: ($R = {-\sqrt{2}, -1, 0, 1, \frac{3}{4}, \pi, 2.5, \ldots}$) (kde čísla mohou být racionální i iracionální)
    

5. **Množina komplexních čísel (C):**
    
    - Příklad: ($C = {3 + 4i, -2i, 1, -\sqrt{2} + \frac{5}{2}i, \ldots}$) (kde (i) je imaginární jednotka)

## Část I: Množiny, relace, zobrazení
#### 1. Zvolte si tři libovolné čtyřprvkové množiny A,B,C tak, že $A \cup B \cap C$. Ukažte na nich, zda platí rovnost $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$. *(2 body)*
---
$A=\{1,2,3,4\}$
$B=\{5,6,7,8\}$
$C=\{9,10,11,12\}$

**Dosadíme:**
$$A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$$
$$A \cup (∅) = \{1,2,3,4,5,6,7,8\} \cap \{1,2,3,4,9,10,11,12\}$$
$$\{1,2,3,4\} \cup (∅) = \{1,2,3,4\}$$
$$\{1,2,3,4\} = \{1,2,3,4\}$$

#### 2. Najděte příklad zobrazení $f: ℕ \rightarrow ℕ$ pro které platí, že je bijektivní, ale není surjektivní (na) *(4 body)*
---
##### Injektivní (prosté)
- **Prosté zobrazení**, nebo také **injektivní zobrazení**, **injekce**, **monomorfismus,** je druh [zobrazení](https://cs.wikipedia.org/wiki/Zobrazen%C3%AD_(matematika)) mezi [množinami](https://cs.wikipedia.org/wiki/Mno%C5%BEina), které různým vzorům ([prvkům](https://cs.wikipedia.org/wiki/Prvek_mno%C5%BEiny)) přiřazuje různé obrazy. Nestane se tedy, že by jeden obraz měl několik různých vzorů a jeden vzor více obrazů. K prostému zobrazení existuje [inverzní zobrazení](https://cs.wikipedia.org/wiki/Inverzn%C3%AD_zobrazen%C3%AD)
![[img/Pasted image 20240106200434.png]]
##### Surjektivní (zobrazení na)
- Surjektivní zobrazení zajišťuje, že každý prvek ve cílové množině má alespoň jeden předobraz ve zdrojové množině. To znamená, že zobrazení pokrývá celou cílovou množinu.
- **Zobrazení na**, nebo také **surjektivní zobrazení**, **surjekce**, **epimorfismus**, je druh zobrazení mezi množinami, které zobrazuje na celou cílovou množinu. Každý prvek cílové množiny má tedy alespoň jeden vzor. Tudíž [obor hodnot](https://cs.wikipedia.org/wiki/Obor_hodnot) je celá cílová množina.
![[img/Pasted image 20240106200527.png]]
##### Bijektivní zobrazené
- Bijektivní zobrazení je zobrazení, které je zároveň injektivní a surjektivní. Každý prvek ze zdrojové množiny má jedinečný obraz ve cílové množině a zároveň každý prvek ve cílové množině má alespoň jeden předobraz ve zdrojové množině.
![[img/Pasted image 20240106200720.png]]
##### Inverzní zobrazení
- Inverzní jde pouze k bijektivnímu zobrazení

Nyní k příkladu zobrazení $f: ℕ \rightarrow ℕ$:

- Nejde udělat jelikož aby byl bijektivní tak musí nastat **surjektivita** a **injektivní**, zároveň.

#### 3. Jsou dány množiny $A = \{a, b, c, d\}$ a $B = \{b, c, d, e\}$. Dále je dáno zobrazení $f: A \rightarrow B$ takto: $f(a) = b$, $f(b) = c$, $f(c) = d$, $f(d) = d$. Určete, zda je zobrazení $f$ injektivní, surjektivní, bijektivní. Pokud je to možné, najděte inverzní zobrazení a určete jeho definiční obor. Pokud to možné není, zdůvodněte proč. *(5 bodů)*
----
- **Injektivita (jednoznačnost):** Zobrazení je injektivní, pokud různým prvkům v $A$ přiřazuje různé prvky v $B$. 

- **Definiční obor** je $A$ a v případě inverzního zobrazení to je cílová množina, takže $B$

Podívejme se na pravidla zobrazení:
   - $f(a)=b$
   - $f(b)=c$
   - $f(c)=d$
   - $f(d)=d$
$d$ má dva vzory takže není **injektivní**

- **Surjektivita (na):** Zobrazení je surjektivní, pokud každý prvek v $B$ má alespoň jednu předobraz v $A$. 

Podívejme se na obraz $B$ vytvořený zobrazením $f$:
- Obraz $B$ je $\{b,c,d\}$.
- Některé prvky z $B$ (například $e$) nemají předobraz v $A$, takže zobrazení $f$ není surjektivní.

- **Bijektivita:** Zobrazení je bijektivní, pokud je zároveň injektivní a surjektivní. V tomto případě zobrazení není surjektivní, takže není bijektivní.
- **Inverzní zobrazení:** Zobrazení $f$ není bijektivní, takže nemá inverzní zobrazení.

Celkově lze říci, že zobrazení $f$ je injektivní, ale není surjektivní ani bijektivní. Inverzní zobrazení neexistuje.

##### Injektivní (prosté)
- **Prosté zobrazení**, nebo také **injektivní zobrazení**, **injekce**, **monomorfismus,** je druh [zobrazení](https://cs.wikipedia.org/wiki/Zobrazen%C3%AD_(matematika)) mezi [množinami](https://cs.wikipedia.org/wiki/Mno%C5%BEina), které různým vzorům ([prvkům](https://cs.wikipedia.org/wiki/Prvek_mno%C5%BEiny)) přiřazuje různé obrazy. Nestane se tedy, že by jeden obraz měl několik různých vzorů a jeden vzor více obrazů. K prostému zobrazení existuje [inverzní zobrazení](https://cs.wikipedia.org/wiki/Inverzn%C3%AD_zobrazen%C3%AD)
![[img/Pasted image 20240106200434.png]]
##### Surjektivní (zobrazení na)
- Surjektivní zobrazení zajišťuje, že každý prvek ve cílové množině má alespoň jeden předobraz ve zdrojové množině. To znamená, že zobrazení pokrývá celou cílovou množinu.
- **Zobrazení na**, nebo také **surjektivní zobrazení**, **surjekce**, **epimorfismus**, je druh zobrazení mezi množinami, které zobrazuje na celou cílovou množinu. Každý prvek cílové množiny má tedy alespoň jeden vzor. Tudíž [obor hodnot](https://cs.wikipedia.org/wiki/Obor_hodnot) je celá cílová množina.
![[img/Pasted image 20240106200527.png]]
##### Bijektivní zobrazené
- Bijektivní zobrazení je zobrazení, které je zároveň injektivní a surjektivní. Každý prvek ze zdrojové množiny má jedinečný obraz ve cílové množině a zároveň každý prvek ve cílové množině má alespoň jeden předobraz ve zdrojové množině.
![[img/Pasted image 20240106200720.png]]
##### Inverzní zobrazení
- Inverzní jde pouze k bijektivnímu zobrazení

#### 4. Mějme binární relaci $R$ na množině $ℕ$. Zobrazíme-li tuto relaci do kartézských souřadnic, dostaneme všechny body kromě diagonály *(osy 1. kvadrantu)*. Je tato relace ekvivalencí? Zdůvodněte a ukažte na příkladu. *(5 bodů)*
---
- Ekvivalence relace vyžaduje, aby byla splněna tři podmínky: **reflexivita**, **symetrie** a **tranzitivita**.
1. **Reflexivita**: Relace $R$ je reflexivní, pokud pro každé $n \in ℕ$ platí $(n, n) \in R$. **To znamená, že všechny body na diagonále by měly být obsaženy v $R$.**

2. **Symetrie**: Relace $R$ je symetrická, pokud z $(a, b) \in R$ vyplývá, že $(b, a) \in R$. **Symetrie znamená, že body lze "zrcadlit" podle diagonály.**
 
3. **Tranzitivita**: Relace $R$ je tranzitivní, pokud z $(a, b) \in R$ a $(b, c) \in R$ vyplývá, že $(a, c) \in R$. **Tranzitivita zajišťuje, že body lze propojit v horizontálním nebo vertikálním směru.**

Pokud graf relace neobsahuje diagonálu, znamená to, že není reflexivní, a tedy není ekvivalencí.


#### 5. Mějme binární relaci $R$ na množině $A=\{1,2,3\}$ obsahující následující prvky: $R=\{(1,1), (1,2), (1,3), (2,2), (2,3), (3,3)\}$. Odebíráním či přidáváním prvků změňte relaci tak, aby byla symetrická, zdůvodněte. *(4 body)*
---
- Chceme relaci změnit tak, aby byla symetrická. Symetrická relace zahrnuje všechny dvojice $(a, b)$, pokud obsahuje $(b, a)$. Jedním způsobem, jak dosáhnout symetrie, je přidávat chybějící symetrické prvky.

- Zjistíme, které prvky chybí v relaci. Pro každý prvek $(a, b)$ v relaci $R$, pokud $(b, a)$ není součástí relace, přidáme ho
	1. Přidáme $(2, 1)$, protože $(1, 2)$ je v relaci, ale $(2, 1)$ není.
	2. Přidáme $(3, 1)$, protože $(1, 3)$ je v relaci, ale $(3, 1)$ není.
	3. Přidáme $(3, 2)$, protože $(2, 3)$ je v relaci, ale $(3, 2)$ není.

Po těchto úpravách bude relace symetrická. Nová relace $R'$ bude vypadat takto:

$$R'=\{(1,1),(1,2),(1,3),(2,1),(2,2),(2,3),(3,1),(3,2),(3,3)\}$$

Nyní je relace $R'$ symetrická, protože obsahuje všechny původní prvky $R$ a jejich symetrické páry.

- Nebo napíšeme si body do grafu a pak je zrcadlíme
![[img/Pasted image 20240109144610.png]]

## Část II: Výroková a predikátová logika
#### 6. Zjistěte pravdivostní hodnotu formule *(2 body)*
---
- $(\neg a ∨ b) \Leftrightarrow (a \Rightarrow b)$
- $\exists x (x\neq z)$ přitom $x \in \{0,1\}$, $z \in \{0,1,2\}$

- Pravdivostní hodnota formule se zjišťuje podle pravdivostní tabulky

 Pravdivostní tabulka je jeden ze způsobů zápisu logických funkcí. Taková tabulka obsahuje pouze logické proměnné, které nejčastěji nabývají dvou hodnot **0** a **1** (nepravda a pravda, ne a ano).
- $2^n$, $n$ je počet vstup *(to znamená třeba: a,b,c)*
	- $2^3=8$ tedy 8 řádků
#### 7. Negujte formule *(4 body)*
---
- $(a \Rightarrow (( a \lor c) \Rightarrow b))$
	Negace: $a \land ((a \lor c) \land \neg b)$
- $\exists x [R(x) \land \neg Z(x)]$
	Negace: $\forall x [\neg R(x) \lor Z(x)]$

- Takto se neguje implikace
![[img/Pasted image 20240109150129.png]]

#### 8. Přeformulujte věty do formulí výrokového počtu a zjistěte, zda je věta pod čarou konsekventem *(sémantickým důsledkem)* vět nad čarou, zdůvodněte. (4 body)
---
- Vlakem jezdím jedině tehdy, pokud je náledí.
- Není náledí. 
- čára
- Nejedu vlakem.
  
$P$: Jedu vlakem.
$Q$: Je náledí.

- $P \rightarrow Q$ *(Vlakem jezdím jedině tehdy, pokud je náledí)*.
- $\neg Q$ *(Není náledí)*.
Věta pod čarou:
- $\neg P$ *(Nejedu vlakem)*.

$\{P \rightarrow Q,\neg Q\}$ je konsekventní, protože existuje model, kde obě věty nad čarou mohou být pravdivé zároveň.

Uvažme model, kde $P$ není pravdivé *(nejezdím vlakem)* a $Q$ není pravdivé *(není náledí)*. Tento model splňuje obě věty nad čarou, ale nesplňuje větu pod čarou.

Tedy věta pod čarou (Nejedu vlakem) je sémantickým důsledkem vět nad čarou.

Nechť S je "Všechny lidi jsou smrtelní" a K je "Každý člověk má srdce." Pokud platí, že ve všech situacích, kde jsou všichni lidé skutečně smrtelní (S je pravdivá), je pravdivé i to, že každý z nich má srdce (K). Pak můžeme říci, že K je konsekventní s S nebo že K je sémantickým důsledkem S.

**Zjišťujeme konsekvent**
- **Konsekvent laijkcy.** Vezemem ty **předchozíi** řádky kde jsou **dve jedničky**, pokud jsou **dve jedničky v tom řádku** i u vysledné, tak poté **je to konsvekvent**
#### 9. Zadanou formuli vyjádřete pravdivostní tabulkou a zapište ji v CNF. Formuli v CNF znegujte. *(4 body)*
---
$(\neg a \lor b) \Rightarrow (b XOR a)$

Nejprve si připomenme, jak jsou definovány některé logické operátory:

- $\neg$ značí negaci (NOT),
- $\lor$ značí disjunkci (OR),
- $\land$ značí konjunkci (AND),
- $\Rightarrow$ značí implikaci,
- $\oplus$ značí XOR (exkluzivní nebo).

- Abychom mohli udělat **DNF** a **CNF** musíme si nejdříve udělat pravdivostní tabulku
##### CNF 
- Podívame se ve výsledku na všechny **0** 
![[img/Pasted image 20240109154355.png]]
- Hledáme jakékoliv kombinace $A$ a $B$ kde nám vznikla nula
	- 0 = $\neg a$
	- 1 = $a$
	- Podle této teorie napíšu první dojci
	  $(\neg a \lor \neg b)$
	  A když bych chtěl přidat další dvojci tak je spojíme znaménkem **konjunkce** ($\lor$)
	  $(\neg a \lor \neg b) \lor (a \lor b)$

- Když negujeme **CNF**
	- Tak jen vyměníme znaky konjunkce ($\lor$) za znaky disjunkce ($\land$)
	- A znegujeme samostatné znaky $a$ a $b$

##### DNF 
- Podívame se ve výsledku na všechny **1** 
![[img/Pasted image 20240109154355.png]]
- Hledáme jakékoliv kombinace $A$ a $B$ kde nám vznikla jednička
	- 0 = $\neg a$
	- 1 = $a$
	- Podle této teorie napíšu první dojci, ve vnitř závorky bude konjunkce ($\land$)
	  $(\neg a \land b)$
	  A když bych chtěl přidat další dvojci tak je spojíme znaménkem **disjunkce** ($\lor$)
	  $(\neg a \land b) \lor ( a \land \neg b)$

- Když negujeme **DNF**
	- Tak jen vyměníme znaky disjunkce ($\lor$) za znaky konjunkce ($\land$)
	- A znegujeme samostatné znaky $a$ a $b$

#### 10. Pomocí uvedené interpretace zapište formule odpovídající výrokům. Vytvořené formule negujte a potom znegované formule vyjádřete přirozeným jazykem. *(6 bodů)*
---
**Interpretace**: 
- lidé
- $S(x)$ – být slepý 
- $H(x)$ – být hluchý
- $D(x)$ – mít dobrý sluch
- $b$ – Bob.

1. Hluší lidé nebo lidé se špatným sluchem nemohou být slepí.
	1. $\forall x [H(x) \lor \neg D(x)] \Rightarrow \neg S(x)$ 
	2. **Negace**: $\exists x [H(x) \lor \neg D(x)] \land S(x)$
2. Lidé jsou buď hluší nebo mají dobrý sluch nebo mají špatný sluch.
	1. $\forall x [H(x) \lor D(x) \lor \neg D(x)]$
	2. **Negace**: $\exists [H(x) \lor \neg D(x)] \land S(x)]$
3. Bob musí být hluchý i slepý.
	1. $H(b) \land S(b)$
	2. **Negace**: $\neg H(b) \lor S(b)$
4. Jestli má Bob dobrý sluch, tak jsou všichni lidé hluší
	1. $D(b) \Rightarrow ( \forall x H(x))$


| Operace | Symboly | Výraz | Význam | Čteme |
| ---- | ---- | ---- | ---- | ---- |
| Konjunkce | $\land$ | $A \land B$ | $A$, $B$ musí být 1 | Výrok $a$ *(zároveň)* výrok $q$ |
| Disjunkce | $\lor$ | $A \lor B$ | $A$ nebo v $B$ musí být 1 | Výrok $a$ nebo výrok $q$ |
| Negace | $\neg$ | $\neg A$ | Pravdivý, pokud $A$ je nepravdivé | Negace $a$ |
| Implikace | $\Rightarrow$ | $A \Rightarrow B$ | Když $1 \Rightarrow 0$ tak je **nepravda**, jinak je to vždy pravdea | Jestliže výrok $a$, pak $q$ |
| Ekvivalence | $\Leftrightarrow$ | $A \Leftrightarrow B$ | Pravdivý, pokud $A$ a $B$ mají stejné hodnoty | Výrok $p$ právě tehdy když výrok $q$ |
| Obecný kvantifikátor | $\forall$ |  | Pro všechna |  |
| Existeční kvantifikátor | $\exists$ |  | 	Existuje alespoň něco co pro něco platí. *(Alespoň jeden člověk)* |  |
[Zdroj](https://www.youtube.com/watch?v=xAXw3c1VioU)
##### Při negaci
- Se obecný kvantifikátor mění na existeční:  $∀ \rightarrow ∃$
- Se existeční kvantifikátor mění na obecný: $∃ \rightarrow ∀$

## Část III: Teorie grafu
#### 11. Mějme graf na obrázku
---
![[img/teorie_grafu.png]]
##### 11.1. Najděte minimální kostru. Použijte Jarníkův-Primův algoritmus, řešte tak, aby bylo vidět, jak algoritmus pracuje *(6 bodů)*

- Použít [Jarníkův-Primův algoritmus](https://cs.wikipedia.org/wiki/Jarn%C3%ADk%C5%AFv_algoritmus)
- Pro každy krok nakreslit jiny obrazek
- hledani *(začínání)* odkudkoliv
	- Postupujeme v grafu po nejmenších hodnotách
- začneme s jednou bodu a vytvařime část kostry – v dalším kroku zkoumáme sousedy a vždy přidame ten s **nejmenší vzdalenosti**
- zkoumáme všechny sousedy, ale davat hrany pokud byla použita už nemůžeme – **neuzavíráme oblouk**
- **vždy zkoumáme všechny uzlíky**

[Správné a detailnější řešení je zde](https://cs.wikipedia.org/wiki/Jarn%C3%ADk%C5%AFv_algoritmus)

##### 11.2. Najděte systém nejkratších cest z uzlu E do všech uzlů. Použijte Dijkstrův algoritmus, řešte tak, aby bylo vidět, jak algoritmus pracuje *(6 bodů)*
[Zde](https://www.youtube.com/watch?v=J8Cce722fkY)

#### 12. Uvažujme následující zobecnění systematického průchodu binárním stromem T (symboly L(T), resp. R(T) označují levý, resp. pravý podstrom stromu T): (6 body)
---
1. ()-inorder: vypiš znak ( tj. levou závorku, projdi L(T), vypiš kořen, projdi P(T),
vypiš znak ) tj. pravou závorku
2. ()-postorder: vypiš znak ( tj. levou závorku, projdi L(T), projdi P(T), vypiš kořen,
vypiš znak ) tj. pravou závorku
Projděte oběma způsoby níže uvedený strom.

![[img/binarni_strom.png]]

Inorder, Preorder a Postorder jsou tři různé způsoby, jak procházet binární stromy. Binární strom je hierarchická datová struktura skládající se z uzlů (nebo vrcholů), kde každý uzel může mít až dva potomky, levého a pravého.

1. **Inorder (levý podstrom - kořen - pravý podstrom):**
    - Projde levý podstrom.
    - Navštíví kořen.
    - Projde pravý podstrom.

- **Preorder (kořen - levý podstrom - pravý podstrom):**
    - Navštíví kořen.
    - Projde levý podstrom.
    - Projde pravý podstrom.
    
- **Postorder (levý podstrom - pravý podstrom - kořen):**
    - Projde levý podstrom.
    - Projde pravý podstrom.
    - Navštíví kořen.
![[img/Pasted image 20240109161939.png]]
- Vždy jdeme do **leva** a počítme kolikrát potkáme daný znak
- U **Inorder**, zapisejeme při druhým potkání znaku
- U **Preorder**, zapisujeme při prvním potkání znaku
- U **Postorder**, zapisujeme při posledním potkání
#### 13. Mějme libovolný úplný symetricky orientovaný graf. Jak bude vypadat jeho kondenzace? Zdůvodněte *(2 body)*
---

- kondenzace bude tvořena jediným uzlem, protože úplný sym. orientovaný graf je celý silněsouvislý (je celý jednou silnou komponentou), z níž pak kondenzací vznikne onen uzel

- Kondenzace, je souvisla komponenta, když je tvořena jedním uzlem

##### Když by náhodou byl nesymetrický
- Celkově lze říci, že kondenzace nesymetrického grafu bude reflektovat strukturu silně souvislých komponent v původním grafu.
![[img/Pasted image 20240109162607.png]]


#### Nebylo v testu ale
##### Bylo v testu 4.1.2023
###### Huffmanovo kódování
