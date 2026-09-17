## Kvadratické a bilneární formy, matice forem

> Skalární součin jsme zkoumali ve vektorových prostorech na realnými i komplexními čísly, a můžeme se ptát, jestli by mělo smysl zkoumat podobné zobrazení i ve vektorových prostorech nad obecnými tělesy.

> Dnes si předvedeme, že je to možné, nadefinujeme si analogii skalárního součinu i normy, a převedeme si, jaké tato zobrazení bude mít vlastnosti.

### Bilineární forma
![alt text](image-394.png)
- linearita vůči skalárnímu násobku v 1. i ve 2. složce

![alt text](image-395.png)
- linearita vůči sčítání v 1. i ve 2. složce

**bi**lineární = lineární v 1. i ve 2. složce

#### Symetrická bilineární forma
![alt text](image-396.png)

### Kvadratická forma

![alt text](image-397.png)

Mohli bychom napsat $g(\mathbf v) := f(\mathbf v, \mathbf v)$, kde $f(\mathbf v, \mathbf v)$ je nějaká bilineární forma. Nicméně takhle se to napsalo proto, že těch forem, které odpovídají stejné kvadratické formě může být víc.

Například pro kvadratickou formu 
$g(x_1, x_2) = x_1 x_2$ na 
$\mathbb{R}^2$ můžeme vzít:


$f_1(u, v) = u_1 v_2 \implies f_1(x, x) = x_1 x_2 = g(x)$

$f_2(u, v) = u_2 v_1 \implies f_2(x, x) = x_2 x_1 = g(x)$

$f_3(u, v) = \frac{1}{2}u_1 v_2 + \frac{1}{2}u_2 v_1 \implies f_3(x, x) = x_1 x_2 = g(x)$

To „pokud existuje“ říká, že aby byla funkce 
$g$ kvadratickou formou, musí jít zkonstruovat položením 
$g(v) = f(v, v)$ z alespoň jedné bilineární formy 
$f$.

Zde je definice z Wikipedie:

![alt text](image-404.png)

### Příklady forem

![alt text](image-398.png)

### Matice forem
> Jak bilineární, tak kvadratické formy můžeme popsat pomocí matic, a to v případě, že máme vektorový prostor konečné dimenze a v něm máme dánu nějakou bázi.
> #### Matice bilineární formy
> ![alt text](image-399.png)

#### Matice kvadratické formy
> Jedné kvadratické formě $g$ může odpovídat více bilineárních forem $f$. Proto, aby byla matice kvadratické formy **jednoznačně** dána, bereme tu matici bilineární formy, která je symetrická.

> Ne vždy musí matice kvadratické formy existovat, protože ne vždy existuje symetrická bilineární forma, jak si záhy ukážeme.

![alt text](image-400.png)

![alt text](image-401.png)
- převod mezi těmito oběma tvary (analytický tvar a matice) bude vysvětlen podrobněji později v tomto videu

> Ne vždy se nám musí podařit matici kvadratické formy najít
>
> ![](image-402.png)
- jinde než na $\mathbb{Z}_2$, tedy na tělese s charakteristikou jinou než $2$ bude vždy existovat od každé bilineární formy její symetrická verze - viz dále: 

> Záhy si ukážeme, jak z předpisu pro kvadratickou formu můžeme sestavit symetrickou matici bilineární formy, a zároveň nám to dá odpověď na otázku, kdy matice kvadratické formy neexistuje.
>
> Nejprve si všimneme, že prvky matice $A$ jsou dány nejenom bilineární formou $f$, tak, že do ní dosadíme $i$-tý a $j$-tý vektor dané báze, ale také, že ji lze spočítat přímo z kvadratické formy tímto výrazem:
>
> ![alt text](image-403.png)

v důkazu:
- předpokládáme, že $g$ a $f$ existuje (což můžeme dokud není řeč o maticích, tak není na $f$ podmínka, aby byla symetrická => $f$ existuje vždy => $g$ existuje vždy) 
- $g$ existuje $\iff g(\mathbf v) = f(\mathbf v, \mathbf v)$ 
- linarita bilin. normy v 1. a 2. složce
- v posledním kroku máme na pravé straně $f(\mathbf b_i, \mathbf b_j) + f(\mathbf b_j, \mathbf b_i)$
	- > u kvadratické formy hledáme symetrickou matici, tzn, že hodnota formy $f$ má být stejná, ať už ty vektory dosadíme v jakémkoli pořadí
- tak tedy dostáváme $2f(\mathbf b_i, \mathbf b_j)$
- a pak obě strany rovnice vydělíme $2$
	- > nad tělesy, které mají charakteristiku $2$, dělit $2$ nelze, a proto v těchto případech nemusí vždy matice kvadratické formy existovat

		> v tělesech ostatních charakteristik má číslo $2$ vždy svůj inverzní prvek (zde $2$ bereme tak, že sečteme dvakrát neutrální prvek vzhledem k násobení)
		>
		> **proto v tělesech, které nemají charakteristiku 2, je vždy matice kvadratické formy dána jednoznačně** (a tedy definována, že)

#### Co si z toho odnést

Vždy, kdy v tělese existuje číslo $2$, můžeme vytvořit matici symetrické bilineární formy.
- a z té pak - viz (forward ref) analytické vyjádření - vytvořit polynom ("funkční předpis")

![alt text](image-404.png)
- že jo nějaká kvadratická forma k bilineární formě existuje vždy (není zde žádný požadavek na symetrii, jedné kvadratické formě může odpovídat víc bilineárních forem)
- a pak pomocí vzorce $a_{ij} = \frac 1 2 (g(\mathbf b_i + \mathbf b_j) - g(\mathbf b_i) - g(\mathbf b_j))$ si vytvořit symetrickou matici bilineární formy
	- a kdybychom chtěli polynom téhle bilin. formy, tak spočteme analytické vyjádření

Takže vlastně takhle trochu oklikou umíme "symetrizovat" bilineární formu.
- a z ní pak sestrojit i matici kvadratické formy ( protože že jo symetrická matice bilineární formy a matice kvadratické formy se liší jenom vstupy - jestli tam pošleme 2 stejné vektory nebo různé)

Proto se matice kvadratické formy definuje tak, že je to "ta symetrická", protože prakticky vždy jde sestrojit, a neztratíme tím žádné možnosti.

(kromě toho edge case, kdy bychom něměli číslo 2, viz $\mathbb{Z}_2$ - pak bychom se asi museli smířit s tím co máme, a netrvat na symetrii - stejně by symetrická a nesymetrická verze téže formy po dosazení vstupních vektorů měla dát stejné číslo)

Alternativně, **máme-li už nějakou nesymetrickou matici formy A**, tak z ní můžeme udělat symetrickou matici B takto: 

$$B = \frac 1 2 (A + A^T)$$

$B$ už je v pohodě matice kvadratické formy, protože je symetrická.

Př. z analytického vyjádření kvadratické formy $g(\mathbf v) = v_1^2 + v_1 v_2 + 3 v_2^2$ (nad $\mathbb{Z}_5$) dostaneme $A = \begin{pmatrix} 1 & 1 \\ 0 & 3 \end{pmatrix}$ 

<details> <summary> Viz ukázka výše s barevnými tečkami </summary>

![](image-401.png)

</details>

<details>

<summary>
Zkouška výpočtené A
</summary>

$$\begin{pmatrix} v_1 & v_2 \end{pmatrix} \begin{pmatrix} 1 & 3 \\ 3 & 3 \end{pmatrix} \begin{pmatrix} v_1 \\ v_2 \end{pmatrix}$$

$$\begin{pmatrix} v_1 & v_2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 3 \end{pmatrix} \begin{pmatrix} v_1 \\ v_2 \end{pmatrix} = \begin{pmatrix} v_1 & v_1 + 3v_2 \end{pmatrix} \begin{pmatrix} v_1 \\ v_2 \end{pmatrix} = v_1^2 + (v_1 + 3v_2)v_2 = v_1^2 + v_1v_2 + 3v_2^2$$
- fungovalo by to i s $\begin{pmatrix} 1 & 0 \\ 1 & 3 \end{pmatrix}$, tj. nemusíme si pamatovat, které souřadnice (z dolních indexů) je která, nebo tak něco.

</details>
<br>

Pak $A$ symetrizujeme:

protože jsme nad $\mathbb{Z}_5$, tak $\frac 1 2$ bude $1 \cdot 2^{-1}$ (inverzní prvek k $2$), což v $\mathbb{Z}_5$ je $3$.

$3 \left(\ \begin{pmatrix} 1 & 1 \\ 0 & 3 \end{pmatrix} + \begin{pmatrix} 1 & 0 \\ 1 & 3 \end{pmatrix} \ \right) = \begin{pmatrix} 1 & 3 \\ 3 & 3 \end{pmatrix}$

To odpovídá výsledku ze slidu.
______________

##### Proč teda chceme symetrii

Spousta nástrojů v lineární algebře pracuje s symetrickými maticemi.
____

> Máme-li ať už bilineární nebo kvadratickou formu popsánu pomocí její matice, můžeme hodnotu této formy vyhodnotit pomocí maticového součinu.
>
> ![alt text](image-405.png)

Důkaz:

$[\mathbf u]_B = (c_1, \dots, c_n)$

$[\mathbf v]_B = (d_1, \dots, d_n)$

![alt text](image-406.png)
- vyjádříme ty vektory pomocí lineární kombinace vektorů báze $B$
- ty koeficienty odpovídají prvkům vektorů souřadnic (viz definice vektoru souřadnic)
	- $[\mathbf u]_B = (c_1, \dots, c_n)$
	- $[\mathbf v]_B = (d_1, \dots, d_n)$

![alt text](image-407.png)
- dosadíme, díky linearitě vytkneme (to s dvojitou sumou funguje stejně jako u skal. součinu - kde jsem to rozebíral podrobněji - akorát tady už nemáme žádné komplexní sdružení)
- odpovídá to $[\mathbf u]_B^T A [\mathbf v]_B$, protože
	- $[\mathbf u]_B = (c_1, \dots, c_n)$
	- $[\mathbf v]_B = (d_1, \dots, d_n)$
	- $a_{ij} = f(\mathbf b_i, \mathbf b_j)$

### Jak se mění matice formy, když měníme bázi
![alt text](image-408.png)
- pozor na tu transpozici
	- kde vznikne vidět z důkazu:

![alt text](image-409.png)

### Analytické vyjádření bilineární formy
> Ať už bilineární nebo kvadratické formy bývají často popisovýny pomocí polynomům tak, jak jsme je používali v našich ukázkách.
>
> Tyto popisy si zaslouží vlastní název:
>
> ![alt text](image-410.png)
- co je **homogenní polynom**
	- polynom, který má v každém ze svých členů stejný součet (tomuto součtu, ač od různých proměnných, říkáme stejně stupeň) mocnin u proměnných - př. $x^3 + 2xy^2 + 3y^3$ je homogenní (všechny členy stupeň 3)

- $\displaystyle\sum_{i=1}^n \sum_{j=1}^n a_{ij} u_i v_j$ vzniklo z maticového součinu, že jo:
	- $\displaystyle\sum_{i=1}^n \sum_{j=1}^n u_i \cdot a_{ij} \cdot v_j$, což právě odpovídá součinu $\mathbf u^T A \mathbf v$

![alt text](image-411.png)

![alt text](image-412.png)
- na což jsme právě přišli pomocí

$$
\begin{pmatrix}
u_1 & u_2
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
4 & 3
\end{pmatrix}
\begin{pmatrix}
v_1 \\
v_2
\end{pmatrix}
$$

> Vidíme, že reprezentace bilineárních a kvadratických forem podstatně závisí na volbě báze. 
>
> Přiště si předvedeme, že některé báze mohou být pro tento účel vhodnější.

## Diagonalizace matic forem, zákon setrvačnosti

> V dnešní lekci si předvedeme, jakmile lze v tělese dělit dvěma, lze také diagonalizovat matice forem. 
>
> Půjde o jinou diagonalizaci než je diagonalizace matic lineárních zobrazení. Přesto však důkaz bude velice podobný diagonalizaci hermitovských matic.

### Kvadratické formy nad tělesy charakteristiky 2
> U těles charakteristiky 2 je jednoduché najít diagonální matici kvadratické formy. Protože buďto vůbec neexistuje, jako např. u formy $g(\mathbf v) = v_1 v_2$. 
>
> A nebo v případě, že nějaká symetrická matic dané kvadratické formy existuje, potom zjistíme, že pokud počítáme analytické vyjádření této formy, tak se všechny smíšené členy navzájem odečtou:
>
> ![alt text](image-418.png)

př. pro 2 složkové vektory $\mathbf u = (u_1, u_2)^T$ a $\mathbf v = (v_1, v_2)^T$ by bilineární forma nad $\mathbb{Z}_2$ (její analytické vyjádření) vypadala obecně takto:

$f(\mathbf u, \mathbf v) = a u_1 v_1 + b u_1 v_2 + c u_2 v_1 + d u_2 v_2$

Pro symetrickou bilin. formu platí platí, že $b = c \land u_1 v_2 = u_2 v_1$

$f(\mathbf u, \mathbf v) = a u_1 v_1 + b(u_1 v_2 + u_2 v_1) + d u_2 v_2$

$u_1 v_2 + u_2 v_1 = 2 u_1 v_2 = 0 u_1 v_2$

a $g(\mathbf v) = f(\mathbf v, \mathbf v)$ že jo

**Ukázka symetrické matice nad tělesem s char. 2**
![alt text](image-419.png)
- jelikož analytické vyjádření rovno $\sum_{i=1}^n a_{ii}  v^2_i$, zde $v_1^2$, tak i matice napravo má stejné analytické vyjádření, a je diagonální

![alt text](image-420.png)

> U ostatních těles dá diagonalizace forem trochu více práce.
### Diagonalizace matic forem nad ostatními tělesy a polární báze (Věta o diagonalizovatelnosti matic forem)
![alt text](image-421.png)
![alt text](image-422.png)
- $R$ je matice přechodu od nové báze k původní bázi, $[id]_{B, E}$
- $R^T A R$ je diagonální matice, vyjádření téže formy vůči nové polární bázi

- že jo viz:
	- ![alt text](image-408.png)
	- ![alt text](image-409.png)

- matice $R^T$ tak není matice přechodu v tradičním smyslu, protože je to $[id]_{B,E}^T$
	- nepřevádí tak nikam vektory v sloupcích, ale v řádcích
	- že jo na rozdíl od lineárních zobrazení, kdy vpravo od matice lin. zobrazení byl vstup, a vlevo od ní byl výstup, máme zde matici formy, kde vpravo je vstup, i vlevo je vstup, a výstup je vyhodnocení výrazu, tedy číslo.
		- btw that means we can't really "pipe" it za sebou, jak jsme to dělali u lin. zobrazení
	- takže jako důsledek, matice $R^T$ slouží na převod **levého** (který je řádkový, a vlevo od $R^T$, proto ta transpozice) vstupního vektoru z nové polární báze do původní báze

- na tohle jednou Fiala udělal forward ref v prezentaci `412-podobnost.pdf` (Podobné matice, diagonalizace):

	![alt text](image-423.png)

	- takže tomuhle našemu vztahu $D = R^T A R$, kde $A$ je matice formy, a $D$ je diagonální matice (=matice té formy vyjádřená k polární bázi) dá říkat kongruence matic

		- Dvě čtvercové matice $A, D \in T^{n \times n}$ jsou **kongruentní**, pokud existuje regulární matice $R$ taková, že $D = R^T A R$.

		- Zatímco relace **podobnosti** ($D = R^{-1} A R$) odpovídá hledání báze, kde je **matice lineárního zobrazení $A$ diagonální**
		-  Tak relace **kongruence** ($D = R^T A R$) odpovídá hledání polární báze, kde je **matice kvadratické (či symetrické bilineární) formy $A$ diagonální.**

![alt text](image-424.png)

> Ještě si všimneme, že u realných matic věta platí již díky diagonalizaci symetrických matic lineárních zobrazení pomocí ortogonálních matic
>
> ![alt text](image-425.png)

- pokud teda na chvilku $A$ = matici formy (že jo navržena na 2 vstupy, proto $R^TAR$) na chvilku "dezinterpetujeme" jako matici lineárního zobrazení (že jo navržena na 1 vstup, proto $R^{-1}AR$)

Pro obecné tělesa to, že tu kongruenci = diagonalizaci matice formy jde udělat,  budeme ještě dokazovat:

![alt text](image-413.png)
#### Důkaz:

Nejdřív uvedu hlavní myšlenku, pak na obrázcích podrobněji.

Indukcí, s tím, že indukční předpoklad vyslovíme pro $n-1$.

Aby se nám matice nepletly, tak ke každé připíšeme její řád do dolního indexu.

**Indukční předpoklad:** Pro jakoukoli symetrickou matici $A_{n-1} \in T^{(n -1) \times (n-1)}$ s $\text{char } T \neq 2$ existuje regulární matice $R_{n-1}$ taková, že $R_{n-1}^T A_{n-1} R_{n-1}$ je diagonální.

**Indukční krok**: Chceme s využitím indukčního předpokladu dokázat, že věta platí pro řád $n$, tedy že platí: Pro libovolnou symetrickou $A_n \in T^{n \times n}$, $\text{char } T \neq 2$ existuje regulární $R_n$ taková, že $R_n^T A_n R_n$ je diagonální.

Pro to potřebujeme nějak vyrobit
- $R_n$ tak, aby byla regulární a diagonální
- $A_n$, tak aby byla diagonální

Aby ten součin $R_n^T A_n R_n$ vyšel diagonální.

V průběhu ukážeme, že umíme vyjádřit výraz obsahující $A_n$ pomocí výrazu, který obsahuje $A_{n-1}$,

konkrétně půjde o ${\color{blue}P_n^T A_n P_n} = \def\arraystretch{1.2}\begin{array}{|c|c|}
\hline
\color{red}{a_{11}} & \color{blue}{\mathbf{0}^{\mathsf{T}}} \\
\hline
\color{blue}{\mathbf{0}} & \color{blue}{\mathbf{A}_{n-1}} \\
\hline
\end{array}$

Bez těch $P_n^T$ a $P_n$ to neumíme, to jsou matice elementárních úprav.

To nám vynucuje volbu regulární matice $R_n$

Která právě proto bude $R_n = P_n \cdot  \def\arraystretch{1.2}\begin{array}{|c|c|}
\hline
 1 & {\mathbf{0}^{\mathsf{T}}} \\
\hline
{\mathbf{0}} & {\mathbf{R}_{n-1}} \\
\hline
\end{array}$

Protože pak totiž po dosazení a transponování

$$R_n^T A_n R_n = \left(P_n \cdot  \def\arraystretch{1.2}\begin{array}{|c|c|}
\hline
 1 & {\mathbf{0}^{\mathsf{T}}} \\
\hline
{\mathbf{0}} & {\mathbf{R}_{n-1}} \\
\hline
\end{array} \ \right)^T \cdot A_n \cdot \left( P_n \cdot  \begin{array}{|c|c|}
\hline
 1 & {\mathbf{0}^{\mathsf{T}}} \\
\hline
{\mathbf{0}} & {\mathbf{R}_{n-1}} \\
\hline
\end{array} \ \right)$$

$$= \begin{array}{|c|c|}
\hline
 1 & {\mathbf{0}^{\mathsf{T}}} \\
\hline
{\mathbf{0}} & \mathbf{R}_{n-1}^T \\
\hline
\end{array} \cdot P_n^T A_n P_n \cdot\begin{array}{|c|c|}
\hline
 1 & {\mathbf{0}^{\mathsf{T}}} \\
\hline
{\mathbf{0}} & {\mathbf{R}_{n-1}} \\
\hline
\end{array}$$

dostáváme uprostřed $P_n^T A_n P_n$, což můžeme nahradit kýženým výrazem, který obsahuje $A_{n-1}$. Celý součin je tak výrazem, který obsahuje všechny tři matice z indukčního předpokladu:

$$= \begin{array}{|c|c|}
\hline
 1 & {\mathbf{0}^{\mathsf{T}}} \\
\hline
{\mathbf{0}} & \mathbf{R}_{n-1}^T \\
\hline
\end{array} \cdot {
\begin{array}{|c|c|}
\hline
\color{red}{a_{11}} & \color{blue}{\mathbf{0}^{\mathsf{T}}} \\
\hline
\color{blue}{\mathbf{0}} & \color{blue}{\mathbf{A}_{n-1}} \\
\hline
\end{array}
} \cdot\begin{array}{|c|c|}
\hline
 1 & {\mathbf{0}^{\mathsf{T}}} \\
\hline
{\mathbf{0}} & {\mathbf{R}_{n-1}} \\
\hline
\end{array}$$

Teď vyhodnotíme blokový součin, a dostaneme:

$${
\def\arraystretch{1.2}
\begin{array}{|c|c|}
\hline
\color{red}{a_{11}} & \color{blue}{\mathbf{0}^{\mathsf{T}}} \\
\hline
\color{blue}{\mathbf{0}} & \color{blue}{\mathbf{R}_{n-1}^T \mathbf{A}_{n-1}} \mathbf{R}_{n-1}\\
\hline
\end{array}
}$$

To je zajímavé proto, že můžeme snadno dokázat, že tento výraz je diagonální:
- $\mathbf{R}_{n-1}^T \mathbf{A}_{n-1} \mathbf{R}_{n-1}$ je diagonální z indukčního předpokladu
	- ten blok je umístěn tak, že je diagonální i celá bloková matice, protože zbytek 1. sloupce a zbytek 1. řádku tvoří nuly


![alt text](image-414.png)

> Pokud je prvek v levém horním rohu $\neq 0$, můžeme s jeho pomocí řádkovými úpravami zeliminovat zbytek 1. sloupce (matice řádkových úprav $P_n^T$), a potom stejnými sloupcovými úpravami zeliminovat zbytek 1. řádku (matice sloupcových úprav $P_n$).
>
> ![alt text](image-415.png)

- matice, kterou si označíme $A_{n-1}$ je symetrická protože je rozdílem 2 symetrických matic:
	- $B$ je symetrická - jako podmatice symetrické $A_n$
	- Výraz $\mathbf{b}\mathbf{b}^T$ (vnější součin) je vždy symetrická matice
		- $(\mathbf{b}\mathbf{b}^T)^T = (\mathbf{b}^T)^T \mathbf{b}^T = \mathbf{b}\mathbf{b}^T$

A na symetrickou matici řádu $n-1$ už můžeme aplikovat indukční předpoklad.

> Dle indukčního přepokladu pro symetrickou matici  $A_{n-1}$ věta platí, tj. bude pro ni existovat regulární matice $R_{n-1}$. Tu doplníme na matici řádu $n$:
>
> ![alt text](image-416.png)

- proč $R_n$ určujeme zrovna takto jsem popsal výše v úvodu


Tato $R_n$ je regulární, protože je součinem regulárních matic:
- $P_n$ je regulární (že jo $1$ na celé diagonále)
- $\def\arraystretch{1.2}\begin{array}{|c|c|}
\hline
 1 & {\mathbf{0}^{\mathsf{T}}} \\
\hline
{\mathbf{0}} & {\mathbf{R}_{n-1}} \\
\hline
\end{array}$ je regulární (z indukčního předpokladu, protože $R_{n-1}$ je regulární)

> Lze ověřit, že součin $R_n^T A_n R_n$ nám dává diagonální matici
>
> ![alt text](image-417.png)

- protože  $R^T_{n-1}A_{n-1}R_{n-1}$ je diagonální z indukčního předpokladu

##### Ukázka použití věty k diagonalizaci matici 3x3 pomocí algoritmu z důkazu

![alt text](image-426.png)

> Zbývá ošetřit případy kdy $a_{11} = 0$. 

(Kdy tedy musíme matici nějak upravit, abychom se dostali k nenulovému $a_{11}$, abychom mohli použit ten důkaz.)

> Nejprve se zaměříme na situaci, kdy $a_{11} = 0$ a vektor $\mathbf b$ je nenulový
>
> ![alt text](image-427.png)

Zde přidám obrázek z videa (v prezentaci už nebyl), který to dobře ilustruje:

> ![alt text](image-429.png)
> k 1. řádku přičteme $i$-tý, a k 1. sloupci přičteme $i$-tý (což právě je to $E^T A E$)

- **můj podrobnější obrázek - s bloky co se změní** (na předchozím obrázku to není jenom nakresleno - výsledek bude symetrická matice), takto:

	$A = \begin{pmatrix} 
0 & a_{1i} & \mathbf{c}^T \\ \hline 
a_{i1} & a_{ii} & \mathbf{d}^T \\ \hline 
\mathbf{c} & \mathbf{d} & C 
\end{pmatrix}$

	$A' = \begin{pmatrix} 
a_{i1} + (a_{1i} + a_{ii}) & a_{1i} + a_{ii} & \mathbf{c}^T + \mathbf{d}^T \\ \hline 
a_{i1} + a_{ii} & a_{ii} & \mathbf{d}^T \\ \hline 
\mathbf{c} + \mathbf{d} & \mathbf{d} & C 
\end{pmatrix}$

	- $a_{ii} = 0$ 
	- $a_{i1} + a_{1i}= 2a_{i1}$, protože matice symetrická

<details>

<summary>
Konkrétně ty součiny
</summary>

Matici $A$ řádu $n$ rozdělíme na bloky odpovídající 1. složce, 
$i$-té složce a zbývajícím $n-2$ složkám:

$$A = \begin{pmatrix} 
0 & a_{1i} & \mathbf{c}^T \\ \hline 
a_{i1} & a_{ii} & \mathbf{d}^T \\ \hline 
\mathbf{c} & \mathbf{d} & C 
\end{pmatrix}$$
Matice $E$, která odpovídá přičtení $i$-tého sloupce k 1. sloupci, a její transpozice $E^T$ mají blokový tvar:

$$E = \begin{pmatrix} 
1 & 0 & \mathbf{0}^T \\ \hline 
1 & 1 & \mathbf{0}^T \\ \hline 
\mathbf{0} & \mathbf{0} & I_{n-2} 
\end{pmatrix}, \qquad 
E^T = \begin{pmatrix} 
1 & 1 & \mathbf{0}^T \\ \hline 
0 & 1 & \mathbf{0}^T \\ \hline 
\mathbf{0} & \mathbf{0} & I_{n-2} 
\end{pmatrix}$$

**1. Krok: Řádková úprava $E^T A$ (přičtení $i$-tého řádku k 1. řádku)**

$E^T A = \begin{pmatrix} 
1 & 1 & \mathbf{0}^T \\ \hline aA
0 & 1 & \mathbf{0}^T \\ \hline 
\mathbf{0} & \mathbf{0} & I_{n-2} 
\end{pmatrix} 
\begin{pmatrix} 
0 & a_{1i} & \mathbf{c}^T \\ \hline 
a_{i1} & a_{ii} & \mathbf{d}^T \\ \hline 
\mathbf{c} & \mathbf{d} & C 
\end{pmatrix} 
= \begin{pmatrix} 
a_{i1} & a_{1i} + a_{ii} & \mathbf{c}^T + \mathbf{d}^T \\ \hline 
a_{i1} & a_{ii} & \mathbf{d}^T \\ \hline 
\mathbf{c} & \mathbf{d} & C 
\end{pmatrix}$

**2. Krok: Sloupcová úprava $(E^T A) E$ (přičtení $i$-tého sloupce k 1. sloupci)**

$$A' = (E^T A) E = \begin{pmatrix} 
a_{i1} & a_{1i} + a_{ii} & \mathbf{c}^T + \mathbf{d}^T \\ \hline 
a_{i1} & a_{ii} & \mathbf{d}^T \\ \hline 
\mathbf{c} & \mathbf{d} & C 
\end{pmatrix} 
\begin{pmatrix} 
1 & 0 & \mathbf{0}^T \\ \hline 
1 & 1 & \mathbf{0}^T \\ \hline 
\mathbf{0} & \mathbf{0} & I_{n-2} 
\end{pmatrix}$$

$$A' = \begin{pmatrix} 
a_{i1} + (a_{1i} + a_{ii}) & a_{1i} + a_{ii} & \mathbf{c}^T + \mathbf{d}^T \\ \hline 
a_{i1} + a_{ii} & a_{ii} & \mathbf{d}^T \\ \hline 
\mathbf{c} + \mathbf{d} & \mathbf{d} & C 
\end{pmatrix}$$

</details>

> Dostáváme symetrickou matici, která má v levém horním rohu nenulové číslo, a můžeme ji tedy upravit stejným způsobem jako v předchozím případě, kdy $a_{ii} \neq 0$

> Pokud by $a_{11} = 0$ a  $a_{ii} \neq 0$, protom je situace o trochu jednodušší, protože stačí pouze prohodit 1. řádek s $i$-tým a také 1. slopec s $i$-tým.
>
> ![alt text](image-430.png)
- což bude jiná matice $E$, protože tamto bylo přičtení, a zde máme jenom prohození.

$A = \begin{pmatrix} 
0 & a_{1i} & \mathbf{c}^T \\ \hline 
a_{i1} & a_{ii} & \mathbf{d}^T \\ \hline 
\mathbf{c} & \mathbf{d} & C 
\end{pmatrix}$

$E = E^T = \begin{pmatrix} 
0 & 1 & \mathbf{0}^T \\ \hline 
1 & 0 & \mathbf{0}^T \\ \hline 
\mathbf{0} & \mathbf{0} & I_{n-2} 
\end{pmatrix}$

$E^T A = \begin{pmatrix} 
0 & 1 & \mathbf{0}^T \\ \hline 
1 & 0 & \mathbf{0}^T \\ \hline 
\mathbf{0} & \mathbf{0} & I_{n-2} 
\end{pmatrix} 
\begin{pmatrix} 
0 & a_{1i} & \mathbf{c}^T \\ \hline 
a_{i1} & a_{ii} & \mathbf{d}^T \\ \hline 
\mathbf{c} & \mathbf{d} & C 
\end{pmatrix} 
= \begin{pmatrix} 
a_{i1} & a_{ii} & \mathbf{d}^T \\ \hline 
0 & a_{1i} & \mathbf{c}^T \\ \hline 
\mathbf{c} & \mathbf{d} & C 
\end{pmatrix}$

$$A' = (E^T A) E = \begin{pmatrix} 
a_{i1} & a_{ii} & \mathbf{d}^T \\ \hline 
0 & a_{1i} & \mathbf{c}^T \\ \hline 
\mathbf{c} & \mathbf{d} & C 
\end{pmatrix} 
\begin{pmatrix} 
0 & 1 & \mathbf{0}^T \\ \hline 
1 & 0 & \mathbf{0}^T \\ \hline 
\mathbf{0} & \mathbf{0} & I_{n-2} 
\end{pmatrix}$$

$$A' = \begin{pmatrix} 
a_{ii} & a_{i1} & \mathbf{d}^T \\ \hline 
a_{1i} & 0 & \mathbf{c}^T \\ \hline 
\mathbf{d} & \mathbf{c} & C 
\end{pmatrix}$$

> Zbývá ošetřit situaci, kdy celý 1. řádek i sloupec jsou nulové
>
> ![alt text](image-431.png)

- tj. nemusíme nic řešit, prostě zahodíme 1. řádek i sloupec, protože už jsou vynulované, což je stav, ke kterému jsme se chtěli v ostatních předmětech dostat.

### Metody diagonalizace matic forem
> Ve výsledku jsem získali 2 metody, jakým způsobem se dají matice forem diagonalizovat
>
> ![alt text](image-432.png)
> - tak, jak jsme se naučili diagonalizovat matice lineárních zobrazení
![alt text](image-413.png)
![alt text](image-425.png)

- že jo samotným těm maticím "je jedno", jaký význam jim přidělíme (pro tento kontext tu matici formy "dezinterpretujeme" jako jinou matici, matici nějakého lineárního zobrazení), víme, že máme tu větu, že tedy ten součin 3 matic nalézt půjde = diagonalizovat půjdou, a můžeme tedy hledat $D = R^{-1}AR$, najít vlastní čísla, která budeme dávat do $D$, a spočíst ty matice přechodu = tam dáme vlastní vektory (viz dříve)
	- případně tedy díky té větě jenom nalézt tu $R$ a pak místo inverze spočítat prostou transpozici

> pokud naše symetrická matice není **realná**, nebo jen nechceme využívat vlastních čísel:
>
> ![alt text](image-433.png)

- což jsme právě dělali v tom důkazu = použijeme důkaz jako algoritmus
- *současně* zde ale stále znamená jedno po druhém, tj. nejdřív provedeme řádkovou operaci, poté provedeme odpovídající sloupcovou operaci, viz další pozorování:

![alt text](image-434.png)

> Jakmile se nám podaří matici $A$ převést eliminací na dolní trojúhelníkovou matici, tak vzhledem k tomu, že po celou dobu udržujeme matici symetrickou, tak výsledná matice bude nejenom dolní trojúhelníková, ale ve skutečnosti i diagonální.
>
> ![alt text](image-435.png)

#### Ukázka diagonalizace symetrické matice pomocí Gaussovy eleminace
![alt text](image-436.png)

$$R = [id]_{B,E} = \begin{pmatrix}
\vert &  & \vert \\
[\text{id}(\mathbf{b}_1)]_E & \dots & [\text{id}(\mathbf{b}_n)]_E \\
\vert & &\vert
\end{pmatrix}

= \begin{pmatrix}
\vert &  & \vert \\
\mathbf{b}_1 & \dots & \mathbf{b}_n \\
\vert & &\vert
\end{pmatrix}

$$

- vpravo máme za začátku matici identity, a pak, jak postupně upravujeme řádkovými úpravami matici nalevo, tak se do té matice napravo ty úpravy také propisují, a je tak na konci "seznamem" všech těch úprav, právě tou maticí řádkových úprav $R^T$

- viz vysvětlení u nadpisu "Diagonalizace matic forem nad ostatními tělesy"

	- ![alt text](image-413.png)
	- $D = R^T A R$ je diagonální matice, vyjádření téže formy vůči nové bázi, kterou nazveme polární
		- proto $R$ musí být matice přechodu od polární báze k původní bázi pro pravý vstupní vektor
		- a $R^T$ musí být matice přechodu (ač teda transponovaná, protože levý vstup vstupuje jako řádek) od polární báze k původní bázi pro levý vstupní vektor
	- kde ta transpozice se odkazuje na předchozí pozorování:
	- ![alt text](image-408.png)
	- ![alt text](image-409.png)

- nebo další pohled na věc, $R^T$ jsou úpravy, které z $A$ udělaly $D$, která je od polární báze $B$ k $B$, a $R$ je pak $[id]_{B,E}$

> Nyní přejdeme ještě dále, a předvedeme si, že v případě realných čísel můžeme získat matici, která kromě nul bude už obsahovat pouze $1$ a $-1$.

### Sylvestrův zákon setrvačnosti — o diagonalizaci kvadratických forem
![alt text](image-437.png)
#### Signatura
![alt text](image-437.2.png)

- signaturu matice formy můžeme určit tak, že pro ni najdeme diagonální matici (=diagonalizujeme ji), a pak s využitím Sylvestrova zákona setrvačnosti, víme, že bude existovat i matice, kde na diagonále budou jenom $1$, $-1$ a $0$. Tedy vydělíme nenulové prvky na diagonále, aby byly $1$, $-1$ (znaménka ponecháme)

	- dá se tedy říct: 
		- Počet kladných vlastních čísel: $p = 1$
		- Počet záporných vlastních čísel: $q = 1$
		-Počet nulových vlastních čísel: $r = 0$

![alt text](image-438.png)
> U forem na $\reals^2$ ve skutečnosti můžeme rozebrat všechny možné případy, protože je jen konečně mnoho signatur (že jo, počtů 1, -1, 0 na hlavní diagonále, kde můžou být celkově 2 prvky).

![alt text](image-439.png)
- ten "pringle" je sedlová plocha

#### Důkaz Sylvestrova zákona setrvačnosti
> Důkaz rozdělíme na 2 části:
> 1. Ukážeme, že nějaká taková vhodná báze existuje
> 2. Ukážeme jednoznačnost počtu $1, -1, 0$

![alt text](image-440.png)
1. **Existence vhodné báze**

	Realné symetrické matice lze diagonalizovat pomocí ortogonálních matic

	(afaik analogie s tím, jak hermitovské matice lze diagonalizovat pomocí unitárních matic)

	![alt text](image-441.png)
	> - pomocnou matici $D'$ si nyní rozložíme jako součin $3$ diagonálních matic, přičemž $D$ bude obsahovat znaménka prvků, které jsou v $D'$ na diagonále.

	> - naším cílem je určit matici $S$ tak, aby byla regulární, tzn. aby všechny prvky na diagonále $S$ byly nenulové.
	>	- s těmi odmocninami tam ve výsledku součinu vznikne $|d'_{ii}|$, a $d_{ii}$ tam přidá znaménko, čímž vznikne původní prvek $d'_{ii}$
	>		- že jo $\sqrt{d'_{ii}} \sqrt{d'_{ii}} = \sqrt{(d'_{ii})^2} =  |d'_{ii}|$
	>		- $\sqrt{-d'_{ii}} \sqrt{-d'_{ii}} = \sqrt{(d'_{ii})^2} =  |d'_{ii}|$

	![alt text](image-442.png)
	- $SR$ regulární protože:
		- $S$ regulární, tak jsme ji zkonstruovali
		- $R$ je regulární z věty, že realné symetrické matice lze vždy diagonalizovat
	- $A = (SR)^T DSR$
		- vzniklo dosazením $D' = S^T DS$ do $A = R^T D' R$:
			1.  $A = R^T D' R$
			2. $A = R^T S^T DS R$
			3. $R^T S^T = (SR)^T$

	> Nyní zbývá pomocí součinu matic $S$ a $R$ převést danou bázi $B$ na hledanou vhodnou bázi $C$. Za tím účelem nejprve součin $SR$ invertujeme, a potom tento součin vezmeme jako matici přechodu $[id]_{C,B}$
	>
	> ![alt text](image-443.png)
	- asi spíš ověříme že ta rovnost vyjde, a tím si potvrdíme, že ten součin vyjde, idk jestli za tou volbou je nějaký intuitivní důvod:
	> = Nyní už můžeme snadno ověřit, že když matici $A$ vynásobíme zleva  $[id]^T_{C,B}$ a zprava $[id]_{C,B}$, jinými slovy vyhodnotíme  $((SR)^{-1})^T (SR)^T DSR(SR)^{-1}$, dostáváme přesně diagonální matici $D$, tak, jak je uvedeno ve znění věty
	- v úpravě výrazu $((SR)^{-1})^T (SR)^T DSR(SR)^{-1}$ použijeme:
		- $((SR)^{-1})^T = ((SR)^T)^{-1}$
		- $((SR)^T)^{-1} (SR)^T = I$
		- $SR(SR)^{-1} = I$

	![alt text](image-444.png)
	- tu ekvivalenci jsme odvodili pomocí toho, že $[id]_{B,C} = [id]_{C,B}^{-1}$

2. **Jednoznačnost počtu $1, -1, 0$**

> V druhé části důkazu si ukážeme, že počet $1, -1, 0$ (signatura) je v diagonální matici přímo dán danou formou $g$.

![alt text](image-445.png)
- tj vektory báze uspořádáme tak, aby to takhle vyšlo
- $\mathbf B$ vznikne uspořádáním vektorů $B$ do sloupců

> Podotýkám, že báze $B$ má jiný význam, než v 1. části důkazu věty.

> Nejprve si ukážeme, že se v obou dvou maticích shoduje počet nul na diagonále. 
>
> Počet nul na diagonále v matici $B$ je roven $n - \text{rank } \mathbf B$
>
> Matici $\mathbf C$ ovšem můžeme získat z matice $\mathbf B$ tak, že ji zprava i zleva vynásobíme maticí přechodu, což je regulární matice, a součin s regulární maticí nemění hodnost.
>
> Proto je hodnost matice $\mathbf B$ stejná jako hodnost matice $\mathbf C$.

$\text{rank }(\mathbf B) = \text{rank }(\text{matice přechodu } \cdot \mathbf B \cdot \text{ matice přechodu}) = \text{rank }(\mathbf C)$

![alt text](image-446.png)

> Nyní se zaměříme na počet $1$. Sporem dokážeme, že $\# 1 \text{ v } B$ a $\# 1 \text{ v } C$ se rovnají

> Předpokládejme nejprve, že by matice $B$ obsahovala více jedniček než matice $C$, čili $r > s$.
>
> V tomto případě uvažme 2 podprostory daného prostoru $\reals^n$:
- $\color{green} U = \text{span}(\mathbf b_1, \dots, \mathbf b_r)$ = generovaný prvními $r$ vektory z báze $B$
- $\color{blue} V = \text{span}(\mathbf c_{s+1}, \dots, \mathbf c_n)$ = generovaný posledními $n-s$ vektory z báze $C$

- $\dim U = r$
- $\dim V = n-s$

![alt text](image-447.png)

![alt text](image-448.png)

![alt text](image-449.png)
- věta z LA1, z [prezentace Věta o výměně, dimenze](https://kam.mff.cuni.cz/~fiala/LA1/542-vymena.pdf)

Levá strana této rovnosti přesahuje $n$.

Na pravé straně $\dim(\text{span } U \cup V) \le \dim \reals^n = n$

To znamená $\dim(U \cap V) \ge 1$

![alt text](image-450.png)

$U \cap V$ má tedy kladnou dimenzi, tzn kromě $\mathbf 0$ obsahuje alespoň $1$ netriviální $\mathbf v$

- že jo vektorový prostor dimenze $0$ obsahuje $\mathbf 0$
	- ač báze prázdná množina
		- ta $\sum$ nula vektorů se taky definuje jako $\mathbf 0$
	- že jo, aby to byl vektorový prostor, tak musí podle def. vektorového prostoru platit, že $(V, +)$ je Abelovská grupa
		- a ta má jako jeden ze svých axiomů:

			V prostoru $V$ existuje prvek $\mathbf{0} \in V$ takový, že pro každý vektor $\mathbf{v} \in V$ platí $\mathbf{v} + \mathbf{0} = \mathbf{v}$

> Když si zapíšeme vektor souřadnic vektoru $\mathbf v$ vůči bázi $B$, zjistíme, že může mít **nenulové** souřadnice pouze v prvních $r$ složkách, protože je lin. kombinací **pouze** vektorů $\mathbf b_1, \dots, \mathbf b_r$
>
> Vektor $\mathbf v$ je navíc nenulový, tzn. alespoň jedna z těchto prvních $r$ složek je nenulová.
>
> Podobně, pohlížíme-li na $\mathbf v$ jako na vektor, kterž jsme získali lineární kombinací posledních $n-s$ vektorů z báze $C$, zjistíme, že souřadnice tohoto vektoru vůči bázi $C$ mají prvních $n-s$ složek nulových, a pot následují další koeficienty, z nichž alespoň jeden je také nenulový.
>
> ![alt text](image-451.png)

- stejně tak protože $\mathbf v \neq \mathbf 0$, alespoň jedno z $d_{s+1}, \dots ,d_n$ je nenulové

![alt text](image-452.png)
- že jo $r = \# 1 \text{ v } \mathbf B$, a $\mathbf B$ je uspořádána tak, že nejdřív jsou sloupce s $1$ na diagonále, pak sloupce s $-1$, pak s $0$
	- tj. prvních $r$ sloupců v $\mathbf B$ obsahuje $1$
- tj. tím $\mathbf B \begin{pmatrix} a_1 \\ \vdots \\ a_n \\ 0 \\ \vdots \\ 0\end{pmatrix}$ se odstraní  části s $-1$, výsledkem bude $\begin{pmatrix} a_1 \\ \vdots \\ a_n \\ 0 \\ \vdots \\ 0\end{pmatrix}$ 

![alt text](image-453.png)

$[\boldsymbol{v}]_C = (0, \dots, 0, d_{s+1}, \dots, d_n)^\mathsf{T}$

- prvních $s$ sloupců $\mathbf C$ mají na diag. $1$, pak jsou ty s $-1$, na konec jsou ty s $0$ 

- tj. tím $C \begin{pmatrix}0 \\ \vdots \\ 0 \\ d_{s+1} \\ \vdots \\d_n \end{pmatrix}$ se jednak odstraní části $\mathbf C$ s $1$, pak se části s $-1$ potkají s koeficienty $d_{s+1}, \dots, d_{\text{rank}(C)}$ (protože víme, kolik ), a části s $0$ se potkají s koeficienty $d_{\text{rank}(C) + 1}, \dots, d_n$, takže výsledkem bude vektor $\begin{pmatrix} 0 \\ \vdots \\ 0 \\ -d_{s+1} \\ \vdots \\-d_{\text{rank}(C)} \\ 0 \\ \vdots \\ 0 \end{pmatrix}$

Pak z $[\mathbf v]_C \begin{pmatrix} 0 \\ \vdots \\ 0 \\ -d_{s+1} \\ \vdots \\-d_{\text{rank}(C)} \\ 0 \\ \vdots \\ 0 \end{pmatrix}$ hned dostáváme $-d_{s+1}^2 - \dots - d_{\text{rank}(C)}^2$

![alt text](image-454.png)
> - Hodnota kvadratické formy jednoho vektoru nemůže být současně kladná a nekladná (že jo $\mathbf C$ a $\mathbf B$ jsou matice stejné formy)
>	- odvodili jsme tedy spor s naším přepokladem , že $r > s$, tj. že by v matici $\mathbf B$ bylo víc jedniček než v matici $\mathbf C$

- Symetricky dokážeme $s \ngtr r$
	- předpokládejme pro spor, že $r < s$
	  
		1. Definujme podprostory:
		- $U = \text{span}(c_1, \dots, c_s)$, $\dim U = s$
		- $V = \text{span}(b_{r+1}, \dots, b_n)$, $\dim V = n-r$
		2. Součet jejich dimenzí je $\dim U + \dim V = s + (n - r) = n + (s - r)$.
		- znovu tedy platí věta o průniku a spojení $\dim U + \dim V = \dim(U \cap V) + \dim(\text{span}(U \cup V))$

		Na pravé straně $\dim(\text{span } U \cup V) \le \dim \reals^n = n$

		To znamená $\dim(U \cap V) \ge 1$

		3. $U \cap V$ obsahuje netriviální vektor
		4. Zvolme $\mathbf v \in (\text{span}(c_1, \dots, c_s) \cap \text{span}(b_{r+1}, \dots, b_n)) \setminus \set 0$

		$[\mathbf v]_C = (a_1, \dots, a_s, 0, \dots, 0)^T$

		$[\mathbf v]_B = (0, \dots, 0, d_{r+1}, \dots, d_n)^T$

		5. Vyhodnoťme $[\mathbf v]_C^T \mathbf C [\mathbf v]_C$ a $[\mathbf v]_B^T \mathbf B [\mathbf v]_B$

		$g(\mathbf v ) = [\mathbf v]_C^T \mathbf C [\mathbf v]_C = a_1^2 + \dots + a_s^2 > 0$

		$g(v) = [v]_B^T B [v]_B = -d_{r+1}^2 - \dots - d_{\text{rank}(B)}^2 \le 0$

		čímž jsme zase došli ke sporu

Celkově tedy $(r \nless s) \land (r \ngtr s) \implies r = s$ 

> A proto mají obě matice stejný počet jak jedniček (to jsme teď dokázali), tak nul (to jsme už dokázali na začátku druhé části důkazu), tak i $-1$ (ty na diagonále zbývají, když mají obě matice stejný řád, a ostatních prvků mají stejně) 
___________

> Na závěr bych rád Sylvestrův zákon setrvačnosti vztáhl k tomu, co jsme se naučili dříve.
>
> Pokud bychom si vzali pozitivně definitní realnou matici, tak ji lze diagonalizovat na jednotkovou matici.
>
> Vzpomeňme si, že Choleského rozklad je součin horní trojúhelníkové matice $U$ se svou hermitovskou transpozicí. A v případě, že pracujeme s realnými maticemi, můžeme hermitovskou transpozici nahradit normální transpozicí a doprostřed tohoto součinu prostě vložit jednotkovou matici.
>
> ![alt text](image-455.png)

> Sylvestrův zákon setrvačnosti můžeme ve skutečnosti vyslovit i pro komplexní symetrické formy. Zde si musíme uvědomit, že komplexní symetrická matice není totéž co hermitovská matice. 
>
> U této věty dostaneme diagonální matice, které budou mít na diagonále jedničky a nuly, jinými slovy se $-1$ můžeme vyhnout, protože ty lze v komplexním oboru odmocnit.
>
> ![alt text](image-456.png)

> Sylvestrův zákon setrvačnosti bylo poslední tvrzení, kterým jsme završili budování teorie v našem kurzu lineární algebry. 
> Přiště si předvedeme, jak formy souvisejí s kuželosečkami a také si předvedeme několik dalších aplikací lineární algebry v jiných oblastech matematiky.