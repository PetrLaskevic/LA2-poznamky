## Podobné matice, diagonalizace (15:01, 64M)

https://kam.mff.cuni.cz/~fiala/LA2/412-podobnost.pdf

> Jedno, a to samé lineární zobrazení může být reprezentováno řadou různých matic, a to vzhledem k různým bazím.

> Vlastní číslo i vlastní vektor ovšem zůstává neměnným, pouze co se může měnit, jsou souřadnice vlastního vektoru = vyjádřené vůči různým bazím.

> Dnes si ukážeme, jak se tyto souřadnice mění, a jak lze hledat šikovný popis matice lineárního zobrazení.

![alt text](image-173.png)
$[id]_{B,C}$ = matice přechodu od báze $B$ k bázi $C$

To $[f]_{C,C} [id]_{B,C}$ je $f(id(\mathbf u))$

> Matice přechodu jsou regulární a splňují $[id]_{C,B} = [id]_{B,C}^{-1}$. To vede na koncept podobnosti matic.

### Podobné matice
![alt text](image-174.png)

$$\underbrace{\mathbf A}_{\large [f]_{B,B}} = 
\underbrace{\mathbf R^{-1}}_{\large [id]_{C,B}} \cdot 
\underbrace{\mathbf B}_{\large [f]_{C,C}} \cdot 
\underbrace{\mathbf R}_{\large [id]_{B,C}}$$

To jest **matice $\mathbf A$, $ \mathbf B$ jsou si podobné, právě když jsou to matice stejného zobrazení, akorát vůči různým bazím**
- jedná se stále o stejné zobrazení, co s vektory dělá stejnou věc, je je jinak "pojmenováváme" pomocí souřadnic. Proto musí mezi maticemi $A$, $B$ existovat vztah = podobnost.

> (někdy se to definuje jako $A = R \cdot B \cdot R^{-1}$ = pak se jen liší, co přesně je ta matice $R$:
> - v té 1. definici je to $[id]_{B,C}$
> - v téhle 2. definici je to $[id]_{C,B}$
>
>)

> Stejný vztah jako: ![alt text](image-175.png) lze formulovat pomocí podobnosti takto:
![alt text](image-176.png)
![alt text](image-177.png)

> Bezprostředním důsledkem je, že jsou-li $A$, $B$ navzájem podobné, potom vlastní číslo $\lambda$ má v obou maticích stejnou **geometrickou násobnost** = dimenzi prostoru vlastních vektorů.

![alt text](image-178.png)

- to "$\mathbf v \to \mathbf{Rv}$ je **isomorfismus**"
	- $R$ je, že jo $[id]_{B,C}$

	- **= Každému nezávislému vlastnímu vektoru $\mathbf v$ v matici 
$A$ odpovídá právě jeden nezávislý vlastní vektor $\mathbf{Rv}$ v matici 
$B$.** (viz pozorování)
		- jak jsme měli o pár řádek výše: "pokud je $\mathbf{v}$ vlastní vektor matice $\mathbf A$, pak $\mathbf{w} = R \mathbf{v}$ je vlastní vektor matice $\mathbf B$ pro stejné vlastní číslo $\lambda$."
	
	- **izomorfismus** (= bijektivní lineární zobrazení) je to proto, že matice $\mathbf R $ je regulární (viz věta o charakterizaci izomorfismů (z LA1))
		- ta věta: **bijektivní zobrazení má inverzní zobrazení - a ta věta říká, že jeho matice je inverzní matice**
						- dává smysl, protože $f \circ f^{-1} = \text{id}$ odpovídá $R \cdot R^{-1} = I$

	- to $\mathbf v \to \mathbf{Rv}$ je "divný" způsob zápisu:

		bijektivní (protože řečeno izomorfismus) zobrazení $f: U \to V$ dané $f(\mathbf v) = \mathbf{Rv}$

		($U$ i $V$ jsou podprostory prostoru, nad kterým matice $A$ i $B$ jsou (konkrétně $U$ je podprostor vlastních vektorů matice $A$, a $V$ je podprostor vlastních vektorů matice $B$) - liší se jenom bází, protože $A$, i $B$ očekávají vstup v různých bazích, dávají výstupu v různých bazích, jejich vl. vektory jsou tudíž taky v různých bazích)
		- někdy se pro tuto šipku používá `\mapsto` = $\mathbf v \mapsto \mathbf{Rv}$

> Další společnou vlastností podobných matic je, že mají shodné charakteristické polynomy:

![alt text](image-179.png)

![alt text](image-180.png)
1. definice $p_B(x)$
2. substituce $B = RAR^{-1}$ a rozšíření součinu $xI$ zleva $R$ i zprava $R^{-1}$
	- to můžeme, protože uvnitř je pouze $x$-násobek jednotkové matice:
	
		$R(xI)R^{-1} = x(R(I)R^{-1}) = x(RR^{-1}) = xI$
3. vytknutí $R$ zleva a $R^{-1}$ zprava
4. pravidlo o determinantu součinu matic
5. $\det R$ a $\det(R^{-1})$ jsou navzájem inverzní skaláry
6. definice $p_A(x)$

> Máme-li vlastní číslo matice $A$, která je podobná matici $B$, potom toto vl. číslo má v obou maticích shodnou **algebraickou násobnost**:
![alt text](image-181.png)
Protože algebraická násobnost je násobnost kořene v charakteristickém polynomu a char. polynomy obou matic jsou naprosto shodné.

> Mezi podobnými maticemi, které přísluší témuž lineárnímu zobrazení se budeme snažit nalézt ty, které mají co nejjednodušší struktury. Ukázka:
![alt text](image-182.png)
> Má $[f]_{E,E} = \begin{pmatrix} 0 & 2 \\ -1 & 3 \end{pmatrix}$ nějaký jednodušší popis?

> Tato vlastní čísla a vlastní vektory nám o tomto zobrazení něco říkají. Ve skutečnosti na to samé zobrazení se můžeme dívat tak, že podél osy procházející bodem $\mathbf v_1$ je toto lin. zobrazení fixováno (=žejo vl. číslo $\lambda_1 = 1$). Zatímco podél přímky procházející $\mathbf v_2$ odpovídá toto lin. zobrazení 2násobnému natažení.

> Pokud bychom si za bázi vzali právě vektory $B =  \set{\mathbf v_1, \mathbf v_2}$, tak:
![alt text](image-183.png)

> Situace, kterou jsme si popsali v ukázce, tzn. co se stane, když dosadíme vlastní vektory do báze prostoru, vůči kterému vyjadřujeme matici lineárního zobrazení, ve skutečnosti platí i obecně:

### Proč matice $[f]_{B,B}$, je-li její báze $B$ tvořena pouze vlastními vektory, je diagonální a má na diagonále vlastní čísla
![alt text](image-184.png)

Definice matice lineárního zobrazení:
$[f]_{B,B} = \begin{pmatrix}
\vert & \vert \\
[f(\mathbf{b}_1)]_B & [f(\mathbf{b}_2)]_B \\
\vert & \vert
\end{pmatrix}$, kde $\mathbf{b}_1, \mathbf{b}_2 \in B$ 

A v pozorování se říká, co když nějaký $\mathbf{b}_i$ je vlastní vektor.

V důkazu použito:
1. $f(\mathbf v) = \lambda \mathbf v$
2. výpočet vektoru souřadnic je lineární zobrazení, tj. linearita vůči skalárnímu násobku
	- (viz LA1 ["Lineární zobrazení, afinní prostory"](https://kam.mff.cuni.cz/~fiala/LA1/612-zobrazeni.pdf), slide 5/14![alt text](image-187.png))
3. $\lambda [\mathbf v]_B = \lambda \mathbf e_i$ je vidět z příkladu:

	$[\lambda_1 \mathbf v_1]_B = (a_1, a_2)^T$ kde $\lambda_1 \mathbf v_1 = a_1 \mathbf v_1 + a_2 \mathbf b_2$

	$a_1 = \lambda_1$ a $a_2 = 0$ (určeno jednoznačně, protože $\mathbf v_1, \mathbf b_2$ jsou v bázi $B$, jsou tedy lineárně nezávislé)

	= vždy vybereme koeficient u příslušeného vlastního vektoru z báze $1$ a u ostatních $0$.


### Diagonalizace

![alt text](image-188.png)

Důkaz:

1. prostor $T^n$ má bázi sestávající se z vlastních vektorů $A$. $\implies$ matice $A \in T^{n \times n}$ je podobná diagonální matici

	> z vlastních vektorů matice $A$ sestavíme matici $R$, a protože jich bude dostatek, tato matice bude nutně regulární, a potom součin $AR$ odpovídá součinu $RD$

	> Čili matice $A$ a $D$ si navzájem budou podobné.

	Rozeberme si to:

	Prostor $T^n$ má bázi z $n$ vektorů. Jsou to vlastní vektory, které jsou nezávislé. Takže máme $n$ vlastních vektorů, které můžeme dát vedle sebe do sloupců, a tím stvořit regulární $R \in T^{n \times n}$. Kdyby jich dostatek nebyl, tak by matice nebyla čtvercová, nebo bychom museli vektory opakovat, čímž by pak byla singulární.

	To, že takto sestrojíme $R$ odpovídá matici přechodu $[id]_{C, E}$, kde $C$ je báze vlastních vektorů, a $E$ je standardní báze. (viz definice matice lin. zobrazení: ![alt text](image-185.png)).

	> součin $AR$ odpovídá součinu $RD$

	$\underbrace{\mathbf A}_{\large [f]_{E,E}} \cdot \underbrace{\mathbf R}_{\large [id]_{C,E}} = \underbrace{\mathbf R}_{\large [id]_{C,E}} \cdot \underbrace{\mathbf D}_{\large [f]_{C,C}}$

	kde $C$ je báze vlastních vektorů

	To vychází z obrázku **(potřeba nezapomenout, že sloupce $R$ jsou vlastní vektory)**:

	Sloupce matice $R$ jsou tvořeny vlastními vektory matice $A$. Pojďme se opřít o to, že to jsou vlastní vektory, a tedy pro každý z nich platí vztah $A \mathbf v_i = \lambda_i \mathbf v_i$

	![alt text](image-189.png)
	**Levá část obrázku**
	- provádíme pro každý sloupec součin $A \mathbf v_i$
	- jelikož je $\mathbf v_i$ vlastní vektor matice $A$, tak $A \mathbf v_i = \lambda \mathbf v_i$

	**Pravá část**
	- Násobíme $R \cdot D$, a chceme, aby výsledná matice dopadla tak, že v $i$-tém sloupci bude výsledek $\lambda_i \mathbf v_i$
		- tomu můžeme vyhovět tak, že matice $D$ bude mít na hlavní diagonále vždy $\lambda_i$ a jinde nuly

	Skutečně tedy jsme našli $D$, která vyhoví $AR = RD$.
	Tvar $AR = RD$ můžeme převést na tvar, kterým se běžně definuje "$A$ je podobná $D$" vynásobením zprava $R^{-1}$:

	![alt text](image-190.png)

	**JINÝMI SLOVY:**

	Chceme zjistit, jak vypadá matice zobrazení vůči bázi 
	$C = \{\mathbf v_1, \dots, \mathbf v_n\}$. Označme ji 
	$D = [f]_{C,C}$.
	Podle definice matice zobrazení platí, že její sloupce jsou souřadnice obrazů bázových vektorů vyjádřené v téže bázi.
	Vezměme první bázový vektor 
	$\mathbf v_1$:

	Obraz: 
	$f(\mathbf v_1) = A \mathbf v_1 = \lambda_1 \mathbf v_1$.
	Souřadnice obrazu v bázi 
	$C$: Jak zapíšeme 
	$\lambda_1 \mathbf v_1$ pomocí vektorů 
	$\mathbf v_1, \mathbf v_2, \dots, \mathbf v_n$?
	$$\lambda_1 \mathbf v_1 = \lambda_1 \cdot \mathbf v_1 + 0 \cdot \mathbf v_2 + \dots + 0 \cdot \mathbf v_n$$
	První sloupec 
	$D$: Jsou to právě ty koeficienty: 
	$\begin{pmatrix} \lambda_1 \\ 0 \\ \vdots \\ 0 \end{pmatrix}$.

	Když to samé uděláme pro 
	$i$-tý vektor 
	$v_i$:

	Obraz: 
	$f(v_i) = \lambda_i v_i$.
	Souřadnice: 
	$\lambda_i v_i = 0 \cdot v_1 + \dots + \mathbf{\lambda_i} \cdot v_i + \dots + 0 \cdot v_n$.

	$i$-tý sloupec 
	$D$: Bude mít nuly všude, kromě 
	$i$-tého řádku, kde bude 
	$\lambda_i$.

	$D = \begin{pmatrix} \lambda_1 & 0 & \dots & 0 \\ 0 & \lambda_2 & \dots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \dots & \lambda_n \end{pmatrix}$

	**A to je přesně to naše předchozí pozorování**:

	Obsahuje-li báze 
	$B$ vlastní vektor 
	$\mathbf{v}$ zobrazení 
	$f$, pak sloupec matice 
	$[f]_{B,B}$ odpovídající 
	$\mathbf{v}$ má 
	$\lambda$ na diagonále a jinak 
	$0$.

	Důkaz: 
	$[f(\mathbf{v})]_B = [\lambda \mathbf{v}]_B = \lambda [\mathbf{v}]_B = \lambda \mathbf{e}_i$ kde 
	$i$ je index 
	$\mathbf{v}$ v bázi $B$.

	(toto:)
	![Nadpis: Proč matice $[f]_{B,B}$, je-li její báze $B$ tvořena pouze vlastními vektory, je diagonální a má na diagonále vlastní čísla](image-184.png)

2. matice $A \in T^{n \times n}$ je podobná diagonální matici $\implies$ prostor $T^n$ má bázi sestávající se z vlastních vektorů $A$.

	> Pokud je matice $A$ podobná diagonální matici $D$, můžeme si tento součin přepsat do $AR = RD$, a vidíme, že sloupce této matice $R$ je opravdu tvoří bázi prostoru $T^n$ a všechny jsou vlastními vektory matice $A$

	Rozeberme si to:

	Podívejme se na $AR = RD$ znovu po sloupcích (viz ten obrázek). V tuto chvíli o sloupcech matice $R$ nic nevíme, kromě toho, že jsou lineárně nezávislé, protože matice $R$ je regulární. Označme si ty sloupce $\mathbf v_1, \dots, \mathbf v_n$.

	$A \cdot R = \begin{pmatrix} | & | & & | \\ A \mathbf v_1 & A \mathbf v_2 & \dots & A \mathbf v_n \\ | & | & & | \end{pmatrix}$

	$R \cdot D = \begin{pmatrix} | & | & & | \\ d_{1,1} \mathbf v_1 & d_{2,2} \mathbf v_2 & \dots & d_{n,n} \mathbf v_n \\ | & | & & | \end{pmatrix}$


	$AR = RD$

	$\begin{pmatrix} | & | & & | \\ A \mathbf v_1 & A \mathbf v_2 & \dots & A \mathbf v_n \\ | & | & & | \end{pmatrix} = \begin{pmatrix} | & | & & | \\ d_{1,1} \mathbf v_1 & d_{2,2} \mathbf v_2 & \dots & d_{n,n} \mathbf v_n \\ | & | & & | \end{pmatrix}$

	$A \mathbf v_i =  d_{i,i} \mathbf v_i$ je definice toho, že $\mathbf v_i$ je vlastní vektor.
	Takže všechny naše vektory $\mathbf v_1, \dots, \mathbf v_n$ jsou vlastní vektory, a, jak už víme z regularity $R$ jsou lineárně nezávislé. Máme $n$ lineárně nezávislých vektorů = všechno co potřebujeme pro sestavení báze prostoru $T^n$.

### Diagonalizovatelná matice
![alt text](image-191.png)


A samotný ten nadpis **Diagonalizace** tam vysvětlený není, ale I assume, že to JE to nalezení matice $D$ s vlastními čísly matice $A$ na diagonále. To že taková matice dává smysl, platí právě když:

$\exists \text{ regulární } R: AR = RD$
