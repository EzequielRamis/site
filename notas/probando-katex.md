---
title: Probando KaTeX
date: 2021-09-05
layout: layouts/post.njk
---

Para ver qué tan lindo se ve LaTeX en la web, vamos a probar por **Inducción** la siguiente proposición $p$.

Sea $n\in\N$, vale:

$$
p(n):\sum_{k=1}^n k=\frac{n(n + 1)}{2}
$$

Antes que nada vamos a ver cómo se comporta con algunos ejemplos:

$$
\begin{array}{l}
\begin{split}
 \bullet\; n=4\implies &\sum_{k=1}^{4} k=1+2+3+4=10\\\\
  \iff&\frac{4\cdot5}{2}=\frac{20}{2}=10\quad\checkmark
\end{split}\\\\
\begin{split}
 \bullet\; n=11\implies &\sum_{k=1}^{11} k=1+2+...+11=66\\\\
  \iff&\frac{11\cdot12}{2}=\frac{132}{2}=66\quad\checkmark
\end{split}\\\\
\begin{split}
 \bullet\; n=100\implies &\sum_{k=1}^{100} k=1+2+...+100=5050\\\\
  \iff&\frac{100\cdot101}{2}=\frac{10100}{2}=5050\quad\checkmark
\end{split}
\end{array}
$$

Luego, como estamos utilizando Inducción, lo primero que se tiene que hacer es probar que el **Caso Base** sea verdadero; en este caso $p(1)$.

- **Caso Base**:

$$
\begin{split}
p(1):& \sum_{k=1}^1 k=\frac{1(1 + 1)}{2}\\\\
\iff & 1 = \frac{2}{2}\\\\
\iff & 1 = 1\quad\checkmark
\end{split}
$$

$\therefore\; p(1)\; V$

Ahora, hay que hacer el **Paso Inductivo**.

- **Paso Inductivo**:

Dado $h\in\N,\; ¿p(h)\; V \implies p(h+1)\; V?$

Dicho de otra forma, si $\forall h\in\N$, $p(h)$ es Verdadera, ¿implica que $p(h+1)$ también sea Verdadera?

Sabemos que nuestra **Hipótesis Inductiva** es $p(h)$

$$
HI: \sum_{k=1}^h k=\frac{h(h + 1)}{2}
$$

y queremos probar $p(h + 1):$

$$
\begin{split}
& \sum_{k=1}^{h + 1} k=\frac{(h + 1)(h + 2)}{2}\\\\
\iff & h + 1 + \sum_{k=1}^{h} k=\frac{(h + 1)(h + 2)}{2}\\\\
\underset{\text{por HI}}{\iff} & h + 1 + \frac{h(h + 1)}{2}=\frac{(h+1)(h+2)}{2}\\\\
\iff & 2h + 2 + h(h + 1) = (h+1)(h+2)\\\\
\iff & 2h + 2 + h^2 + h = h^2 + 3h +2\\\\
\iff & h^2 + 3h + 2 = h^2 + 3h +2\\\\
\iff & 0=0\quad\checkmark
\end{split}
$$

$\therefore\; p(h)\; V \implies p(h+1)\; V$

Es decir, $p(n)$ es Verdadera.$\quad\blacksquare$
