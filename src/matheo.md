# Master-Theorem
Die Rekursion  
$T(n)=aT({n \over b})+cn^k$  
$T(1)=c$  
für Konstante $a,b,c$ und $k$ mit $a\geq 1$ und $b>1$ hat die Laufzeit  
$T(n)\in\begin{cases}
\Theta(n^k)&\text{wenn }a<b^k\\
\Theta(n^k\log n)&\text{wenn }a=b^k\\
\Theta(n^{\log_ba})&\text{wenn }a>b^k\\
\end{cases}$

# Master-Theorem (nach Brinkmeier)
Seien $a\geq 1$ und $b>1$ Konstanten, $f(n)$ eine Funktion und sei $T(n)$ auf den nicht-negativen ganzen Zahlen definiert durch:  
$T(n)=a*T({n \over b})+f(n)$,  
wobei ${n \over b}$ entweder $\lfloor{n \over b}\rfloor$ oder $\lceil{n \over b}\rceil$ ist.

1.  Gilt $f(n)\in\mathcal O(n^d)$ mit $d=\log_b a-\epsilon$ für $\epsilon>0$, dann ist  
    $T(n)\in\Theta(n^{log_ba})$
2.  Gilt $f(n)\in\mathcal O(n^d)$ mit $d=\log_b a$, dann ist  
    $T(n)\in\Theta(n^d\log(n))$
3.  Gilt $f(n)\in\Omega(n^d)$ mit $d=\log_b a+\epsilon$ für $\epsilon>0$, und ist $af({n \over b})\leq cf(n)$ für eine Konstante $c<1$ und alle hinreichend großen $n$, dann ist  
    $T(n)\in\Theta(f(n))$