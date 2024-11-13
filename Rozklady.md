# Rozklady

![[Třídy rozkladu množiny]]

n - objektů (prvků) rozdělujeme (rozkládáme) do tříd (skupin).

Objekty mohou být:
- nerozlišitelné,
- rozlišitelné.

Třídy mohou být:
- nerozlišitelné,
- rozlišitelné.

## Úlohy
### N nerozlišitelných objektů do rozlišitelných tříd
[[Diofantická rovnice příklad]]

> [!tip]
Počet rozkladů $n$ nerozlišitelných objektů do k rozlišitelných tříd. Třída může zůstat prázdná. Je roven počtu celočíselných řešení diofantické rovnice $x_1 + ... + x_k = n$.
- $\forall i \; x_i \in N$

- $x_i$ - počet prvků v $i$-té třídě 

Dvě různá řešení:
(1,0,...,n-1)
(n-1,0,...,1)

Bitové řetězce:
$x_1 + x_2 + ... + x_k = n$

Místo každého $+$ (oddělovače) dáme $0$.
$x_1 0 x_2 0 ... 0 x_k = n$
Místo počtu prvků v jednotlivých rozkladech umísťujeme $1$.
Do každé přihrádky dáme tolik jedniček, kolik je tam prvků. 

Počet $0,1$:
- $n*1$
- $(k-1)*0$


$$
P(n,k-1) = C_{n+k-1}^{k-1}
$$
### N nerozlišitelných objektů rozkládáme do k tříd, v i-té třídě je alespoň $a_i$ objektů.

$$
x_1 + x_2 + ... + x_k = n
$$
- $0 \leq a_i \leq x_i$

Odpovídá počtu řešení diofantické rovnice.

$$
\sum_{i=1}^k a_i \leq n
$$
Převod na binární řetězce:
- Přihrádky: $(k-1)*0$
- Zbude po povinném naplnění skupin: $(n - \sum_{i=1}^k a_i) * 1$

$$
P\left(k-1, n-\sum_{i=1}^k a_i\right) = C_{n+k-1-\sum_{i=1}^k a_i}^{k-1}
$$

### N nerozlišitelných objektů rozkládáme do k rozlišitelných tříd, v i-té tříde je alespoň $a_i$ a nejvýše $b_i$ objektů
- $0 \leq a_i \leq b_i \leq x_i$

$$
\sum_{i=1}^k a_i \leq n
$$Odpovídá počtu řešení diofantické rovnice.

$$
x_1 + x_2 + ... + x_k = n
$$
- $\forall i (0 \leq) a_i \leq x_i \leq b_i$

Komplikuje nám to horní mez.
Řešíme pomocí: princip inkluze a exkluze

1. Převedeme úlohu do standardizovaného tvaru.

Odečteme $a_i$

$$
0 \leq x_i - a_o \leq b_i - a_i
$$
$$
0 \leq y_i \leq c_i
$$
$y_1 + ... + y_k = m$
- $\forall i \; 0 \leq y_i \leq c_i$
- $m = n - \sum_{i=1}^k a_i$

Počáteční podmínky:
- $\alpha_1: c_1+1 \leq y_1$
- $\alpha_2: c_2+1 \leq y_2$
- ...
- $\alpha_k: c_k+1 \leq y_k$
$$
N(\bar \alpha_1, \bar \alpha_2, ..., \bar \alpha_k) =
N - 
\sum_{i=1}^k N(\alpha_i) + 
\sum_{i\leq i_1 \leq k} N(\alpha_{i_2}, \alpha_{i_2}) -
\sum_{i\leq i_1 \leq i_2\leq i_3\leq n}^k N(\alpha_i) + 
... +
(-1)^k N(\alpha_1, \alpha_2, ..., \alpha_k)
$$


$N =P(k-1,n)$
$N(\alpha_i) = P(k-1,n-(c_i+1))$
$N(\alpha_{i_1}, \alpha_{i_2}) = P(k-1,n-(c_{i_1}+1)-(c_{i_2}+1))$
...
$N(\alpha_{i_1}, \alpha_{i_2}, \alpha_k) = P(k-1,n-\sum _ {i=1} ^k c_i -k)$

## Řešení těchto úloh pomocí: vytvořujících funkcí
$$
x_1 + x_2 + ... + x_k = n
$$
$(1+x+x^2+...)$

Konvoluce:
$$
f(x) = (1+x+x^2+...)^k
$$

Uzavřený tvar:
$$
\frac{1}{1-x}
$$

$$
f(x) = \frac{1}{(1-x)^k} = (1-x)^{-k}
$$

Když:
$a_i \leq x_i$

Změna:
$$
f(x) = \prod_{i=1}^k (x^{a_i}+x^{a_i+1}+...)
$$
$$
f(x) = \frac{x^{\sum_{i=1}^k a_i}}{(1-x)^k} = x^{\sum_{i=1}^k a_i} a_i (1-x)^{-k}
$$

Když:
$a_i \leq x_i \leq b_i$

$$
f(x) = \prod_{i=1}^k (x^{a_i}+x^{a_i+1}+...+x^{b_i})
$$
$$
f(x) = \prod_{i=1}^k x^{a_i}(1+x+...+x^{b_i-a_i})
$$

$$
\frac
{1-x^{b_i-a_i+1}}
{1-x}
$$

## N nerozlišitelných objektů rozkládáme do nerozlišitelných tříd

> [!tip]
Počet rozkladů n nerozlišitelných rozkladů objektů do nerozlišitelných tříd (všechny možnosti možných počtů tříd) je roven:
- Počtu rozkladů přirozeného čísla n na kladné sčítance.
- Počtu řešení diofantické rovnice $x_1 + 2x_2 + ... nx_n = n$.
	- $\forall i \; x_i \in N$
- Počet rozkladů přirozeného čísla $n$ na sčítance rovné některým z čísel $a_1,...,a_k$ (předepisujeme počty prvků v jednotlivých třídách, předepisujeme velikosti sčítanců)

$n = 1 + ... + 1$
Sčítání je komutativní:
$1+2 = 2 +1$

> [!note] Sčítance budeme vypisovat od nejmenšího po největší.

- $x_i$ - počet sčítanců velikosti i (počet skupin velikosti i)


Počet řešení diofantické rovnice
$$
a_1x_1 + ... + a_kx_k = n
$$
- $\forall i \; x_i \in N$

n = 353
a_1 = 12
a_2 = 33
a_3 = 42

Nelze vyřešit tuto diofantickou rovnici.
Podmínka:
$NSD(a_1,...,a_k) | n$