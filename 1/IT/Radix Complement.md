for a $n$ digit number $y$, $RC=b^n-y$.

RC(0005) = 9995
RC(9945) = 0055
# Diminished Radix Complement
The diminished radix complement of a number $y$ in radix $b$ is, by definition, $(b^n-1)-y$.

This means instead of 100 - $y$, it is 99 - $y$, so we **never have to borrow.**
In radix 10, $DRC(x)=10^n-1-x$
	and $DRC( DRC(x) )=x$

A - B = D
B - A = -D
DRC(B-A) = DRC(-D)
$10^n-1-(B-A)=10^n-1+D$
...

$$\begin{align} \\
47 - 13 &= DRC( DRC(47) + 13 ) \\
&=DRC(52+13) \\
&=DRC(65) \\
&=34 \\
\end{align}$$
000000 - 1 = 999999
000047 + 999999 = 000043
6-digit binary computer:
111 111 = -1

---
# Negative Binary Numbers
Convention: reserve MSB (Most Significant Bit) as "sign bit"

Highest 6 digit positive val we can have is **0**11111 ($31_{10}$)
Lowest 6 digit negative binary number is **1**00000 ($-32_{10}$)
