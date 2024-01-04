 Kvadratická funkce je taková funkce, kterou lze vyjádřit předpisem $f(x) = ax^2+bx+c$, kde $a,b,c$ jsou reálná čísla a dále $a≠0$. 
- Kvadratická funkce je zase vždy popsána **parabolou**.

## Vlastnosti kvadratické funkce
- Definiční obor kvadratické funkce je $R$m množina realných čísel
- Obor hodnot zavisí na konkrétní funkci, ale vždy jde do *(plus nebo minus)* nekonečna
- Kvadratický funkce je dále vždy v polovině intervalu rostoucí a druhé polovině klesajíci
- Pokud je lineární člen roven nule ($b=0$), kvadratický funkce je sudý
- **Kvadratický funkce nikdy není prostá funkce**

## Omezení shora nebo zdola
- Kvadratický funkce je vždy buď omezena shora, nebo zdola
- Závisí to pouze na parametru $a$
- Pokud je totiž parametr $a$ kladný, pak graf funkce "roste nahoru", graf vypadá jak písmeno "U" a graf je tak oemezený zdola
- Příklad je funkce $f(x)=2x^2$

```functionplot
---
title: Shora
xLabel: 
yLabel: 
bounds: [-2,2,-2,2]
disableZoom: false
grid: true
---
f(x)=2x^2
```
- Vidíme, že všechny funkčí hodnoty *(všechny červené body)* jsou nad číslem $-1$, funkce je tak zdola omezená
- Pokud bychom měli funkci $f(x)=-2x^2$

```functionplot
---
title: Zdola
xLabel: 
yLabel: 
bounds: [-3,3,-3,3]
disableZoom: false
grid: true
---
f(x)=-2x^2
```

## Konvexnost a konkávnost
- Konvexnost a konkávnost opět zavisí na parametru $a$
- Kvadratický funkce je **konvexní** pokud má tvar písmene "U"
- Kvadratický funkce je **konkávní** pokud má tvar převráceného písmene "U"
- Paramtr $a$ dále ovlivňuje je i to, jestli bude graf úzký nebo široký.
- Čím více se hodnota blíží nule, tím je graf širší a naopak

## Průsečíky s osou $x$ a $y$
- Musíme si převést funkci na tvar $y = yx^{2}+ bx + c$, což znamená, že y-ovou souřadnici v bodě $x=2$ zjistíme tak, že za všechna $x$ dosadíme dva.
- Když chceme průsečík s osou $x$ tak ve funkci prostě za všechny $y$ dosadíme $0$
- Když chceme průsečík s osou $y$ tak ve funkci prostě za všechny $x$ dosadíme $0$

## Jak vypočítat souřadnice vrcholu
- Nejdůlěžitějším bodem paraboly je **vrchol V** $[v_1;v_2]$
- 