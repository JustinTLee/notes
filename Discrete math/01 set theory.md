# Set theory

---

## Table of Contents

01. [Sets](#sets)
02. [Sequences](#sequences)
03. [Regular expressions](#regular-expressions)
04. [Definitions](#definitions)
05. [Equations](#equations)
06. [Theorems](#theorems)
07. [Algorithms](#algorithms)
08. [References](#references)

---

## Sets

A **set** is a well-defined collection of **elements**. Elements that exist within a set are called **members**. 

* member order is not important
* each member is distinct.

Enumerating the contents of a set with $n$ members is represented by:

\begin{equation*}
S = {A_{1}, \dotso, A_{n}}
\end{equation*}

$x \in S$ defines that $x$ **is** a member of set $S$. $x \notin S$ defines that $x$ **is not** a member of set $S$.

We can specify a set by the properties that all the members have in common like so:

\begin{equation*}
S = \{x \: | \: P(x)\}
\end{equation*}

where $P(x)$ denotes a proposition concerning member $x$ where $P(x)$ is true.

---

The following are common sets:

* $Z^{+} = \{x \: | \: x \text{ is a positive integer}\}$
* $N = \{x \: | \: x \ge 0 \text{ and } x \text{ is an integer}\}$
* $Z = \{x \: | \: x \text{ is an integer}\}$
* $\mathbb{R} = \{x \: | \: x \text{ is real number}\}$
* $\emptyset$ has no elements ($S = \{\}$)

---

Two sets are **equal** if they have the same elements, written as:

\begin{equation*}
S_{1} = S_{2}
\end{equation*}

If every member of $A$ is also a member of $B$ ($x \in A$ and $x \in B$ for all x), then $A$ is a **subset** of $B$:

\begin{equation*}
A \subseteq B
\end{equation*}

Furthermore, $\emptyset \subseteq S$ at all times.

---

A set is **finite** if it has $n$ distinct elements. $n$ is called the **cardinality** of set $S$ and is denoted by $|S|$.

A **power set** is the set of all subsets of $S$ and is denoted by $P(S)$. If $|S| = n$, then $|P(S)| = 2^{n}$.

---

The **union** between two sets is defined as:

\begin{equation*}
S_{1} \cup S_{2} = \{x \: | \: x \in S_{1} \text{ or } x \in S_{2}\}
\end{equation*}

The union between $k$ sets can be written as $\bigcup_{i = 1}^{k} S_{i}$.

The **intersection** between two sets is defined as:

\begin{equation*}
S_{1} \cap S_{2} = \{x \: | \: x \in S_{1} \text{ and } x \in S_{2}\}
\end{equation*}

The union between $k$ sets can be written as $\bigcap_{i = 1}^{k} S_{i}$.

Two sets that have no common elements are called **disjoint** and can be represented as:

\begin{equation*}
S_{1} \cup S_{2} = \emptyset
\end{equation*}

The **complement** of two sets is defined as:

\begin{equation*}
S_{1} - S_{2} = \{x \: | \: x \in S_{1} \text{ and } x \notin S_{2}\}
\end{equation*}

The complement of a set compared to some universal set can be denoted as $\overline{S}$.

The **symmetric difference** between two sets are all the elements that belong to either one of the sets but not to both. It is represented by:

\begin{equation*}
S_{1} \oplus S_{2} = \{x \: | \: (x \in S_{1} \text{ and } x \notin S_{2}) \text{ or } (x \notin S_{1} \text{ and } x \in S_{2})\}
\end{equation*}

---

#### Theorem

The algebraic properties of sets are:

**Commutative**:

* $S_{1} \cup S_{2} = S_{2} \cup S_{1}$
* $S_{1} \cap S_{2} = S_{2} \cap S_{1}$

**Associative**:

* $S_{1} \cup (S_{2} \cup S_{3}) = (S_{1} \cup S_{2}) \cup S_{3}$
* $S_{1} \cap (S_{2} \cap S_{3}) = (S_{1} \cap S_{2}) \cap S_{3}$

**Distributive**:

* $S_{1} \cup (S_{2} \cap S_{3}) = (S_{1} \cap S_{2}) \cup (S_{1} \cap S_{3})$
* $S_{1} \cap (S_{2} \cup S_{3}) = (S_{1} \cup S_{2}) \cap (S_{1} \cup S_{3})$

**Idempotent**:

* $S_{1} \cup S_{1} = S_{1}$
* $S_{1} \cap S_{1} = S_{1}$

**Complement rules**:

* $\overline{(\overline{S_{1}})} = S_{1}$
* $S_{1} \cup \overline{S_{1}} = U$
* $S_{1} \cap \overline{S_{1}} = \emptyset$
* $\overline{\emptyset} = U$
* $\overline{U} = \emptyset$
* $\overline{S_{1} \cup S_{2}} = \overline{S_{1}} \cap \overline{S_{2}}$
* $\overline{S_{1} \cap S_{2}} = \overline{S_{1}} \cup \overline{S_{2}}$

**Universal rules**:

* $S_{1} \cup U = U$
* $S_{1} \cap U = S_{1}$

**Null rules**:

* $S_{1} \cup \emptyset = S_{1}$
* $S_{1} \cap \emptyset = \emptyset$

---

#### Theorem: addition principle

If two sets are disjoint, the cardinality of their union is:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}|
\end{equation*}

If two sets are not disjoint, the cardinality of their union is given by the **addition principle**:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}| - |S_{1} \cap S_{2}|
\end{equation*}

---

The **characteristic function** of a set is defined as:

\begin{equation*}
f_{S}(x) =
\begin{cases}
1 \quad \text{if } x \in S \\
0 \quad \text{if } x \notin S
\end{cases}
\end{equation*}

---

#### Theorem

Characteristic functions of subsets satify the following properties:

* $f_{S_{1} \cup S_{2}}(x) = f_{S_{1}}(x)f_{S_{2}}(x)$
* $f_{S_{1} \cap S_{2}}(x) = f_{S_{1}}(x) + f_{S_{2}}(x) - f_{S_{1}}(x)f_{S_{2}}(x)$
* $f_{S_{1} \oplus S_{2}}(x) = f_{S_{1}}(x) + f_{S_{2}}(x) - 2f_{S_{1}}(x)f_{S_{2}}(x)$

---

[(back to top)](#table-of-contents)

---

## Sequences

A **sequence** is a list of elements ordered by increasing value. The list may be finite or infinite. List items can be non-distinct. A general sequence can be written as $a_{1}, a_{2}, a_{3}, \dotsc$ or $(a_{i})_{1 \leq i < \infty}$.

A **countable** set is a set corresponding to all distinct elements in a sequence. The set $S^{*}$ consists of all finite sequences of the members of $S$. If the members of $S$ are symbols, $S^{*}$ is called an **alphabet**. Finite sequences in $S^{*}$ are called **strings**. $S^{*}$ includes the empty string $\Lambda$. The **catenation** of two strings is equivalent to:

\begin{equation*}
s \cdot w = \underbrace{s_{1}s_{2}s_{3}}_{\text{string #1}} \underbrace{w_{1}w_{2}w_{3}}_{\text{string #2}}
\end{equation*}

Catenation with the empty string is an identity:

* $s \cdot \Lambda = s$
* $\Lambda \cdot s = s$

---

#### Theorem: multiplication principle

If independent tasks $T_{i}$ for $i = 1, \dotsc, n$ are to be performed in sequence and each $T_{i}$ can be performed $N_{i}$ ways, then the sequence $T_{1}T_{2} \dotsc T_{n}$ can be performed $\prod_{i = 1}^{n} N_{i}$ ways.

---

For a set that is $|S| = n$, an arrangement of the members of S into a sequence of length $n$ is a **permutation** of S. For a sequence that is length $r$ taken from set $S$, it is known as a **permutation of $S$ taken $r$ at a time**.

---

#### Theorem: permutation

If $|S| = n$ and $1 \leq r \leq n$, then the number of permutations of $S$ taken $r$ at a time is:

\begin{equation*}
P_{r}^{n} = \frac{n!}{(n - r)!}
\end{equation*}

This formula is also known as a **permutation**.

---

#### Theorem: combination

If $|S| = n$ and $1 \leq 0 \leq n$, then the number of $r$-element subsets of $S$ is:

\begin{equation*}
C_{r}^{n} = \frac{n!}{r!(n - r)!}
\end{equation*}

This formula is also known as a **combination**.

---

[(back to top)](#table-of-contents)

---

## Regular expressions

A **regular expression** over set $S$ is a string constructed from the elements of $S$ and/or the following symbols:

* (
* )
* $\vee$
* $*$
* $\lambda$

The following are rules for regular expressions:

* the symbol $\lambda$ is a regular expression
* if $x \in S$ then $x$ is a regular expression
* if $\alpha$ and $\beta$ are regular expressions, then $\alpha\beta$ is a regular expression
* if $\alpha$ and $\beta$ are regular expressions, then $\alpha\vee\beta$ is a regular expression
* if $\alpha$ is a regular expression, then $(\alpha)^{*}$ is a regular expression

The set $S^{*}$ is called a **regular set** of $S$. 

---

#### Algorthim: computing a regular set

Computing a regular set involves the following algorithm:

1. Expression $\lambda$ corresponds to the set $\{\Lambda\}$
2. if $x \in S$, then the regular expression $x$ corresponds to set $\{x\}$
3. if $\alpha$ and $\beta$ are regular expressions corresponding to subsets $A$ and $B$ of $S^{*}$, then $\alpha\beta$ corresponds to $A \cdot B = \{s \cdot t \: | \: s \in A \text{ and } x \in B\}$
4. if $\alpha$ and $\beta$ are regular expressions corresponding to subsets $A$ and $B$ of $S^{*}$, then $\alpha\vee\beta$ corresponds to $A \cup B$
5. if $\alpha$ is a regular expression that corresponds to subset $A$ of $S^{*}$, then $(\alpha)^{*}$ corresponds to set $A^{*}$

---

[(back to top)](#table-of-contents)

---

## Definitions

* **set** - well-defined collection of elements
* **members** - elements that exist within a set
* **equal** - two sets that have the same elements, denoted by $=$
* **subset** - a set in which all members are also members of another set
* **finite** - a set with $n$ distinct elements
* **cardinality** - the number of distinct elements within a finite set, denoted by $|S|$
* **power set** - set of all subsets of $S$, denoted by $P(S)$
* **union** - a set that contains all of the elements of two or more other sets
* **intersection** - a set that contains all of the common elements of two or more other sets
* **disjoint** - two or more sets that share no elements in common
* **complement** - the elements in one set but not in another set being compared to
* **symmetric difference** - the non-common elements between two or more sets
* **sequence** - a list of elements ordered by increasing value
* **countable set** - set corresponding to all distinct elements in a sequence
* **alphabet** - a set of symbols
* **strings** - finite sequences of members of a set, where the members are symbols
* **catenation** - the writing of two or more strings adjacently
* **permutation** - an arragement of members of a set into a sequence
* **regular expression** - a string constructed from the elements of a set and a subclass of symbols

---

[(back to top)](#table-of-contents)

---

## Equations

#### Cardinality of power set:

\begin{equation*}
|P(S)| = 2^{n}
\end{equation*}

#### Addition principle of disjoint sets:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}|
\end{equation*}

#### Addition principle of non-disjoint sets:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}| - |S_{1} \cap S_{2}|
\end{equation*}

#### Characteristic function:

\begin{equation*}
f_{S}(x) =
\begin{cases}
1 \quad \text{if } x \in S \\
0 \quad \text{if } x \notin S
\end{cases}
\end{equation*}

#### Permutation:

\begin{equation*}
P_{r}^{n} = \frac{n!}{(n - r)!}
\end{equation*}

#### Combination:

\begin{equation*}
C_{r}^{n} = \frac{n!}{r!(n - r)!}
\end{equation*}

---

[(back to top)](#table-of-contents)

---

## Theorems

#### _Theorem 01.01 (**Sets**)_:

The algebraic properties of sets are:

* **Commutative**: 
	* $S_{1} \cup S_{2} = S_{2} \cup S_{1}$
	* $S_{1} \cap S_{2} = S_{2} \cap S_{1}$
* **Associative**: 
	* $S_{1} \cup (S_{2} \cup S_{3}) = (S_{1} \cup S_{2}) \cup S_{3}$
	* $S_{1} \cap (S_{2} \cap S_{3}) = (S_{1} \cap S_{2}) \cap S_{3}$
* **Distributive**:
	* $S_{1} \cup (S_{2} \cap S_{3}) = (S_{1} \cap S_{2}) \cup (S_{1} \cap S_{3})$
	* $S_{1} \cap (S_{2} \cup S_{3}) = (S_{1} \cup S_{2}) \cap (S_{1} \cup S_{3})$
* **Idempotent**:
	* $S_{1} \cup S_{1} = S_{1}$
	* $S_{1} \cap S_{1} = S_{1}$
* **Complement rules**:
	* $\overline{(\overline{S_{1}})} = S_{1}$
	* $S_{1} \cup \overline{S_{1}} = U$
	* $S_{1} \cap \overline{S_{1}} = \emptyset$
	* $\overline{\emptyset} = U$
	* $\overline{U} = \emptyset$
	* $\overline{S_{1} \cup S_{2}} = \overline{S_{1}} \cap \overline{S_{2}}$
	* $\overline{S_{1} \cap S_{2}} = \overline{S_{1}} \cup \overline{S_{2}}$
	* $S_{1} \cup U = U$
	* $S_{1} \cap U = S_{1}$
* **Null rules**:
	* $S_{1} \cup \emptyset = S_{1}$
	* $S_{1} \cap \emptyset = \emptyset$

#### _Theorem 01.02 (**Sets - addition principle**)_:

If two sets are disjoint, the cardinality of their union is:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}|
\end{equation*}

If two sets are not disjoint, the cardinality of their union is given by the **addition principle**:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}| - |S_{1} \cap S_{2}|
\end{equation*}

#### _Theorem 01.03 (**Sets**)_:

Characteristic functions of subsets satify the following properties:

* $f_{S_{1} \cup S_{2}}(x) = f_{S_{1}}(x)f_{S_{2}}(x)$
* $f_{S_{1} \cap S_{2}}(x) = f_{S_{1}}(x) + f_{S_{2}}(x) - f_{S_{1}}(x)f_{S_{2}}(x)$
* $f_{S_{1} \oplus S_{2}}(x) = f_{S_{1}}(x) + f_{S_{2}}(x) - 2f_{S_{1}}(x)f_{S_{2}}(x)$

#### _Theorem 01.04 (**Sequences - multiplication principle**)_:

If independent tasks $T_{i}$ for $i = 1, \dotsc, n$ are to be performed in sequence and each $T_{i}$ can be performed $N_{i}$ ways, then the sequence $T_{1}T_{2} \dotsc T_{n}$ can be performed $\prod_{i = 1}^{n} N_{i}$ ways.

#### _Theorem 01.05 (**Sequences - permutation**)_:

If $|S| = n$ and $1 \leq r \leq n$, then the number of permutations of $S$ taken $r$ at a time is:

\begin{equation*}
P_{r}^{n} = \frac{n!}{(n - r)!}
\end{equation*}

#### _Theorem 01.06 (**Sequences - combination**)_:

If $|S| = n$ and $1 \leq 0 \leq n$, then the number of $r$-element subsets of $S$ is:

\begin{equation*}
C_{r}^{n} = \frac{n!}{r!(n - r)!}
\end{equation*}

---

[(back to top)](#table-of-contents)

---

## Algorithms

#### Computing a regular set

1. Expression $\lambda$ corresponds to the set $\{\Lambda\}$
2. if $x \in S$, then the regular expression $x$ corresponds to set $\{x\}$
3. if $\alpha$ and $\beta$ are regular expressions corresponding to subsets $A$ and $B$ of $S^{*}$, then $\alpha\beta$ corresponds to $A \cdot B = \{s \cdot t \: | \: s \in A \text{ and } x \in B\}$
4. if $\alpha$ and $\beta$ are regular expressions corresponding to subsets $A$ and $B$ of $S^{*}$, then $\alpha\vee\beta$ corresponds to $A \cup B$
5. if $\alpha$ is a regular expression that corresponds to subset $A$ of $S^{*}$, then $(\alpha)^{*}$ corresponds to set $A^{*}$

---

[(back to top)](#table-of-contents)

---

## References

---

[(back to top)](#table-of-contents)

---