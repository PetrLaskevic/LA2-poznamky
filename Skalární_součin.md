
## Skalární součin, norma, Cauchyova-Schwarzova nerovnost (14:36, 90M)

> V poslední lekci jsme měli situaci, kdy bylo třeba mezi sebou vynásobit 2 aritmetické vektory maticovým součinem, a výsledkem byl 1 prvek tělesa = skalár

> **Připomínám, že v obecném vektorovém prostoru součin $2$ vektorů není možný** (pokud jeden z nich že jo netransponujeme a neuděláme maticový součin) **- pouze je dovoleno 2 vektory spolu sečíst, a nebo provést skalární násobek vektoru**

> Doba však dozrála k tomu, abychom si pojem vektorového prostoru rozšířili i o součin 2 vektorů. Bude to tzv. skalární součin.

> Podotýkám však, že se nejprve omezíme na vektorové prostory nad realnými a nad komplexními čísly.

![alt text](image-259.png)
- čili na $\reals$ dá se říct komutativita
- zobrazení z $V \times V$ = kartézský součin $V$ se sebou samým $V$ = libovolná dvojice vektorů z $V$
- linearita vůči součtu bude i vzhledem k 2. složce, ale to si odvodíme z ostatních axiomů (forward ref):

	![alt text](image-264.png)
### Ukázky, mj. Standardní skalární součin
![alt text](image-260.png)
- šlo by i $\mathbf u^T (\mathbf v^H)^T$, což odpovídá pořadí $u_i \overline{v_i}$
	- jde to protože výsledkem tohoto maticového součinu je skalár, což je jako matice o $1$ prvku = je symetrická, platí pro ni $A = A^T$
- ze stejného důvodu u skal. součinu na $\reals^n$ by šlo: $\mathbf u^T \mathbf v$

#### Skalární součin na $\reals^n$ určený regulární maticí $A$
> skal. součin 2 vektorů můžeme definovat pomocí maticového součinu,  tak že doprostřed součinu $\mathbf v^T \mathbf u$ ještě vložíme součin matice s její transpozicí 
>
> ![alt text](image-261.png)
> vidíme, že kromě $u_i v_i$ zde máme i smíšené součiny
> je třeba ukázat, že i tento skalární součin všech 5 axiomů z definice
- nebo se na to dívat tak, že $\mathbf v^T A^T$ je $(A\mathbf v)^T$, tj. $\langle \mathbf u | \mathbf v \rangle = (A\mathbf v)^T A \mathbf u$
	- tj. že na oba operandy provedeme lineární zobrazení $A$ (zobrazení dané regulární $A$ určitě je lineární, dokonce je to izomorfismus), a pak na ně provedeme standardní skalární součin

> lze ukázat, že i takto definovaný součet splňuje všechny axiomy
>
> ![alt text](image-262.png)
- pokud bychom si namísto aritmetických vektorů vzali spojité objekty, tzn. 2 funkce, taky je můžeme mezi sebou vynásobit ve všech bodech a potom vše dohromady sečíst, ovšem pomocí integrálů.

### Vlastnosti skalárního součinu
![alt text](image-263.png)
- číslo a k němu komplexně sdružené se rovná právě když je realné, že jo $a + bi = a - bi$, když $b = 0$
#### Linearita vůči součtu v druhé složce
![alt text](image-264.png)
- použita vlastnost komplexního sdružení, že součet, nad kterým provedeme komplexní sdružení, je stejný, jako když komplexní sdružení provedeme na jednotlivých sčítancích (to afaik se nikde neodvozovalo, ale dává to smysl)
- použit 3. axiom, o záměně pořadí vektorů

![alt text](image-265.png)

![alt text](image-266.png)
$$\left\langle \sum_{i=1}^k a_i \mathbf u_i  \middle| \sum_{i=1}^l b_j \mathbf v_j  \right\rangle$$

$$\left\langle  a_1 \mathbf u_1 + \dots + a_k \mathbf u_k  \middle| \sum_{i=1}^l b_j \mathbf v_j  \right\rangle$$

$$\left\langle  a_1 \mathbf u_1 \middle| \sum_{i=1}^l b_j \mathbf v_j  \right\rangle + \dots + \left\langle  a_k \mathbf u_k \middle| \sum_{i=1}^l b_j \mathbf v_j  \right\rangle$$

$$a_1\left\langle \mathbf u_1 \middle| \sum_{i=1}^l b_j \mathbf v_j  \right\rangle + \dots +  a_k \left\langle \mathbf u_k \middle| \sum_{i=1}^l b_j \mathbf v_j  \right\rangle$$

Rozepišme si 1. sčítanec:

$$a_1\left\langle \mathbf u_1 \middle| \sum_{i=1}^l b_j \mathbf v_j  \right\rangle$$

$$a_1\left\langle \mathbf u_1 \middle| b_1 \mathbf v_1 + \dots + b_l \mathbf v_l \right\rangle$$

$$a_1\left\langle \mathbf u_1 \middle| b_1 \mathbf v_1 \right\rangle + \dots + a_1\left\langle \mathbf u_1 \middle| b_l \mathbf v_l \right\rangle$$

$$a_1\overline{b_1} \left\langle \mathbf u_1 \middle| \mathbf v_1 \right\rangle + \dots + a_1 \overline{b_l} \left\langle \mathbf u_1 \middle| \mathbf v_l \right\rangle$$

Takto tedy vypadá rozepsaný 1. sčítanec.

$$\sum_{j=1}^l a_1 \overline{b_j} \left\langle \mathbf u_1 \middle| \mathbf v_j \right\rangle$$

My jich máme ale celkově $k$:

$$\sum_{j=1}^l a_1 \overline{b_j} \left\langle \mathbf u_1 \middle| \mathbf v_j \right\rangle + \dots + \sum_{j=1}^l a_i \overline{b_j} \left\langle \mathbf u_i \middle| \mathbf v_j \right\rangle + \dots + \sum_{j=1}^l a_k \overline{b_j} \left\langle \mathbf u_k \middle| \mathbf v_j \right\rangle$$

Tedy je to součet $k$ sčítanců, z nichž každý je vyjádřen sumou $\sum_{j=1}^l$.

$$\sum_{i=1}^k \left( \sum_{j=1}^l a_i \overline{b_j} \left\langle \mathbf u_i \middle| \mathbf v_j \right\rangle \right)$$

V podstatě jako nested `for`, kde $\sum_{j=1}^l$ je ta vnitrřní smyčka a $\sum_{i=1}^k$ ta vnější.

On tam akorát nenapsal tu závorku.
___
![alt text](image-267.png)
$t \overline{t} = (a+bi)(a-bi) = a^2 - b^2 i^2= a^2+b^2$

absolutní hodnota komplexního čísla je $\sqrt{a^2+b^2}$

> Nyní už máme skalární součin nadefinovaný a známe také jeho některé podoby. Připomínám, že byl motivován geometricky, a proto si na Euklidovských prostorech aukážeme, jak souvisí s úhly a délkami úseček.

> Poté také odvodíme některá známá fakta, jako např. trojúhelníkovou nerovnost nebo Cauchyho-Schwarzovu nerovnost.

![alt text](image-268.png)
$$||\mathbf u|| = \sqrt{\langle \mathbf u | \mathbf u \rangle} = \sqrt{\sum_{i=1}^n u_i \overline{u_i}} = \sqrt{|u_1|^2 + \dots +|u_n|^2}$$
- btw. v podstatě jako abs. hodnota komplexního čísla, ale pro vektory (že jo komplexní čísla bychom samy o sobě mohli vnímat jako vektory o $2$ složkách)

![alt text](image-269.png)
$$||t\mathbf u|| := \sqrt{\langle t \mathbf u | t \mathbf u \rangle} = \sqrt{t \overline{t} \langle \mathbf u | \mathbf u \rangle} = \sqrt{|t|^2\langle \mathbf u | \mathbf u \rangle} = \sqrt{|t|^2} \sqrt{\langle \mathbf u | \mathbf u \rangle} = |t| \cdot ||\mathbf u||$$

#### Geometrická interpretace normy
![alt text](image-270.png)

$$-2 \| \mathbf{u} \| \cdot \| \mathbf{v} \| \cos \varphi =
- \langle \mathbf u | \mathbf v \rangle - \langle \mathbf v | \mathbf u \rangle$$
Jsme na $\reals^n$, komplexně sdružené číslo k realnému číslu je realné číslo, tj. máme komutativitu:
$- \langle \mathbf u | \mathbf v \rangle - \langle \mathbf v | \mathbf u \rangle = -2 \langle \mathbf u | \mathbf v \rangle$
### Cauchyho-Schwarzova nerovnost
![alt text](image-271.png)
- protože
$\sqrt{\langle \mathbf u | \mathbf u \rangle \langle \mathbf v | \mathbf v \rangle} = \sqrt{\langle \mathbf u | \mathbf u \rangle}\sqrt{\langle \mathbf v | \mathbf v \rangle}$

- ta absolutní hodnota je tam proto, aby tam lvelo bylo vždy realné č. (abychom neporovnávali komplexní $\le$ realné, to nejde)

![alt text](image-272.png)
> Pro důkaz nerovnosti v ostatních případech nejprve prozkoumáme, jak vypadá 2. mocnina normy lin. kombinace, kde k $\mathbf u$ přičteme vhodný skalární násobek $\mathbf v$ (jaký vzít si ukážeme za chvíli)

![alt text](image-273.png)
![](dukaz_cauchy_schwarz.png)

### Důsledky Cauchyho-Schwarzovy nerovnosti

![alt text](image-274.png)
Btw **Definice: kvadratický průměr**
$$=\sqrt {{1 \over n} \sum_{i=1}^{n} u_i^2} = \sqrt {{u_1^2 + u_2^2 + \cdots + u_n^2} \over n}$$
= odmocnina z aritmetického průměru druhých mocnin složek toho vektoru

Tím jak ten vektor je realný, tak v tom vzorci nemusí na složky $u_i$ nemusí být absolutní hodnota.
- že jo na komplexní čísla by nefungovala pořadně odmocnina = 2 výsledky - s tím by si afaik nevědělo rady $\le$
- také $\le$ ostatně funguje jenom pro realná čísla (která mají lineární uspořádání)

Obecná verze vzorce (pro komplexní vektor) by btw afaik vypadala takto:
$$\left| \sum_{i=1}^{n} u_{i} \right| \leq \sqrt{\sum_{i=1}^{n} |u_{i}|^{2}} \cdot \sqrt{n}$$
(a dokázalo by se to stejně)
(
$\langle \boldsymbol{u} \mid \boldsymbol{u} \rangle = \sum u_i \overline{u_i} = \sum |u_i|^2$
)
![alt text](image-275.png)

<details>
<summary>Detour, jak by to bylo u komplexních čísel</summary>

(pro komplexní by std. součin byl $\langle \boldsymbol{u} \mid \boldsymbol{v} \rangle = \sum u_i \overline{v_i}$,

U standardního skalárního součinu (i v komplexním oboru) počítáme 
$\sum u_i \cdot \overline{v_i}$. Protože 
$v_i = 1$, tak 
$\overline{1} = 1$.

$$\langle \boldsymbol{u} \mid \boldsymbol{v}\rangle = u_1 \cdot 1 + u_2 \cdot 1 + \dots + u_n \cdot 1 = \sum_{i=1}^n u_i$$
Když na to aplikujeme tu absolutní hodnotu z, máme levou stranu:

$$\left| \sum_{i=1}^n u_i \right| = |\langle \boldsymbol{u} \mid \boldsymbol{v} \rangle |$$

Pak aplikujeme Cauchyho-Schwarzovu větu.

A zbytek dokončíme stejně, akorát na tu abs. hodnotu u $u_i$ pod odmocninou.
</details>

![alt text](image-276.png)
- makes sense, to nalevo by se to mohlo od sebe odečíst

![](dukaz_norma_splnuje_trojuhelnikovou_nerovnost.png)

> Předvedli jsme si, že v Euklidovských prostorech (= ty $\reals^n$) odpovídá skalární součin úhlu mezi $2$ vektory. V realném životě se však $1$ z úhlů vyskytuje častěji než jiný = pravý úhel. Kolmost prozkoumáme v příštích lekcích podrobněji.

## Kolmost, ortonormální báze, Fourierovy koeficienty, isometrie (19:38, 117M)

> Minule jsme zjistili, že v Euklidovských prostorech (= $\reals^n$) odpovídá skalární součin kosinu úhlu sevřeneho 2 vektory (přesněji řečeno $\langle \mathbf u | \mathbf v \rangle = ||\mathbf u || \cdot || \mathbf v || \cdot \cos \varphi$)

> Kosinus pravého úhlu je 0, a proto definice kolmých vektorů bude velice jednoduchá:

![alt text](image-277.png)

![alt text](image-278.png)
- tedy $\mathbf v_0$ nepatří do množiny netriválních vektorů, což je spor

> Už dobře víme, že standardní skalární součin se počítá tak, že 2 vektory postupně procházíme po složkách, ty mezi sebou násobíme a všechny dílčí součty pak dohromady sečteme.
>
> Pokud bycho si namísto aritmetických vektorů vzali spojité objekty, tzn. 2 funkce, taky je můžeme mezi sebou vynásobit ve všech bodech a potom vše dohromady sečíst, ovšem pomocí integrálů. To je standardní skalární součin na množině funkcí, tak, jak jsme si jej zavedli minule.

### Ortonormální báze
![alt text](image-279.png)
![alt text](image-280.png)
$$A = \begin{pmatrix}
| & | & & | \\
\mathbf e_1  & \mathbf e_2  & \dots & \mathbf e_n \\
| & | & & |
\end{pmatrix}$$

$$A^H = \begin{pmatrix}
\text{---} & \mathbf e_1^H & \text{---} \\
\text{---} & \mathbf e_2^H & \text{---} \\
& \vdots  &\\
\text{---} & \mathbf e_n^H &\text{---} \\
\end{pmatrix}$$

Viz unitární matice splňuje $\mathbf v_i^H \mathbf v_i = 1$ a pro $i \neq j: \mathbf v_i^H \mathbf v_j = 0$

S vektory standardní báze jako sloupce to je vidět hned, ale platí to pro jakoukoli ortonormální bázi, viz její definice. 

- $|| \mathbf b_i || = 1$, tedy $\sqrt{|b_1|^2 + \dots + |b_n|^2} = \sqrt{\langle \mathbf b_i | \mathbf b_i \rangle} = 1$, tj. $\langle \mathbf b_i | \mathbf b_i \rangle = 1$ 
- $\boldsymbol{b}_i \perp \boldsymbol{b}_j \iff \langle \mathbf b_i | \mathbf b_j \rangle = 0$

### Ukázky
![alt text](image-281.png)
![alt text](image-282.png)
![alt text](image-283.png)
![alt text](image-284.png)

### Vlastnosti ortonormální báze: Fourierovy koeficienty
![alt text](image-285.png)
- pro ty vektory jsou kolmé, pro $i \neq j$ je skal. součin $0$, jenom pro $i=j$ to je $1$

![alt text](image-286.png)

![alt text](image-287.png)
- této věty jsme už využili, když jsme definovali standardní skalární součin na $\reals^n$ a $\mathbb{C}^n$ (ty že jo mají by default standardní bázi, která je ortonormální)
	- ![alt text](image-260.png)
		- pokud bychom si v $\mathbb{C}^n$ nebo $\reals^n$ vzali jinou než ortonormální bázi, tak by v skalárním součinu byly **smíšené členy**, viz část <details> <summary>
		"Skalární součin na $\reals^n$ určený regulární maticí $A$"</summary>
		![alt text](image-261.png)
		zde ty smíšené členy jsou $2u_1 v_2$ a $2u_2 v_1$ 
			</details>

			- potřeba se na to dívat tak, že $\mathbf v^T A^T$ je $(A\mathbf v)^T$, tj. $\langle \mathbf u | \mathbf v \rangle = (A\mathbf v)^T A \mathbf u$
			- tj. že na oba operandy provedeme lineární zobrazení $A$, zde **matice přechodu od původní báze k nějaké ortogonální bázi**, a pak na ně provedeme standardní skalární součin

![alt text](image-288.png)
- vnitřní sumu můžeme odstranit tím, že si uvědomíme, že člen  $\langle \mathbf b_i | \mathbf b_j \rangle$ bude $0$ kromě případu $j=i$, kdy bude $1$.
- $n$ složek $\langle \mathbf u | \mathbf b_i \rangle$ odpovídá $[\mathbf u]_B$ (=Fourierovy koeficienty)
- $n$ složek $\overline{\langle \mathbf v | \mathbf b_i \rangle}$ odpovídá $[\mathbf v]^H_B$ (=Fourierovy koeficienty)
- součin skalárů je v tělese vždy komutativní, proto můžeme činitele v součinu v sumě prohodit

### Lineární zobrazení, která zachovávají skalární součin (=isometrie)
![alt text](image-289.png)
![alt text](image-290.png)

> Ukážeme si větu, díky níž už nemusíme kontrolovat skalární součin všech možných dvojic vektorů, stačí zkontrolovat, že se zachovává skalární součin každého vektoru se sebou samým. Jinými slovy, tato podmínka je jednodušší než ta, kterou je isometrie definována.
>
> ![alt text](image-291.png)

![alt text](image-292.png)
isometrie, tj. zachovává skalární součin $\implies$ zachovává normu

norma je definována odmocninou ze skalárního součinu $2$ stejných vektorů

$\forall \mathbf u, \mathbf v \in V:  \langle \mathbf u | \mathbf v \rangle =  \langle f(\mathbf u) | f(\mathbf v) \rangle \implies \forall \mathbf u \in V: \langle \mathbf u | \mathbf u \rangle =  \langle f(\mathbf u) | f(\mathbf u) \rangle \implies ||\mathbf u||= \sqrt{\langle \mathbf u | \mathbf u \rangle} = \sqrt{\langle f(\mathbf u) | f(\mathbf u) \rangle} = || f(\mathbf u) ||$
_______

zachovává normu $\implies$ isometrie, tj. zachovává skalární součin

podívejme se, jakou hodnotu nabývá $|| \mathbf u + t \mathbf v ||^2$ = lin. kombinace $\mathbf u$ a $t \mathbf v$, přičemž hodnotu toho skal. násobku si určíme za chvilku

Stejně, tak, když zachovává normu (=předpoklad), tak se norma této lin. kombinace rovná normě svého obrazu. 

![alt text](image-293.png)
- červeně tedy máme členy, které se díky předpokladu rovnají
	- tzn. součty zbytků se rovnájí

- je to komplexní rovnice, tj. číslo na levé i na pravé části má reálnou a imaginární část.


TODO: zamyslet se 
Naše rovnice vypadá v podstatě takto:

$t \bar{A} + \bar{t} A = t \bar{B} + \bar{t} B$

my chceme zjistit, čemu se rovná realná a čemu imaginární část.

Pokud zvolíme pouze jednu hodnotu, například 
$t = 1$:

$$\bar{A} + A = \bar{B} + B$$
Protože 
$A + \bar{A} = 2\operatorname{Re}(A)$, tato rovnice nám říká pouze to, že:

$$\operatorname{Re}(\langle\boldsymbol{u}\mid\boldsymbol{v}\rangle) = \operatorname{Re}(\langle f(\boldsymbol{u})\mid f(\boldsymbol{v})\rangle)$$
To znamená: reálné části se rovnají, ale o imaginárních částech nevíme vůbec nic. (Například čísla 
$2 + 5\mathrm{i}$ a 
$2 - 3\mathrm{i}$ mají stejnou reálnou část, ale nejsou stejná).

Proč potřebujeme i druhou hodnotu (
$t = \mathrm{i}$)?
Abychom zjistili, co se děje s imaginární částí, potřebujeme druhou nezávislou rovnici. Proto dosadíme 
$t = \mathrm{i}$:

$$\bar{A} - A = \bar{B} - B$$
Tato druhá rovnice nám dává informaci o imaginární části:

$$\operatorname{Im}(\langle\boldsymbol{u}\mid\boldsymbol{v}\rangle) = \operatorname{Im}(\langle f(\boldsymbol{u})\mid f(\boldsymbol{v})\rangle)$$


TODO: pak teda dobrá otázka, co s tím t=1 a t=i

- když odečteme druhou rovnici od první, máme výsledek

### Maticová charakterizace bijektivních isometrií
> v ukázkách **isometrií** jsem záměrně uváděl jejich matice, protože matice zobrazení lze hezky využít při charakterizaci bijektivních isometrií. To je shrnuto v této větě:
>
> ![alt text](image-294.png)

#### Důkaz 
> Již dříve jsme si ukázali, že lin. zobrazení je bijekcí (=isomorfismem) právě když matice tohoto zobrazení je regulární.
>
> ![alt text](image-295.png)

![alt text](image-296.png)
- to jedna implikace (použit předpoklad "díky isometrii")

![alt text](image-297.png)
- v tomhle je schovaná i ta druhá, je tam psáno "pokud", ale to jistě $\iff$, protože ta rovnost je definiční robnost isometrie, a isometrie je definována pomocí ekvivalence:
	- ![alt text](image-298.png)

> Zjistili jsme, že ortonormální báze mají řadu pěkných vlastností, které umožní zjednodušit řadu výpočtů.
>
> Ovšem nevíme, jak takové ortonormální báze nalézt. To se dozvíme příště.