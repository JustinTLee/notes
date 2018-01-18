# Set theory

---

## Table of Contents

01. [Relations](#relations)
02. [Digraphs](#digraphs)

---

## Relations

A **relation** from a set $A$ to set $B$ is a subset of $A \times B$. If $R \subseteq A \times B$ and $(a, b) \in R$, then $a$ is related to $b$ by $R$.

$a$ being related to $b$ by $R$ is written as $a \, \text{R} \, b$. <br/> $a$ not being related to $b$ by $R$ is written as $a \, \not{\text{R}} \, b$.

The **domain** of $R$ ($\text{dom}\{R\}$) is the set of elements in $A$ which are related to an element in $B$. The **range** of $R$ ($\text{range}\{R\}$) is the set of elements in $B$ which form an ordered pair with an element in $A$.

---

$R$ can be represented by the $m \times n$ matrix $\textbf{M}_{\textbf{R}}$, defined as:

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

A relation matrix can be represented by a graph. The elements of $A$ and $B$ are vertices. An edge from one vertex to another (with an arrow indicating direction) exists only if $m_{ij} = 1$. This is known as a **directed graph** (**digraph**).

The **in-degree** of a vertex $a$ is the amount of directed edges leading to $a$. The **out-degree** of a vertex $a$ is the amount of directed edges coming out of $a$.

---

The **restriction of $R$ to $B$** is $R \cup B \times B$ when $B \subseteq A$.

---

[(back to top)](#table-of-contents)

---