## Část I: Množiny, relace, zobrazení
1. Zvolte si tři libovolné čtyřprvkové množiny A,B,C tak, že $A \bigcup B \bigcap C$. Ukažte na nich, zda platí rovnost $A \bigcup (B \bigcap C) = (A \bigcup B) \bigcap (A \bigcup C)$.

$A=\{1,2,3,4\}$
$B=\{5,6,7,8\}$
$C=\{9,10,11,12\}$

**Dosadíme:**
$$A \bigcup (B \bigcap C) = (A \bigcup B) \bigcap (A \bigcup C)$$
$$A \bigcup (∅) = \{1,2,3,4,5,6,7,8\} \bigcap \{1,2,3,4,9,10,11,12\}$$
$$\{1,2,3,4\} \bigcup (∅) = \{1,2,3,4\}$$
$$\{1,2,3,4\} = \{1,2,3,4\}$$
2. Najděte příklad zobrazení $f: ℕ \rightarrow ℕ$ pro které platí, že je bijektivní, ale není surjektivní (na)

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

### Zobrazení (téma otázky 3)
#### Injektivní
- Injektivní zobrazení zajišťuje, že každý prvek ze zdrojové množiny má jedinečný obraz ve cílové množině. Jinými slovy, žádné dva různé prvky ze zdrojové množiny nemají stejný obraz
#### Surjektivní
- Surjektivní zobrazení zajišťuje, že každý prvek ve cílové množině má alespoň jeden předobraz *(duplicity)* ve zdrojové množině. To znamená, že zobrazení pokrývá celou cílovou množinu.
#### Bijektivní zobrazené
- Bijektivní zobrazení je zobrazení, které je zároveň injektivní a surjektivní. Každý prvek ze zdrojové množiny má jedinečný obraz ve cílové množině a zároveň každý prvek ve cílové množině má alespoň jeden předobraz *(duplicitu)* ve zdrojové množině.
#### Inverzní zobrazení

4. Mějme binární relaci $R$ na množině $ℕ$. Zobrazíme-li tuto relaci do kartézských souřadnic, dostaneme všechny body kromě diagonály *(osy 1. kvadrantu)*. Je tato relace ekvivalencí? Zdůvodněte a ukažte na příkladu.
## Část II: Výroková a predikátová logika
## Část III: Teorie graf