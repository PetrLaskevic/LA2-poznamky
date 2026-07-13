# 1. Determinanty

## Determinanty, základní vlastnosti (15:16, 59M)
prezentace [https://kam.mff.cuni.cz/~fiala/LA2/113-determinanty.pdf](https://kam.mff.cuni.cz/~fiala/LA2/113-determinanty.pdf)

Determinant je číslo, které je přiřazeno ke čtvercové matici.

Byl objeven, když se lidé snažili získat formulku, která by jim umožnila řešit soustavy s regulární maticí.
Hned vám ukážu, o jak složitý výraz jde a jaké má vlastnosti.

Máme-li soustavu 2 lineárních rovnic o 2 neznámých s regulární maticí A, pak víme, že tato soustava má jednoznačné řešení.

![alt text](image.png)


Když tento podíl $\frac{a_{11} b_{2} - a_{21} b_{1}}{a_{11} a_{22} - a_{21} a_{12}}$ dosadíme do vyjádření $x_1$, zjistíme, že podobným podílem můžeme vyjádřit i $x_1$.

Čeho si můžeme všimnout je, že jmenovatelé v obou podílech jsou shodné. V každém se vyskytují koeficienty matice $A$.
A v čitateli se vyskytují koeficienty vektoru pravých stran.

Stejným způsobem, tzn vyjadřováním neznámých a dosazováním do ostatních rovnic můžeme vyřešit i soustavu 3 lineárních rovnic o 3 neznámých s regulární maticí a získat tyto výrazy pro neznámé $x_1$, $x_2$, $x_3$:

![alt text](image-1.png)

Opět si všimneme, že jmenovatelé jsou stejné, v čitatelích jsou výrazy, kde se vyskytují koeficienty z vektoru pravých stran.

Každý jmenovatel je dán součtem několika součinů, přičemž členy, které v těchto součinech jsou vždy vybírají koeficienty tak, že z každého řádku a každého sloupce vybírám pouze 1 člen (tj koeficienty jednoho součinu jsou všechny v různých sloupcích a různých řádcích)

Můžeme si také všimnout, že u některých členů je znaménko kladné, a u některých záporné.

Tyto vlastnosti bude mít i formální definice determinantu.

Než si determinant zadefinujeme, připomeneme si, že symbolem $S_n$ značíme grupu permutací na množině přirozených čísel od $1$ do $n$, a že znaménko permutace odpovídá paritě (=sudost/lichost) počtu inverzí.
Čili máme permutace, které mají kladné znaménko, a permutace, které mají záporné.

![alt text](image-2.png)

Determinant spočteme tak, že:
- probereme všechny možné permutace s grupy permutací na $n$ prvcích
- pro každou z těchto permutací určíme její znaménko, a toto znaménko vynásobíme tím součinem (=co se zmiňoval výše)
	- = součinem, kde postupně vybíráme všechny řádky matice, tím $i$, a na každém řádku vybereme $p(i)$-tý prvek (prvek, který je dán obrazem indexu řádku v rámci permutaci $p$).
- součin společně se znaménkem nám dá 1 sčítanec ve velkém součtu, ve kterém sčítáme přes všechny možné permutace 

![alt text](image-3.png)

Výpočet deteminantu pro matici řádu 2:

Na 2 prvcích máme pouze 2 permutace:
- identickou permutaci (=identitu)
- permutaci, která odpovídá transpozici prvků 2 a 1

identita má kladné znaménko, tranpozice má záporné znaménko

![alt text](image-4.png)

Pro výpočet determinantu matice řádu 3 máme 6 permutací, z toho 3 kladné znaménko, 3 záporné znaménko

![alt text](image-5.png)

Tento výraz odpovídá jmenovateli, který jsme viděli v řešení soustavy 3 lineárních rovnic o 3 neznámých.

Pro zapamatování, které členy mají mít kladné a které záporné znaménko se používá tzv. **Sarrusovo pravidlo** (to je btw fakt dobrý výpočetní trik)

![alt text](image-6.png)

$a_{11} \cdot a_{22} \cdot a_{33} + a_{12} \cdot a_{23} \cdot a_{31} + a_{13} \cdot a_{21} \cdot a_{32} - a_{31} \cdot a_{22} \cdot a_{13} - a_{32} \cdot a_{23} \cdot a_{11} - a_{33} \cdot a_{21} \cdot a_{12}$

Btw: Existuje i varianta, kde se píšou další 2 řádky (ne sloupce):
(vyjde to nastejno):

![](Sarrus_pres_radky.png)

(funguje jenom pro matice 3x3)

![alt text](image-7.png)

![alt text](image-8.png)

(starší verze důkazu sporem z videa:

![alt text](image-10.png)
)

**Ten důkaz sporem, podrobněji:**

>Pokud by $\forall i \in \set{1, \dots, n} :i \le p(i)$
___________________________

(tj. pro každou dvojici $(i, p(i))$ by odpovídající prvek $a_{i, p(i)}$ byl v tom horním trojúhelníku: ![](horni_trojuhelnik.png))
________________
> A pro některé $i_1$ by platilo, že $i_1 < p(i_1)$, pak posloupnost $i_1, i_2 = p(i_1), i_3 = p(i_2), \dots$ roste neomezeně, což není možné.
_____
K pochopení mi pomohlo nakreslit si obrázek:

![](determinant_trojuhelnikove_matice_dukaz.png)

levý sloupec je $i$, pravý sloupec je $p(i)$

Předtím jsme řekli, že $\forall i \in \set{1, \dots, n} :i \le p(i)$. A pak, že pro nějaký prvek platí dokonce $i < p(i)$. To znamená, že ta posloupnost je rostoucí. 
Proč rostoucí, a ne jen neklesající? Protože zobrazení $p(i)$ je permutace, tedy je bijektivní, tj. surjektivní a **prosté** = nemůžou se zobrazit 2 prvky na stejný prvek. 

=> A to teda znamená, že ten prvek, pro který platí $i < p(i)$, na obrázku ta $1$, si vynucuje, aby se další prvek, na obrázku $2$, zobrazil na nějaké vyšší číslo. (Kdyby se $2$ zobrazila na $2$, tak by se dva prvky zobrazily na stejný prvek. To nejde.)

Prvek $2$ tak pro změnu donutí prvek $3$, a tak to prokaskáduje až na konec, na obrázku prvek $4$. Jenže kam se má zobrazit ten?

A zde narážíme na spor = "pak posloupnost $i_1, i_2 = p(i_1), i_3 = p(i_2), \dots$ roste neomezeně, což není možné."

Obor hodnot je omezen, je to jen $\set{1, \dots, n}$
=> spor s tím neomezeně v tom růstu (= ten obor hodnot je pro permutaci daná věc, takže rostoucí na celém def. oboru být nemůže)

Pokud bychom přece chtěli někam prvek $4$ zobrazit, tak nám zbývá akorát $1$ => a to by teda byl spor s tím "rostoucí"

To jest, rozbíjí se to, odhalili jsme spor.

Jinými slovy opravdu platí, že:

> pro $p \neq \text{id}$ existuje $i \in \set{1, \dots, n}$, takový, že $i > p(i)$

(tedy ten "klesající")

=> tedy ten prvek mimo horní trojúhelník
![horní trojúhelník](horni_trojuhelnik.png)
, tedy v oblasti kde jsou $0$

=> každá permutace, která má nějaký člen nad hlavní diagonálou, má i nějaký člen pod ní, který je $0$, proto se do výsledku nezapočítá

=> dá se na to pohlížet i geometricky = tak, že každý součin $\prod_{i=1}^n a_{i, p(i)}$ má $n$ členů, a díky tomu, jak musí být rozmístěny - žádné 2 se nemohou shodovat ani v řádku, ani v sloupci - tak pokud se chceme vyhnout oblasti pod hlavní diagonálou, tak je můžeme naskládat jenom na hlavní diagonálu.
	
=> skutečně, jenom ta permutace nás zajímá, úvodní vztah platí:

$\begin{vmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
0 & a_{22} & \dots & a_{2n} \\
\vdots & \ddots & \ddots & \vdots \\
0 & \dots & 0 & a_{nn}
\end{vmatrix} = a_{11} a_{22} \dots a_{nn}$

![alt text](image-9.png)

### Vlastnosti determinantu

![alt text](image-11.png)
Vztah mezi permutací a její inverzí je bijekce.

(tím $p \to q = p^{-1}$ "zkomprimoval" 2 věci dohromady:
$p \to p^{-1}$ a přeznačení $q = p^{-1}$ pro přehlednost ve zbytku důkazu.)

(a pokud bychom chtěli být formální, tak řekl "bijekce **mezi**", což znamená obojsměrný vztah (bijektivní zobrazení z A do B a jemu inverzní bijektivní zobrazení z B do A), a $\to$ je vztah jednosměrný (bijektivní zobrazení z A do B)
=> asi když se množiny A, B rovnají, tak je to asi jedno

=> mohli bychom ale napsat $p \leftrightarrow p^{-1}$, pro naprostou zřejmost, ne?
)

<br>

![alt text](image-12.png)
použito (co odrážka to rovnítko):
- definice determinantu
- definice transpozice matice
- substituce $p^{-1}(j)$ za $i$ a substituce $j$ za $p(i)$, a aby to sedělo, aby se mělo kde vzít $p^{-1}$, tak v sumě změna z $p$ na $p^{-1}$ (viz další odstavec), využití, že $p$ a $p^{-1}$ má stejné znaménko
- substituce $q$ za $p^{-1}$ - I assume aby nás nemátl ten exponent, prostě další písmenko
- s tím $q$ to zcela jasně odpovídá definici $\det A$ 

Ano, tím $p^{-1} \in S_n$ probereme ve finále stejné permutace jako tím $p \in S_n$, protože v grupě každý prvek má inverzní prvek = každá permutace je k nějaké permutaci inverzní.

=> nutno říct, že ve výrazy $\sum_{p \in S_n}$ a $\sum_{p^{-1} \in S_n}$ bychom neměli brát jako for loopy, které probírají prvky ve stejném pořadí (samozřejmě, $p$ na "i-té pozici" se nutně nerovná $p^{-1}$ (to ostatně platí jenom pro identitu)) => prostě ale v nějakém pořadí se to projde, v grupě je všechno, a sčítání je komutativní, pohoda

(v tom je ta změna $p$ na $p^{-1}$ trochu jiná no, není to substituce v tradičním slova smyslu, kde se ty výrazy rovnají)

Permutace $p$ a její inverze mají stejné znaménko (= že jo logické, protože # inverzí je počet křížení když si permutaci nakreslíme jako graf => pro inverzní permutaci akorát otočíme směř šipek, ale samotné úsečky šipek tam zůstanou => kříží se ve stejných místech, stejný počet křížení => stejný počet inverzí => stejné znaménko (= $-1^{\text{počet inverzí}}$))

![alt text](image-13.png)

použito:
- def. determinantu
- když $j=p(i)$, tak $b_{i, p(i)} = a_{i, q( p(i) )}$
- každý člen sumy vynásobíme $1$, tj. $\text{sgn } (q) \cdot \text{sgn } (q) = 1$
- $q(p(i))$ buď můžeme brát jako postupnou aplikaci permutací: nejdřív aplikujeme $p$, pak $q$, NEBO jako složenou permutaci (tj. aplikujeme jednou tu složenou permutaci $r := q \circ p$, a máme výsledek)
	- abychom mohli udělat tohle, tak je třeba určit znaménko $q \circ p$, což je  $\text{sgn } r =  \text{sgn } (q) \cdot \text{sgn } (p)$
- vytknutí $1 = \text{sgn } q$ před sumu, změna sumy na $r \in S_n$, protože teď pravujeme s tou složenou permutací $r$ (můžeme udělat, protože $S_n$ je grupa permutací = je uzavřena na skládání permutací (a zároveň asi bude platit, že mezi $p \in S_n$ a $q \circ p$ je bijekce)

![alt text](image-15.png)
![alt text](image-17.png)
(protože výměna 2 řádků = ta permutace je transpozice = záporné znaménko ($-1^{\text{\# inverzí}} = -1^1$)) => ? je to 1, nebo jak to je přesně s tím grafem? nekříží to víc po cestě?

![alt text](image-18.png)

> Pak by výměna těchto 2 řádků měla změnit znaménko determinantu (viz bod výše). Ovšem po výměně 2 stejných řádků se nám matice nezmění = čili by měl determinant zůstat stejný.

$d$ je tady myšleno $\det A$:

$\det A = -\det A \implies \det A = 0$

> Ovšem nad tělesy, které mají charakteristiku různou od 2,  se prvek rovná svému inverznímu prvku (ke sčítání = opačnému prvku) pouze tehdy, když je nulový.

(a u tělesa s charakteristikou 2, př $\mathbb{Z}_2$ to neplatí:

Z definice grupy $G$: existence inverzního prvku: 
$\forall a \in G \ \exists b \in G:  a \circ b = e$ 

$\circ$ je obecná operace (tady sčítání, zajímá nás z tělesa ta aditivní grupa)

$e$ je neutrální prvek, k operaci sčítání je to $0$

takže $a + b = 0$

Když do $a$ dosadíme $1$: 

$1 + b = 0$, jsme v $\mathbb{Z}_2$, takže $1 + 1 = 0$

=> inverzní prvek k $1$ je $1$ => máme nenulový prvek, který se rovná svému opačném prvku)

)

> ve skutečnosti toto pozorování platí nejenom u těles $\text{char} \neq 2$, platí obecně


Podle mě bychom mohli alternativně říct, že když má matice 2 stejné řádky, tak odečteme jeden od druhého, tím vytvoříme jeden nulový => a už víme, že matice s nulovým řádkem má nulový determinant.

Když má 2 stejné sloupce, tak ji nejdřív transponujeme, tím determinant nezměníme. Pak znovu získáme nulový řádek =>  a už víme, že matice s nulovým řádkem má nulový determinant.

=> no přepokládal jsem bez důkazu, že ty operace můžeme takhle provádět a determinant se tím nezmění (což teda můžeme)

> tak teda Fialova obecná verze
![alt text](image-19.png)



