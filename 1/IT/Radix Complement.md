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

47 - 13 = DRC( DRC(47) - 13 )
$$=DRC(52-13)$$