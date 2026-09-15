# Věty a tvrzení 
tak nějak sepsané věty a tvrzení na LA2 k Fialovi, nezaručuju že neobsahuje chyby.

taky jsem to psal pro sebe, takže nezaručuju že se v tom dá vyznat.

(body za větu / body za důkaz).

1. věta o linearitě determinantu. (8/10\)

	$$
	t\begin{vmatrix}
	-a_1^T-\\
	-a_2^T-\\
	-a_3^T-\\
	-a_4^T-\\
	\end{vmatrix}=
	\begin{vmatrix}
	-ta_1^T-\\
	-a_2^T-\\
	-a_3^T-\\
	-a_4^T-\\
	\end{vmatrix}=
	\begin{vmatrix}
	-a_1^T-\\
	-ta_2^T-\\
	-a_3^T-\\
	-a_4^T-\\
	\end{vmatrix}
	$$
	$$
	\begin{vmatrix}
	-a_1^T-\\
	-a_2^T-\\
	-b^T+c^T-\\
	-a_4^T-\\
	\end{vmatrix}=
	\begin{vmatrix}
	-a_1^T-\\
	-a_2^T-\\
	-b^T-\\
	-a_4^T-\\
	\end{vmatrix}+
	\begin{vmatrix}
	-a_1^T-\\
	-a_2^T-\\
	-c^T-\\
	-a_4^T-\\
	\end{vmatrix}
	$$

2. věta o determinantu součinu dvou matic. (6/12\)

    $$\det(AB)=\det(A) \cdot \det(B)$$

3. věta o Laplaceově rozvoji determinantu. (8/10\)

    $$\det(A^{n\times n})=\sum\limits^{n}_{j=1}{a_{ij}(-1)^{i+j}\det(A^{ij}})$$

    $A^{ij}$ je podmatice získaná z $A$ odstraněním i-tého řádku a j-tého sloupce.

4. Cramerovo pravidlo pro řešení soustav přes determinanty.(8/10\)

	$A_{i\to b}$ značí že i-tý sloupec nahradíme vektorem $b$
    $$Ax=b \implies x_i = \frac{\det(A_{i \to b})}{\det(A)}$$

5. věta o adjungované matici. (8/10\)

    $$A \in T^{n\times n}, n\geq 2: A^{-1} = \frac{\operatorname{adj}(A)}{\det(A)}$$

6. větu o počtu koster grafu. (8/14\)

    Laplaceova matice grafu $G$ na $V_G = \set{v_1, . . . , v_n}$ je $L_G \in R^ {n\times n}$, kde $k$ je násobnost hrany a $deg(v_i)$ nepočítá smyčky:
	$$
	L(G)_{ij}=
	\begin{cases}
	deg(v_i) & i=j\\
	-k & (v_i,v_j) \in E_G \land i\ne j\\
	0
	\end{cases}
	$$

	potom má graf $\det(L^{1,1}_G)$ koster

7. malou Fermatovu větu. (6/8)

    pro každé prvočíslo $p$ a každé $x\in \Bbb{Z}_p \setminus \{0\}$: $x^{p-1}=1$

8. větu o Vandermondově matici. (6/10)

    Pro $n + 1$ dvojic $(x_0, y_0), . . . ,(x_n, y_n)$ s různými $x_i$ , najít $p \in T(x)$ stupně nejvýše $n$ takový, že $p(x_i) = y_i$ pro každé $i$. 

    Vandermondova matice $V_{n+1}(x_0,\dots,x_n)$ je definovaná takto a koeficienty $a_0,...,a_n$ z polynomu $p$ řeší tuto soustavu:

	$$
	\underbrace{\begin{pmatrix}
	1 &&x_0&&x_0^2&&... &&x_0^n\\
	1 &&x_1&&x_1^2&&... &&x_1^n\\
	\vdots&&\vdots&&\vdots&&\ddots&&\vdots\\
	1 &&x_n&&x_n^2&&... &&x_n^n\\
	\end{pmatrix}}_{\normalsize V_{n+1}(x_0,\dots,x_n)}
	\begin{pmatrix}
	a_0\\
	a_1\\
	\vdots\\
	a_n\\
	\end{pmatrix}=
	\begin{pmatrix}
	y_0\\
	y_1\\
	\vdots\\
	y_n\\
	\end{pmatrix}
	$$

	k tomu:
	Vandermondova matice $V_{n+1}$ je regulární pokud jsou $x_0,\dots,x_n$ navzájem různé

9.  správnost Lagrangeovy interpolace. (8/10\)

    

10. pozorování o podprostoru vlastních vektorů. (6/8\)

    vlastní vektory příslušné stejnému vlastnímu číslu tvoří podprostor

11. větu o lineární nezávislosti vlastních vektorů. (6/8\)

    mějme vlastní čísla $\lambda_1,\dots,\lambda_k$ a k nim příslusné netriviální vlastní vektory $v_1,\dots,v_k$, potom jsou tyto vektory lineárně nezávislé

12. větu o kořenech charakteristického polynomu matice. (6/8\)

    $\lambda$ je vlastním číslem $A$ právě tehdy když je $\lambda$ kořenem charakteristického polynomu $A$

13. větu o konstrukci matice s předepsaným charakteristickým polynomem. (8/10\)

    Pro libovolná $b_0, b_1, . . . , b_{n−1} \in T$ má matice

	$$
	\begin{pmatrix}
	0&0&\dots&0&-b_0\\
	1&0&...&0&-b_1\\
	0&1&...&0&-b_2\\
	\vdots&\vdots&\ddots&\vdots&\vdots\\
	0&0&...&1&-b_{n-1}\\
	\end{pmatrix}\in \Bbb{T}^{n\times n} 
	$$

	charakteristický polynom $(x^n+b_{n-1}x^{n-1}+\dots+b_1x+b_0)(-1)^n$ 

14. pozorování o hodnotách tří koeficientů charakteristického polynomu matice. (10/12\)

    $b_n=(-1)^n$

    $b_0=\det(A)$

    $b_{n-1}=(-1)^{n-1}\sum\limits_{i=1}^n{a_{ii}}$ 

15. větu o Geršgorinových kruzích. (8/10\)

    Nechť $A \in \mathbb{C}^{n\times n}$. Pro každé vlastní číslo $\lambda$ existuje index řádku $i \in \{1, . . . , n\}$ takový, že $|\lambda − a_{ii}| \leq \sum\limits_{j\ne i} |a_{ij}|$.

16. Cayleyovu–Hamiltonovu větu. (8/14\)

    pro $A\in\Bbb{T}^{n\times{n}}$ a její polynom platí:

    $p_A(x)=(-1)^nx^n+b_{n-1}x^{n-1}+\dots+b_1x+b_0$

    $p_A(A)=(-1)^nA^n+b_{n-1}A^{n-1}+\dots+b_1A+b_0I =0^{n\times n}$ 

17. Dvě pozorování a související důsledky o násobnostech vlastních čísel podobných matic. (6/8\)

    pokud $A$ je podobné $B$, tj. $A=RBR^{-1}$ a $\lambda$ je vlastní číslo $A$ a $v$ je k němu příslušný vlastní vektor, pak $\lambda$ je vlastní číslo $B$ a vektor k němu příslušný je $Rv$.
    z toho plyne že $\lambda$ má v $B$ stejnou geometrickou násobnost jako v $A$.
    pokud $A$ je podobné $B$, pak $p_A(x)=p_B(x)$
    z toho plyne že $\lambda$ má v $B$ stejnou algebraickou násobnost jako v $A$

18. větu o vztahu geometrické a algebraické násobnosti vlastního čísla. (6/10\)

    pro každé vlastní číslo $\lambda$ matice $A$ platí že jeho geometrická násobnost je maximálně tak velká jako jeho algebraická násobnost

19. nezbytnou a postačující podmínku, kdy je matice diagonalizovatelná. (6/8\)

    právě tehdy když se algebraická násobnost každého vlastního čísla matice $A$ rovná jeho geometrické násobností, je matice $A$ diagonalizovatelná.
	pokud má $A^{n\times n}$ právě $n$ různých vlastních čísel, je diagonalizovatelná, ale ne naopak

20. tvrzení o zobecněných vlastních vektorech. (8/8\)

    $J_\lambda$ je jordanův blok
	nechť $AR=RJ_\lambda$, označímeli $i$-tý sloupec $R$ jako $v_i$, pak splňuje $(A-\lambda I)^iv_i=0$
	vektor co toto splňuje se nazývá **zobecněný vlastní vektor**

21. větu o diagonalizaci speciálních komplexních matic. (6/14\)

    každá hermitovská matice $A$ má realná vlastní čísla, navíc existuje unitární $R$ taková že $RAR^{-1}$ je diagonální

22. Cauchyovu–Schwarzovu nerovnost. (6/10\)

    každý skalarní součin nad $\Bbb{C}$ splňuje: $|\langle x,y\rangle|\leq\lVert x\rVert \cdot \lVert y\rVert=\sqrt{\langle x,x\rangle\langle y,y\rangle}$ 

23. vztah mezi aritmetickým a kvadratickým průměrem. (8/8\)

    pro $u\in \Bbb{R}^n$:
	$$
	\frac{\sum\limits_{i=1}^n{u_i}}{n}\leq
	\sqrt{\frac{\sum\limits_{i=1}^n{u_i^2}}{n}}
	$$

24. trojúhelníkovou nerovnost. (6/10\)

    $\lVert{u+v}\rVert\leq\lVert{u}\rVert+\lVert{v}\rVert$

25. pozorování o navzájem kolmých vektorech. (6/8\)

    množina netriviálních vzájemně kolmých vektorů je lineárně nezávislá

26. tvrzení o Fourierových koeficientech. (6/8\)

    nechť $B=(b_1,b_2,\dots,b_n)$ je ortonormální báze prostoru $V$.
	pro každé $v \in V$ platí: $v=\sum\limits_{i=1}^n{\langle{v|b_1}\rangle b_i}$. Koeficienty  $\langle{v|b_1}\rangle$ se nazívají fourierovy koeficienty

27. větu o výpočtu skalárního součinu z Fourierových koeficientů. (8/10\)

    pro každé $u,v \in V$ platí: $\langle{u|v}\rangle=[v]^H_B[u]_B$

28. tvrzení o kolmé projekci a normě. (8/10\)

    $U\Subset V$ s bází $B$, potom ortogonální projekce vektoru $u$ do podprostoru generovaného $B$ se značí $p_B(u)$ a je to takový vektor z $U$ který minimalizuje $\Vert{u-p_B(u)}\rVert$

29.  správnost Gramovy–Schmidtovy ortonormalizace. (6/8\)

    

30. větu o izometrii a normě. (6/10\)

    lineární zobrazení $f$ je izometrie právě tehdy když zachovává normu: $\forall u\in V:\lVert{u}\rVert=\lVert{f(u)}\rVert$

31. větu o charakterizaci izometrie pomocí její matice. (8/10\)

    mějme prostory $V$ a $W$ s bázemi $B$ a $C$, pak $f:V \to W$ je bijektivní isometrie, právě když $_C[f]_{B}$ je unitární.

32. větu o ortogonalitě a prostorech určených maticí. (6/8\)

    pro $A \in \Bbb{R}^{m\times n}$ platí: $ker(A)=(R_A)^{\perp}$

33. větu o ortogonálním doplňku, mj. o jeho dimenzi. (6/12\)

    pro $U\Subset V$ platí: $(U^\perp)^\perp=U$ a $dim(U)+dim(U^\perp)=dim(V)$

34. větu o skalárním součinu dvou vektorů a Gramově matici. (8/8\)

    nechť $V$ je prostor s bází $B=(b_1,...,b_n)$, potom je **Gramova matice** $A$ definovaná $a_{ij}=\langle{b_i|b_j}\rangle$ a splňuje: $\forall u,v \in V:[v]_B^HA^T[u]_B$

35. tři pozorování o vlastnostech pozitivně definitních matic vzhledem k maticovým operacím. (6/9\)

    pro pozitivně definitní $A, B$ platí:
	1. $A+B$ je pozitivně definitní
	2. pro $R$ regulární je $R^HAR$ pozitivně definitní
	3. $A^{-1}$ je pozitivně definitní

36. tvrzení o pozitivní definitnosti blokové matice. (8/8\)

    $A, B$ jsou pozitivně definitní, právě když$\begin{pmatrix}A&O_{n,m}\\0_{m,n}&B\end{pmatrix}$ je pozitivně definitní

37. větu o třech ekvivalentních podmínkách pro pozitivně definitní matice. (6/9\)

	1. $A$ je pozitivně definitní
	2. $A$ má všechna vlastní čísla kladná
	3. existuje regulární $U$ taková, že $A=U^HU$

38. větu o Choleského rozkladu včetně správnosti algoritmu pro výpočet. (10/8\)

    pro každou pozitivně definitní matici $A$ exisuje **jednoznačná** horní trojúhelníková $U$ s kladnou diagonálou která splňuje $A=U^HU$ a nazývá se **Choleského rozklad**

39. větu o rekurentní podmínce pro pozitivně definitní matice. (10/8\)

    matice $A=\begin{pmatrix}a_{11}&b^H\\b&B\end{pmatrix}$ je pozitivně definitní, právě když $a^{11}\in \Bbb{R}^+$ a $B-\frac{bb^H}{a_{11}}$ je pozitivně definitní
	toto odpovídá gausově eliminaci kdy se pouze odčítá $\alpha$ násobek řádku od řádku pod ním

40. větu o pozitivně definitních maticích a determinantech. (8/10\)

    hermitovská matice $A$ řádu $n$ je pozitivně definitní, právě když matice $A_1,\dots,A_n$ mají kladné determinanty, kde $A_i$ se sestává z prvních $i$ řádků a sloupců $A$.
	$$
	\begin{matrix}
	\textcolor{red}{A_1}\\
	\textcolor{orange}{A_2}\\
	\textcolor{gold}{A_3}\\
	\end{matrix}
	\fcolorbox{gold}{white}{$
	\begin{matrix}
	\fcolorbox{orange}{white}{
	$\begin{matrix}
	\fcolorbox{red}{white}{a}&b\\
	d&f
	\end{matrix}$
	}&\begin{matrix}c\\g\end{matrix}\\
	\begin{matrix}h&&i\end{matrix}&j
	\end{matrix}$}
	$$

41. větu o diagonalizovatelnosti matic forem. (8/14\)

    Je-li $g$ kvadratická forma na vektorovém prostoru $V$ konečné dimenze nad tělesem $T$,  kde $char(T)\ne 2$, pak forma $g$ má diagonální matici vůči vhodné bázi $B$. (Věta platí i pro symetrické bilineární formy)

42. Sylvesterův zákon setrvačnosti — o diagonalizaci kvadratických forem. (10/14)

    každá kvadratická forma má vzhledem k vhodné bázi diagonální matici která má navíc na diagonále pouze $0,1$ a $-1$. navíc každá taková matice odpovídajcí stejné bázi má stejnou trojici $(\#1,\#-1,\#0)$, kde $\#$značí počet dotyčných čísel na diagonále. trojice je takzvaná signatura  

43. větu o počtu přímek svírajících stejný úhel. (6/8\)

	v $\Bbb{R}^d$ může maximálně ${d+1}\choose{2}$ přímek svírat stejný úhel.