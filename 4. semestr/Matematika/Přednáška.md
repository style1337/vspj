Nulový vektor je $0 = (0,0,..0)$

## Operace
Nasobení s realným číselm
- Každým realním číslem vynásobíme každou složku
Součet 
- Musí mít stejný součet souřadnic
- Součiny jsou výsledkem součty souřadnic
Skalární součin
$ab = a_{1}b_{1}+a_{2}b_{2}+...+a_{n}b_{n}$

## Příklad 1
$\vec{u} = (3,1,-1)$
$\vec{v} = (1,2,3)$
$\vec{v_{2}}= (0,-1,-3)$
$\vec{v_{3}}= (2,1,2)$

$\vec{u} = c_{1}v_{1}+c_{2}v_{2}+c_{3}v_{3}$
Dosadíme
$(3,1,-1) = c_{1}(1,2,3)+c_{2}(0,-1,-3)+c_{3}(2,1,2)$
$(3,1,-1)= (c_{1},2c_{2},3c_{3})+(0,-c_{2},-2c_{2})$
Musíme z toho udělat jeden vektor
$(3,1-1,)=(c_{1}+2c_{3},2c_{1}-c_{2}-c_{3},3c_{1}-3c_{2}+2c_{3})$

Rovnice se třemi neznámimi
$3= c_{1}+2c_{3}$
$1= 2c_{1}-c_{2}+c_{3}$
$-1 = 3c_{1}-3c_{2}+2c_{3}$

$c_{1}= 1,c_{2}=2,c_{3}=1$
$\vec{u}=v_{1}+2v_{2}+v_3$
$\vec{v_{1}}=u-2v_{2}-v_{1}$

## Lineární závislost vektorů

## Matice
$\begin{bmatrix}a_{11}a_{12}......&a_{1n}\\a_{21}a_{22}... & a_{2n}\\....&....\\a_{m1}a_{m2}...&a_{mn}\end{bmatrix}$

### Příklad 
$A = \begin{bmatrix}2  &&1 && -2 \\ 3 && 2 && 2\\1 && 0 && 2\end{bmatrix}$
$B = \begin{bmatrix}5&&2&&-2\\3&&0&&4\\1&&1&&3\end{bmatrix}$

Pro první honodtu jsme vzali první řádek A + první sloupec B a takhle jsem jeli dokola pro číslo dvě to byl druhý sloupce B

$A*B = \begin{bmatrix}11&&2&&-6\\23&&8&&8\\7&&4&&4\end{bmatrix}$

Obrácený součin 
- $AB \neq BA$   
$B*A = \begin{bmatrix}\end{bmatrix}$


$D=(1,2,,3,4,5)$
$E = \begin{bmatrix}0\\1\\2\end{bmatrix}$
- $D*E$... není definovaný
- $E*D$... je definovaný
	 $E*D(3,5)$

$ED = \begin{bmatrix}0\\1\\2\end{bmatrix}*(1,2,3,4,5)=\begin{bmatrix}0&&0&&0&&0&&0\\1&&2&&3&&4&&5\\2&&4&&6&&8&&10\end{bmatrix}$


$A = \begin{bmatrix}2&&2&&3\\5&&-2&&2\\2&&0&&2\\1&&3&&1\\-1&&2&&0\end{bmatrix}$~$\begin{bmatrix}1&&3&&1\\5&&-2&&2\\2&&0&&2\\2&&2&&3\\-1&&2&&0\end{bmatrix}=\begin{bmatrix}1&&3&&1\\0&&-17&&-3\\0&&-6&&0\\0&&-4&&1\\0&&5&&1\end{bmatrix}$~$\begin{bmatrix}1&&3&&1\\0&&1&&0\\0&&-17&&-3\\0&&-4&&1\\0&&5&&1\end{bmatrix}$~$\begin{bmatrix}1&&3&&1\\0&&1&&0\\0&&0&&-3\\0&&0&&1\\0&&0&&1\end{bmatrix}=> h(A)=3$
