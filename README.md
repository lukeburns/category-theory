# Category Theory

I'm learning category theory by trying to explain it. This is a work in progress. Please [open an issue](https://github.com/lukeburns/category-theory/issues) or [fork and submit a pull request](https://github.com/lukeburns/category-theory/pulls) if you find a mistake.

## What is category theory, and how do I use it?

Category theory is a mathematical language that formalizes the notion of process. Anytime you want to talk about processes with input and output, category theory will be useful.

A category $C$ consists of:

1. a collection of **objects** denoted $\text{Ob}(C)$. If $X$ is an object of $C$, then write $X \in C$.
2. for every pair of of objects $(X, Y)$, a set of **processes** (or usually "morphisms") $\text{Proc}(X, Y)$ that transform $X$ into $Y$. If $f \in \text{Proc}(X, Y)$, then write $f : X \to Y$;

with the following rules that ensure processes actually behave like processes with objects as inputs and outputs:

- for processes $f : X \to Y$ and $g : Y \to Z$, there is a process $gf : X \to Z$ (read "$g$ after $f$" or "g composed with f"),
- for every object $X$, there is a process that does nothing $1_X : X \to X$ called the **identity** of $X$ such that $f = f 1_X$ and $f = 1_Y f$ for any process $f : X \to Y$,
- $hgf = (hg)f = h(gf)$ if the objects of inputs and outputs are compatible.

Processes are prevalent. When programmers program, physicists do physics, and mathematicians do math, they are trying to describe or engineer processes. 

You can use category theory to talk about other mathematical languages and dig up relationships between them. You can even use categories to talk about categories.

My goal here is to show you how to use category theory, so let's start with some examples.