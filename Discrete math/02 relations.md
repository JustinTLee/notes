# Relations

---

## Table of Contents

01. [Relations](#relations)
02. [Digraphs](#digraphs)
03. [Paths](#paths)

---

## Relations

* **relation** from a set $A$ to set $B$ is subset of $A \times B$
    * each element of $A \times B$ represented by ordered pair $(a, b)$
* if $R \subseteq A \times B$ and $(a, b) \in R$, then $a$ is related to $b$ by $R$

<br/>

* $a$ being related to $b$ by $R$: $a \, \text{R} \, b$
* $a$ not being related to $b$ by $R$: $a \, \not{\text{R}} \, b$.

<br/>

* **domain** of $R$ ($\text{dom}\{R\}$) is set of elements in $A$ which are related to an element in $B$
* **range** of $R$ ($\text{range}\{R\}$) is set of elements in $B$ which form an ordered pair with an element in $A$.

<br/>

* $R$ represented by $m \times n$ matrix $\textbf{M}_{\textbf{R}}$:

\begin{equation*}
m_{ij} =
\begin{cases}
1 \quad \text{if } (a_{i}, b_{i}) \in R \\
0 \quad \text{if } (a_{i}, b_{i}) \notin R \\
\end{cases}
\end{equation*}

---

[(back to top)](#table-of-contents)

---

### Digraphs

* a relation matrix can be represented by a **directed graph** (**digraph**)
    * elements of $A$ and $B$ are vertices
    * an edge from one vertex to another (with an arrow indicating direction) exists only if $m_{ij} = 1$
* **in-degree** of a vertex $a$ is amount of directed edges leading to $a$
* **out-degree** of a vertex $a$ is amount of directed edges coming out of $a$


<br/>

* the following produces the digraph below:

\begin{equation*}
A = \{1, 2, 3, 4\}
\end{equation*}
\begin{equation*}
R = \{(1, 1), (1, 2), (2, 1), (2, 2), (2, 3), (2, 4), (3, 4), (4, 1)\}
\end{equation*}

![](./images/digraph example.png)

<br/>

* **restriction of $R$ to $B$** is $R \cup B \times B$ when $B \subseteq A$

---

[(back to top)](#table-of-contents)

---

### Paths

* a path of length n from elements $a$ to $b$ in set $A$ is such that:

\begin{equation*}
a \, R \, x_{1}, x_{1} \, R \, x_{2}, \dots, x_{n - 1} \, R \, b
\end{equation*}

* paths are not necessarily distinct
    * follows the directions of arrows in digraphs
* paths that begin and end at same vertex called **cycles**
    * 1 to 2 to 3 to 4 is a cycle:

![](./images/digraph example.png)

* $a \, R^{n} \, b$ represents path of length $n$ from $a$ to $b$ in $R$
    * $a \, R^{\infty} \, b$ means that there exists some path that will eventually lead $a$ to $b$

<br/>

* given that $\textbf{M}_{\textbf{R}} = [m_{ij}]$ represents the relation matrix of $R$
    * $m_{ij} = 1$ if $a_{i} \, R \, a_{j}$ exists
    * $R^{n}$ is represented by $\textbf{M}_{\textbf{R}}^{n}$

<br/>

#### Theorem: traversing digraph using matrices

For $n \ge 1$:

\begin{equation*}
\textbf{M}_{\textbf{R}^{\textbf{n}}} = \textbf{M}_{\textbf{R}}^{n}
\end{equation*}

where $R$ is a relation on set $A$.

**End theorem.**

<br/>

* **reachability** ($R^{*}$) means that either:
    * $x \, R^{*} \, y$
    * $x = y$
* given $\pi_{1} = a, x_{1}, \dots, x_{n - 1}, b$ and $\pi_{2} = b, y_{1}, \dots, y_{m - 1}, c$, the **composition** of $\pi_{1}$ and $\pi_{2}$ is:

\begin{equation*}
a, x_{1}, \dots, x_{n - 1}, b, y_{1}, \dots, y_{m - 1}, c
\end{equation*}

* where the path is of length $n + m$

<br/>

* **inverse path** is a path defined in reverse:

\begin{equation*}
\pi^{-1} = b, x_{n - 1}, \dots, x_{1}, a
\end{equation*}

* inverse path may not be in $R$, given $R$ is digraph

---

[(back to top)](#table-of-contents)

---