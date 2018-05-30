# Logic circuits

## 1 Logic functions

* binary values take on two forms: $\{0, 1\}$
* binary logic functions have:
    * $\ge 1$ binary inputs
    * $1$ binary output
* a logic expression is of the form $L \left( x \right)$

* $3$ basic binary operators are:
    * AND
    * OR
    * NOT

---

### 1.1 AND operator

$$
L \left( x_{1}, x_{2} \right) = x_{1} \cdot x_{2}
$$

#### 1.1.1 AND truth table

$x_{1}$|$x_{2}$|$L\left( x_{1}, x_{2} \right)$
:---:|:---:|:---:
$0$|$0$|$0$
$0$|$1$|$0$
$1$|$0$|$0$
$1$|$1$|$1$

#### 1.1.2 AND diagram

* AND can be represented as switches in series:

<!-- image -->

#### 1.1.3 AND logic gate symbol

<!-- image -->

---

### 1.2 OR operator

$$
L \left( x_{1}, x_{2} \right) = x_{1} + x_{2}
$$

#### 1.2.1 OR truth table

$x_{1}$ | $x_{2}$ | $L\left( x_{1}, x_{2} \right)$
:---:|:---:|:---:
$0$|$0$|$0$
$0$|$1$|$1$
$1$|$0$|$1$
$1$|$1$|$1$

#### 1.2.2 OR diagram

* OR can be represented as switches in parallel:

<!-- image -->

#### 1.2.3 OR logic gate symbol

<!-- image -->

---

### 1.3 NOT operator

$$
L \left( x \right) = \bar{x}
$$

#### 1.3.1 NOT truth table

$x$|L\left( x \right)
:---:|:---:
$0$|$0$
$1$|$0$

#### 1.3.2 NOT diagram

* NOT can be represented as a resistor in series with a switch:

<!-- image -->

#### 1.3.3 NOT logic gate symbol

<!-- image -->

---

* circuit built out of logic gates called **logic network**
* engineers perform:
    * **analysis** - determining behavior of logic networks
    * **synthesis** - creating new logic networks

</br>
</br>

---

</br>
</br>

## 2 NAND and NOR logic gates

* the following logic gates can be generated as networks of the basic gates:
    * NAND
    * NOR

---

### 2.1 NAND operator

$$
L \left( x_{1}, x_{2} \right) = \overline{x_{1} \cdot x_{2}}
$$

#### 2.1.1 NAND truth table

$x_{1}$|$x_{2}$|$L\left( x_{1}, x_{2} \right)$
:---:|:---:|:---:
$0$|$0$|$1$
$0$|$1$|$1$
$1$|$0$|$1$
$1$|$1$|$0$

#### 2.1.2 NAND diagram

* AND can be represented as an AND gate followed by a NOT gate:

<!-- image -->

#### 2.1.3 NAND logic gate symbol

<!-- image -->

---

### 2.2 NOR operator

$$
L \left( x_{1}, x_{2} \right) = \overline{x_{1} + x_{2}}
$$

#### 2.2.1 NOR truth table

$x_{1}$|$x_{2}$|$L\left( x_{1}, x_{2} \right)$
:---:|:---:|:---:
$0$|$0$|$1$
$0$|$1$|$0$
$1$|$0$|$0$
$1$|$1$|$0$

#### 2.2.2 NOR diagram

* AND can be represented as an +OR gate followed by a NOT gate:

<!-- image -->

#### 2.2.3 NOR logic gate symbol

<!-- image -->

</br>
</br>

---

</br>
</br>

## 3 Timing diagrams

* behavior of network in responses to changes in input signals captured by **timing diagram**
    * time runs from left to right
* timing diagrams capture real delays in signal propagation

<!-- image -->

</br>
</br>

---

</br>
</br>

## 4 Functionally equivalent networks

* **functionally equivalent networks** have the same output behavior as given by a truth table
* considerations in choosing which network to accept:
    * simplicity
    * cost

</br>
</br>

---

</br>
</br>

## 5 Boolean algebra

* **Boolean algebra** is algebraic process for manipulating true/false statements
* Boolean alegbra as set notation:
    * AND - intersection ($\wedge$)
    * OR - union ($\vee$)
* operation precedence is:

1. NOT
2. AND
3. OR

### 5.1 Axioms

$$
0 \cdot 0 = 0
$$

$$
0 + 0 = 0
$$

$$
1 \cdot 1 = 1
$$

$$
1 + 1 = 1
$$

$$
1 \cdot 0 = 0 \cdot 1 = 0
$$

$$
1 + 0 = 0 + 1 = 1
$$

### 5.2 Single-value theorems

$$
x \cdot 0 = 0
$$

$$
x + 0 = x
$$

$$
x \cdot 1 = x
$$

$$
x + 1 = 1
$$

$$
x \cdot x = x
$$

$$
x + x = x
$$

$$
x \cdot \bar{x} = 0
$$

$$
x + \bar{x} = 1
$$

$$
\bar{\bar{x}} = x
$$

---

### 5.3 Multiple-value theorems

#### 5.3.1 Commutative

$$
x \cdot y = y \cdot x
$$

$$
x + y = y + x
$$

#### 5.3.2 Associative

$$
x \cdot \left( y \cdot z \right) = \left(x \cdot y \right) \cdot z
$$

$$
x + \left( y + z \right) = \left(x + y \right) + z
$$

#### 5.3.3 Distributive

$$
x \cdot \left( y + z \right) = x \cdot y + x \cdot z
$$

$$
x + y \cdot z = \left( x + y \right) \cdot \left( x + z \right)
$$

#### 5.3.4 Absorption

$$
x + x \cdot y = x
$$

$$
x \cdot \left( x + y \right) = x
$$

#### 5.3.5 Combination

$$
x \cdot y + x \cdot \bar{y} = x
$$

$$
\left( x + y \right) \cdot \left( x + \bar{y} \right) = x
$$

#### 5.3.6 Consensus

$$
x \cdot y + y \cdot z + \bar{x} \cdot z = x \cdot y + \bar{x} \cdot z
$$

$$
\left( x + y \right) \cdot \left( y + z \right) \cdot \left( \bar{x} + y \right) = \left( x + y \right) \cdot \left( \bar{x} + z \right)
$$

#### 5.3.7 DeMorgan's theorem

$$
\overline{x \cdot y} = \bar{x} + \bar{y}
$$

$$
\overline{x + y} = \bar{x} \cdot \bar{y}
$$

---

### 5.4 Principle of duality

* the dual of a logic expression is obtained by:

1. replacing all AND operators with OR operators and vice-versa
2. replacing all $1$'s with $0$'s and vice-versa

</br>
</br>

---

</br>
</br>

## 6 Synthesis strategies

* $2$ methods for synthesis are:
    * sum-of-products
    * product-of-sums

### 6.1 Sum-of-products

* generate a minterm for each row
    * minterm obtained by performing AND operation on:
        * input variable if value is $1$
        * complement of input variable if value is $0$
* perform OR operation on all minterms in which output value is $1$

* example:

row #|$x_{1}$|$x_{2}$|$x_{3}$|$f \left( x_{1}, x_{2}, x_{3} \right)$
:---:|:---:|:---:|:---:|:---:|
$0$|$0$|$0$|$0$|$0$
$1$|$0$|$0$|$1$|$1$
$2$|$0$|$1$|$0$|$0$
$3$|$0$|$1$|$1$|$0$
$4$|$1$|$0$|$0$|$1$
$5$|$1$|$0$|$1$|$1$
$6$|$1$|$1$|$0$|$1$
$7$|$1$|$1$|$1$|$0$

\begin{align*}
f \left( x_{1}, x_{2}, x_{3} \right) &= \underbrace{\bar{x}_{1} \cdot \bar{x}_{2} \cdot x_{3}}_{m_{1}} + \underbrace{x_{1} \cdot \bar{x}_{2} \cdot \bar{x}_{3}}_{m_{4}} + \underbrace{x_{1} \cdot \bar{x}_{2} \cdot x_{3}}_{m_{5}} + \underbrace{x_{1} \cdot x_{2} \cdot \bar{x}_{3}}_{m_{6}} \\
&= \sum (m_{1}, m_{4}, m_{5}, m_{6}) \\
&= \sum m(1, 4, 5, 6) \\
\end{align*}

* if each product term is minterm, expression is **canonical sum-of-products**
* canonical sum-of-products can be built out of NAND gates:

<!-- image -->

---

### 6.2 Product-of-sums

* generate a maxterm for each row
    * maxterm obtained by performing OR operation on:
        * input variable if value is $0$
        * complement of input variable if value is $1$
* perform AND operation on all maxterms in which output value is $0$

* example:

row #|$x_{1}$|$x_{2}$|$x_{3}$|$f \left( x_{1}, x_{2}, x_{3} \right)$
:---:|:---:|:---:|:---:|:---:|
$0$|$0$|$0$|$0$|$0$
$1$|$0$|$0$|$1$|$1$
$2$|$0$|$1$|$0$|$0$
$3$|$0$|$1$|$1$|$0$
$4$|$1$|$0$|$0$|$1$
$5$|$1$|$0$|$1$|$1$
$6$|$1$|$1$|$0$|$1$
$7$|$1$|$1$|$1$|$0$

\begin{align*}
f \left( x_{1}, x_{2}, x_{3} \right) &= \underbrace{ \left( x_{1} + x_{2} + x_{3} \right) }_{ M_{0} } \cdot \underbrace{ \left( x_{1} + \bar{x}_{2} + x_{3} \right) }_{ M_{2} } \cdot \underbrace{ \left( x_{1} + \bar{x}_{2} + \bar{x}_{3} \right) }_{ M_{3} } \cdot \underbrace{ \left( \bar{x}_{1} + \bar{x}_{2} + \bar{x}_{3} \right) }_{ M_{7} }\\
&= \prod (M_{0}, M_{2}, M_{3}, M_{7}) \\
&= \prod M(0, 2, 3, 7) \\
\end{align*}

* if each product term is maxterm, expression is **canonical product-of-sums**
* canonical sum-of-products can be built out of NOR gates:

<!-- image -->

</br>
</br>

---

</br>
</br>

## 7 Multiplexing

* need to choose one source from multiple input sources
* for $2$ inputs, add another input that serves as switch:

<!-- image -->

---

<br/>
<br/>