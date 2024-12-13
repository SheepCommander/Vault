for $x^n$:
$$\frac{d}{dx}ax^n=a*nx^{n-1}$$
sin
cos
-sin
-cos
$$
\begin{align} f'(x) &= \lim_{h \to 0} \dfrac{f(x + h) - f(x)}{h} \\
&= \lim_{h \rightarrow 0} \dfrac{a^{x + h} - a^x}{h} \\
&= \lim_{h \rightarrow 0} \dfrac{a^x a^h - a^x}{h}\\ &= \lim_{h \rightarrow 0} \dfrac{a^x \big(a^h - 1\big)}{h}. \end{align}
$$
$$f'(x) = a^x \displaystyle \lim_{h \rightarrow 0} \dfrac{a^h -1}{h}$$
$$f(x) = a^x = \big(e^{\ln{a}}\big)^x = e^{x \ln{a}}$$
$$f'(x) = e^{x \ln{a}} (\ln{a})= a^x \ln{a}$$
$$
\boxed{\frac{d}{dx} (e^x) = e^x}
\boxed{\frac{d}{dx} (a^x) = a^x \ln a}
$$







Equ of tangent line: $(x,y)=(c,f(c))$
$y=mx+b=f'(c)*(x-c)=f(c)$











---
When you find the derivative, you're really finding the instantaneous slope of the original function. 
Or in other words, you're finding the slope of the *tangent* line at a point on the original graph.

You can first approximate the tangent using two secant lines, making $a$ smaller and smaller.
$$
AROC=\frac{f(a+h)-f(a)}{(a+h)-a}
$$
This finds the slope of a secant line, representing the **average rate of change** over the interval $[a,a+h]$.

The **instantaneous rate of change** for $f$ at $a$ where $h$ represents the change from $a$ to $a+h$ is:
$$
f'=IROC=\lim_{h \to 0}\frac{f(x+h)-f(a)}{h}
$$


---
$$\lim_{x\to c}\frac{f(x)-f(c)}{x-c}$$
$\Delta x$ form
$$\lim_{x\to \Delta x}\frac{f(x+\Delta x)-f(x)}{\Delta x}$$
**forward difference** quotient
$$\lim_{h\to 0}\frac{f(x+h)-f(x)}{h}$$
**backward difference** quotient
$$\lim_{h\to 0}\frac{f(x)-f(x-h)}{h}$$
**symmetric difference** quotient
$$\lim_{h\to 0}\frac{f(x+h)-f(x-h)}{2h}$$
