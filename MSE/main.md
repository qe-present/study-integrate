# 题目来源

[integration - Laplace transform of $\int_{0}^\infty\frac{e^{-t}\sin^2t}{t}dt$ - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1846789/laplace-transform-of-int-0-infty-frace-t-sin2ttdt?noredirect=1)

# 题目

$$
{\large
\bbox[#EEF, 20px, border: 2px solid red]{\color{blue}{ {\large  \,\, 
I=\int\limits_0^{+\infty}{\frac{e^{-t}\sin ^2t}{t}}dt
} } }}   \\
$$

## 解法一

因为
$$
\sin^2{t}=\frac{1-\cos{2t}}{2}
$$
同时考虑到1的拉普拉斯变换
$$
\color{blue}{
\int\limits_0^{+\infty}{e^{-tx}}dt=\frac{1}{t}
}
$$
原式为
$$
\large{
\begin{align} 
I&=\int\limits_0^{\infty}{e^{-t}}\frac{1-\cos 2t}{2}\int\limits_0^{\infty}{e^{-tx}dx}dt
\\
&=\frac{1}{2}\int\limits_0^{\infty}{\int\limits_0^{\infty}{e^{-t\left( 1+x \right)}\left( 1-\cos 2t \right) dx}}dt
\\
&=\frac{1}{2}\int\limits_0^{\infty}{\int\limits_0^{\infty}{e^{-t\left( 1+x \right)}-e^{-t\left( 1+x \right)}\cos 2tdx}}dt\,\,
\\
&=\frac{1}{2}\int\limits_0^{\infty}{\int\limits_0^{\infty}{e^{-t\left( 1+x \right)}-e^{-t\left( 1+x \right)}\mathrm{Re}e^{-2ti}dx}}dt
\\
&=\frac{1}{2}\int\limits_0^{\infty}{\int\limits_0^{\infty}{e^{-t\left( 1+x \right)}-\mathrm{Re}e^{-t\left( 1+x \right) -2ti}dx}}dt
\\
&=\frac{1}{2}\int\limits_0^{\infty}{\int\limits_0^{\infty}{e^{-t\left( 1+x \right)}-\mathrm{Re}e^{-t\left( 1+x+2i \right)}dx}}dt
\\
&=\frac{1}{2}\mathrm{Re}\int\limits_0^{\infty}{\int\limits_0^{\infty}{e^{-t\left( 1+x \right)}-e^{-t\left( 1+x+2i \right)}dx}}dt   
 \end{align} 
 }

$$
**去实部**
$$
\large{
\cos2t=\Re e^{-2ti}
}
$$
**交换积分次序**
$$
\color{blue}{
\begin{align}
I &= \frac{1}{2}\mathrm{Re}\int\limits_0^{\infty}{\int\limits_0^{\infty}{e^{-t\left( 1+x \right)}-e^{-t\left( 1+x+2i \right)}dx}}dt \\
&= \frac{1}{2}\mathrm{Re}\int\limits_0^{\infty}{\frac{1}{1+x}-\frac{1}{1+x+2i}}dx \\
&= \frac{1}{2}\mathrm{Re}\ln \left( \frac{1+x}{1+x+2i} \right) \mid_{x=0}^{x=\infty} \\
&= \frac{1}{2}\mathrm{Re}\left( 0-\left( \ln \left( \frac{1}{1+2i} \right) \right) \right) \\
&= \frac{1}{2}\Re \ln \left( 1+2i \right) \\
&= \frac{1}{2}\ln \left( \sqrt{1^2+2^2} \right) \\
&= \frac{\ln 5}{4}
\end{align}
}
$$

## 解法2