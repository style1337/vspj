## Funkční závislosti
$R(A,B,C,D)$
$F = {A \to B, BC \to D, D \to BC, C \to A}$

- určit klíč
$A: BCD (B,C,D,A)$, Je redudatní
$B:CD(C,D,B,A)$, Je redudatní
$C: D(D,B,C,A)$, Je redudatní
D je klíč

- spočítat minimální pokrytí
1. Kanonické pokrytí *(na pravé straně jednoduché atr)*
$$D \to BC$$
$D \to B$
$D \to C$

$A: BCD+ (B,C,D,A)$, Je redudatní
$B: CD+ (C,D,A,B)$, Je redudatní
$C: D+ = (D,B,C,A)$, Je redudatní
D je klíč
   
2. Odstranit redudatní atributy z levých stran
   $$BC \to D$$
$BC + = (B,C,D,A)$
$B:C+= (C,A,B,D)$, Je redudatní
$C:B+=(B)$, Není redudatní

3. Odstranit redudatní závilosti
   $$D \to B$$
   $D:B (D,B,C,A)$
   $D+= (D,C,A,B)$, Je redudatní

$$D \to C$$
$D:C(D,B,C,A)$
$D+=(D)$, Není redudatní
$$A \to B$$
$A:B(A,B)$
$A+=(A)$, Není redudatní
$$C \to D$$
$C:D(C,D,A,B)$
$C:(A,B,C)$, Není redudatní
$$C \to A$$
$C:A(C,A,D,B)$
$C+=(C,D)$, Není redudatní

- určit další klíče
$R(D,C,B,A)$
$F = {A \to B, BC \to D, D \to BC, C \to A}$
$D:CBA+=(C,B,A,D)$, Je redudatní
$C:AB+=(A,B)$, Není redudatní
$B:AC+=(A,C,B,D)$, Je redudatní
$A:C+=(C,A,B,D)$, Je redudatní
Klíč je C