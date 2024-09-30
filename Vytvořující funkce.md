# Vytvořující funkce
Obyčejnou vytvořující funkcí posloupnosti $\{a_n\}_{n=0}^\infty$ rozumíme algebraický výraz (formální mocninou řadu, respektive jakýkoliv výraz s ním ekvivalentní).

$$
f(x) = \sum_{n=0}^\infty a_n x^n
$$
Tedy:
$$
a_0 + a_1 x + a_2 x^2 + ... + a_n x^n + ...
$$

Příklad:
$$
a_n = (\frac{2}{3})^n
$$
Geometrická posloupnost:
$$
f(x) = \sum_{n=0}^\infty x^n = \frac{3}{3-2x}
$$

## f(x) může mít tvary:
### formální mocninná řada
$$
a_0 + a_1 x + a_2 x^2 + ... + a_n x^n + ...
$$
Vidíme tvar jednotlivých členů posloupnost.

### uzavřený tvar vytvořující funkce
Konečný výraz.

## Postup řešení
$$
\{a_n\} ... f(x) = \sum a_n x^n
$$
1. Máme otevřený tvar.
2. Hledáme uzavřený tvar $f(x)$.
Manipulace s funkcemi.
2. Nový uzavřená tvar $g(x)$.
3. Otevřený tvar $g(x) -> {b_n}$.

Přechod mezi těmi to stavy jsou úlohy které můžeme řešit.

Existuje vzájemně jednoznačný vztah mezi posloupností a její vytvořující funkcí. 

[[Derivace|Zderivujeme]]:
- $a_0 = f(0)$
- $a_1 = dx f(0)$
- $a_2 = \frac{dx^2}{2} f(0)$

$$
a_n = \frac{dx^n}{n!} f(0)$
$$
## Převod mezi stavy
Otevřený <-> uzavřený tvar

Geometrická posloupnost:
$$
{q^n}_{n=0}^\infty = \frac{1}{1-qx}
$$
Kombinační číslo (binomický koeficient):
$$
{C_n^k}_{k=0}^\infty = (1+x)^n
$$
- $n \in Z$

TODO: napiš n nad k
$C_n^k = \left(n k\right)$

$$
\left\{\frac{q^n}{n!}\right\} = e^{qx}
$$

Velmi často bude uzavřený tvar vytvořující funkce:

$$
f(x) = \frac{P(x)}{Q(x)}
$$
Kde:
- $P(x), Q(x)$ jsou polynomy.

Rozklad na parciální zlomky.

