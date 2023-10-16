# Popis
Počet kreditů: **5**
Předmět je povinný a ukončen **Zápočtem a zkouškou**

## B-stromy
### Moje prezentace
#### Základní informace
- **Strom** je široce využívanou datovou strukturou, která prestavuje stromovou strukturu s propojenými uzly
- Uzel stromu  *(anglicky "node")* může
	- obsahovat hodnotu *(popř. tzv. klíč)*
	- obsahovat podmínku
	- reprezentovat strukturu oddělených dat
	- obsahovat vlastní trom

- Uzly jsou navzájem spojeny *"hranami"*
- **Neexistuje osamocený uzel ke kterému by nevedla žádná hrana** *(s výjimkou stromu s pouze jedním uzlem)*
- Pokud jsou hrany orientované, nazývají se uzly připojené k jednomu uzlu jako "potomci uzlu"
	- Nadřazený uzel je potom "rodičovský uzel"
- Uzel může mít pouze **jednoho rodiče ale více potomků**
- Počet všechy potomků nějakého uzlu se nazývá *"stupeň uzlu"*

#### Základní prvky stromu
##### Kořen stromu
- Nejvyšší uzel ve stromu se nazývá *"kořen stromu" (anglicky "root")*
- Kořen stromu je jediným uzlem ve stromu bez rodiče
- V každém stromu se nachází maximálně jeden kořen, takový strom nazýváme *"zakořeněný strom"*
![[img/strom.png]]
##### Vnitřní uzly
- Uzel, který není koncovým uzlem se nazývá *"vnitřní uzel" (anglicky: internal node nebo inner node)*
##### Koncové uzly
- **Koncový uzel** někdé také "list" *(anglicky leaf nebo leaf node)* je takový prvek který nemá žádného potomka
###### Maximalní počet potomků
- Pro B-strom je to definovaná hodnota **n**
##### Podstrom
- Je část stromové datové struktury tvořené jedním uzlem *("kořenem podstromu")* a všemi jeho potomky
- Může se brát jako kompletní strom sám o sobě
 ![[img/podstrom.png]]

#### B-strom
- B-strom řádu **n** je takový strom, který splňuje tyto vlastnosti
- Všechny listy *(uzly které nemají žádne potomky)* jsou na stejné úrovni *(ve stejné hloubce)*
- Všechny vnitřní uzly kromě kořene mají maximálně **n** a minimálněě $[\frac{n}{2}]$ potomků
- Kořen má nejvýše $n$ potomků, spodní hranice není omezena