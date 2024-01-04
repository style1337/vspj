### Zobrazení (téma otázky 3)
#### Injektivní
- Injektivní zobrazení zajišťuje, že každý prvek ze zdrojové množiny má jedinečný obraz ve cílové množině. Jinými slovy, žádné dva různé prvky ze zdrojové množiny nemají stejný obraz
#### Surjektivní
- Surjektivní zobrazení zajišťuje, že každý prvek ve cílové množině má alespoň jeden předobraz *(duplicity)* ve zdrojové množině. To znamená, že zobrazení pokrývá celou cílovou množinu.
#### Bijektivní zobrazené
- Bijektivní zobrazení je zobrazení, které je zároveň injektivní a surjektivní. Každý prvek ze zdrojové množiny má jedinečný obraz ve cílové množině a zároveň každý prvek ve cílové množině má alespoň jeden předobraz *(duplicitu)* ve zdrojové množině.
#### Inverzní zobrazení
## Část I: Množiny, relace, zobrazení
1. Zvolte si tři libovolné čtyřprvkové množiny A,B,C tak, že $A \cup B \cap C$. Ukažte na nich, zda platí rovnost $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$.

$A=\{1,2,3,4\}$
$B=\{5,6,7,8\}$
$C=\{9,10,11,12\}$

**Dosadíme:**
$$A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$$
$$A \cup (∅) = \{1,2,3,4,5,6,7,8\} \cap \{1,2,3,4,9,10,11,12\}$$
$$\{1,2,3,4\} \cup (∅) = \{1,2,3,4\}$$
$$\{1,2,3,4\} = \{1,2,3,4\}$$
2. Najděte příklad zobrazení $f: ℕ \rightarrow ℕ$ pro které platí, že je bijektivní, ale není surjektivní (na)
$$f(n)=2n$$
- Zobrazení je bijektivní, protože je injektivní (různým číslům $n_1$ a $n_2$ jsou přiřazena různá čísla $2n_1$ a $2n_2$) a surjektivní (každé číslo $m$ je přiřazeno nějakým $n = \frac{m}{2}$).

- Nicméně, toto zobrazení není surjektivní (na), protože některá čísla z oboru hodnot (např. lichá čísla) nemají žádný předobraz v oboru definičním (přirozená čísla).

3. Jsou dány množiny $A = \{a, b, c, d\}$ a $B = \{b, c, d, e\}$. Dále je dáno zobrazení $f: A \rightarrow B$ takto: $f(a) = b$, $f(b) = c$, $f(c) = d$, $f(d) = d$. Určete, zda je zobrazení $f$ injektivní, surjektivní, bijektivní. Pokud je to možné, najděte inverzní zobrazení a určete jeho definiční obor. Pokud to možné není, zdůvodněte proč. 

- **Injektivita (jednoznačnost):** Zobrazení je injektivní, pokud různým prvkům v $A$ přiřazuje různé prvky v $B$. 

Podívejme se na pravidla zobrazení:
   - $f(a)=bf(a)=b$
   - $f(b)=cf(b)=c$
   - $f(c)=df(c)=d$
   - $f(d)=df(d)=d$
$d$ má dva vzory takže není **injektivní**

- **Surjektivita (na):** Zobrazení je surjektivní, pokud každý prvek v $B$ má alespoň jednu předobraz v $A$. 

Podívejme se na obraz $B$ vytvořený zobrazením $f$:
- Obraz $B$ je $\{b,c,d\}$.
- Některé prvky z $B$ (například $e$) nemají předobraz v $A$, takže zobrazení $f$ není surjektivní.

- **Bijektivita:** Zobrazení je bijektivní, pokud je zároveň injektivní a surjektivní. V tomto případě zobrazení není surjektivní, takže není bijektivní.
- **Inverzní zobrazení:** Zobrazení $f$ není bijektivní, takže nemá inverzní zobrazení.

Celkově lze říci, že zobrazení $f$ je injektivní, ale není surjektivní ani bijektivní. Inverzní zobrazení neexistuje.

. Mějme binární relaci $R$ na množině $ℕ$. Zobrazíme-li tuto relaci do kartézských souřadnic, dostaneme všechny body kromě diagonály *(osy 1. kvadrantu)*. Je tato relace ekvivalencí? Zdůvodněte a ukažte na příkladu.

- Ekvivalence relace vyžaduje, aby byla splněna tři podmínky: **reflexivita**, **symetrie** a **tranzitivita**.
1. **Reflexivita**: Relace $R$ je reflexivní, pokud pro každé $n \in ℕ$ platí $(n, n) \in R$. **To znamená, že všechny body na diagonále by měly být obsaženy v $R$.**

2. **Symetrie**: Relace $R$ je symetrická, pokud z $(a, b) \in R$ vyplývá, že $(b, a) \in R$. **Symetrie znamená, že body lze "zrcadlit" podle diagonály.**
 
3. **Tranzitivita**: Relace $R$ je tranzitivní, pokud z $(a, b) \in R$ a $(b, c) \in R$ vyplývá, že $(a, c) \in R$. **Tranzitivita zajišťuje, že body lze propojit v horizontálním nebo vertikálním směru.**

Pokud graf relace neobsahuje diagonálu, znamená to, že není reflexivní, a tedy není ekvivalencí.

5. Mějme binární relaci $R$ na množině $A=\{1,2,3\}$ obsahující následující prvky:
$R=\{(1,1), (1,2), (1,3), (2,2), (2,3), (3,3)\}$. Odebíráním či přidáváním prvků změňte relaci tak, aby byla symetrická, zdůvodněte.

- Chceme relaci změnit tak, aby byla symetrická. Symetrická relace zahrnuje všechny dvojice $(a, b)$, pokud obsahuje $(b, a)$. Jedním způsobem, jak dosáhnout symetrie, je přidávat chybějící symetrické prvky.

- Zjistíme, které prvky chybí v relaci. Pro každý prvek $(a, b)$ v relaci $R$, pokud $(b, a)$ není součástí relace, přidáme ho
	1. Přidáme $(2, 1)$, protože $(1, 2)$ je v relaci, ale $(2, 1)$ není.
	2. Přidáme $(3, 1)$, protože $(1, 3)$ je v relaci, ale $(3, 1)$ není.
	3. Přidáme $(3, 2)$, protože $(2, 3)$ je v relaci, ale $(3, 2)$ není.

Po těchto úpravách bude relace symetrická. Nová relace $R'$ bude vypadat takto:

$$R'=\{(1,1),(1,2),(1,3),(2,1),(2,2),(2,3),(3,1),(3,2),(3,3)\}$$

Nyní je relace $R'$ symetrická, protože obsahuje všechny původní prvky $R$ a jejich symetrické páry.
## Část II: Výroková a predikátová logika
1. Zjistěte pravdivostní hodnotu formule 
- $(\neg a ∨ b) \Leftrightarrow (a \Rightarrow b)$
- $\exists x (x\neq z)$ přitom $x \in \{0,1\}$, $z \in \{0,1,2\}$

 Pravdivostní tabulk je jeden ze způsobů zápisu logických funkcí. Taková tabulka obsahuje pouze logické proměnné, které nejčastěji nabývají dvou hodnot **0** a **1** (nepravda a pravda, ne a ano).
- $2^n$, $n$ je počet vstup *(to znamená třeba: a,b,c)*
	- $2^3=8$ tedy 8 řádků

2. Negujte formule
	- $(a \Rightarrow (( a \lor c) \Rightarrow b))$
		$a \land ((a \lor c) \land \neg b)$
	- $\exists x [R(x) \land \neg Z(x)]$
		$\forall x [\neg R(x) \lor Z(x)]$
3. Přeformulujte věty do formulí výrokového počtu a zjistěte, zda je věta pod čarou konsekventem (sémantickým důsledkem) vět nad čarou, zdůvodněte. (4 body)

- Vlakem jezdím jedině tehdy, pokud je náledí.
- Není náledí. 
-
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

**Zjišťujeme konsekvent**
- **Konsekvent laijkcy.** Vezemem ty **předchozíi** řádky kde jsou **dve jedničky**, pokud jsou **dve jedničky v tom řádku** i u vysledné, tak poté **je to konsvekvent**
## Část III: Teorie grafu