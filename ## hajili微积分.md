# 这是hajili微积分讲义
#### 参考
###### T. Apostol, **Calculus Vol 1**  Stewart
* 这节课介绍了R和R上的序关系
### \(\mathbb{R}\)
我们假设存在一个无限集合 \( \mathbb{R} \)（称为实数集 real numbers），  
配备加法 \( + \) 和乘法 \( \cdot \) 运算，满足以下公理（axioms）：

- **公理1（交换律 commutativity）**：  
  \( x + y = y + x \)，\( x y = y x \)，对任意 \( x, y \in \mathbb{R} \)。
- **公理2（结合律 associativity）**：  
  \( x + (y + z) = (x + y) + z \)，  
  \( x (y z) = (x y) z \)。
- **公理3（分配律 distributivity）**：  
  \( x (y + z) = x y + x z \)。
- **公理4（单位元 identity elements）**：  
  存在 \( 0, 1 \in \mathbb{R} \)，使得对任意 \( x \in \mathbb{R} \)，  
  \( x + 0 = x \)，\( 1 \cdot x = x \)。
- **公理5（加法逆元 additive inverse）**：  
  对任意 \( x \in \mathbb{R} \)，存在 \( -x \in \mathbb{R} \)，使得  
  \( x + (-x) = 0 \)。
- **公理6（乘法逆元 multiplicative inverse）**：  
  对任意 \( x \in \mathbb{R}, x \neq 0 \)，存在 \( x^{-1} \in \mathbb{R} \)，使得  
  \( x \cdot x^{-1} = 1 \)。

---

##### 定理1.7（加法消去律 cancellation law for addition）：
\[
(a + b = a + c) \Rightarrow b = c
\]
**证明**：  
给定 \( a + b = a + c \)，  
1. 两边同时加上 \( -a \)（加法逆元 additive inverse）：  
   \( (-a) + a + b = (-a) + (a + c) \)  
2. 由结合律 associativity：  
   \( [(-a) + a] + b = [(-a) + a] + c \)  
3. 由加法逆元 additive inverse 性质：  
   \( 0 + b = 0 + c \)  
4. 由单位元 identity element 性质：  
   \( b = c \)

---

##### 唯一性（Uniqueness）：
零元（zero element）0 是唯一的。  
**证明**：假设存在另一个零元 0'，满足对任意 \( x \in \mathbb{R} \)，  
\( x + 0' = x \)。  
取 \( x = 0 \)，则 \( 0 + 0' = 0 \)。  
但由公理4，\( 0' + 0 = 0' \)。  
由交换律 commutativity，\( 0 + 0' = 0' + 0 \)，  
因此 \( 0' = 0 \)。

---

##### 备注：
在实数集 \( \mathbb{R} \) 中，单位元（identity element）1 不等于零元（zero element）0。  
**反证法（proof by contradiction）**：假设 \( 1 = 0 \)，  
则对任意 \( x \in \mathbb{R} \)，  
\( x = 1 \cdot x = 0 \cdot x = 0 \)，  
这意味着 \( \mathbb{R} = \{0\} \)，与 \( \mathbb{R} \) 是无限集矛盾。

---

##### 定理1.12（负负得正）：
\[
(-a) b = -(a b), \quad (-a)(-b) = a b
\]
**特例**：  
\[
(-1)(-1) = 1
\]

---

#### 序公理（Order Axioms）

我们假设存在一个子集 \( \mathbb{R}^+ \subseteq \mathbb{R} \)，称为正实数集（positive real numbers），满足：

- **公理7（封闭性 closure）**：  
  对任意 \( x, y \in \mathbb{R}^+ \)，有  
  \( x + y \in \mathbb{R}^+ \)，\( x y \in \mathbb{R}^+ \)。
- **公理8（三分律 trichotomy）**：  
  对任意 \( x \in \mathbb{R}, x \neq 0 \)，  
  要么 \( x \in \mathbb{R}^+ \)，要么 \( -x \in \mathbb{R}^+ \)。
- **公理9（零非正）**：  
  \( 0 \notin \mathbb{R}^+ \)。

---

##### 定义7（序关系 order relations）：
1. \( x < y \) 表示 \( y - x \in \mathbb{R}^+ \)。
2. \( y > x \) 表示 \( x < y \)。
3. \( x \leq y \) 表示 \( x < y \) 或 \( x = y \)。
4. \( y \geq x \) 表示 \( x \leq y \)。

**例子**：  
\( 2 - (-2) = 4 \in \mathbb{R}^+ \)，因此 \( -2 < 2 \)。

---

##### 定理1.22（正数判定）：
\[
(x > 0) \iff (x \text{ 是正数 positive})
\]
**证明**：  
- \( (\Rightarrow) \)：\( x > 0 \) 按定义即 \( 0 < x \)，也就是 \( x - 0 \in \mathbb{R}^+ \)，即 \( x \in \mathbb{R}^+ \)。  
- \( (\Leftarrow) \)：若 \( x \in \mathbb{R}^+ \)，则 \( x = x - 0 \in \mathbb{R}^+ \)，即 \( x > 0 \)。

---

##### 定义8（负数 negative number）：
若 \( x < 0 \)，则称 \( x \) 为负数（negative）。  
若 \( x \geq 0 \)，则称 \( x \) 为非负数（nonnegative）。

---

##### 例子1.23：
我们知道 \( 1 \neq 0 \)，因此 \( -1 \neq 0 \)。  
由公理8（三分律 trichotomy），  
要么 \( 1 \in \mathbb{R}^+ \)，要么 \( -1 \in \mathbb{R}^+ \)。  
事实上，\( 1 \in \mathbb{R}^+ \)。  
**反证法（proof by contradiction）**：假设 \( -1 \in \mathbb{R}^+ \)，  
则 \( (-1)(-1) = 1 \in \mathbb{R}^+ \)，矛盾。

---

##### 定理1.24（全序性 total order）：
对任意 \( a, b \in \mathbb{R} \)，以下三种情况有且仅有一种成立：  
\( a < b \)，\( b < a \)，或 \( a = b \)。

**证明**：令 \( x = b - a \)。  
- 若 \( x = 0 \)，则 \( b = a \)。  
- 若 \( x \neq 0 \)，由公理8（三分律 trichotomy），  
  要么 \( x \in \mathbb{R}^+ \)（即 \( a < b \)），  
  要么 \( -x \in \mathbb{R}^+ \)（即 \( b < a \)）。

---

##### 定理1.25（传递性 transitivity）：
\[
(a < b \text{ 且 } b < c) \Rightarrow (a < c)
\]
**证明**：  
\( a < b \) 即 \( b - a \in \mathbb{R}^+ \)，  
\( b < c \) 即 \( c - b \in \mathbb{R}^+ \)。  
由公理7（封闭性 closure），  
\( (c - b) + (b - a) = c - a \in \mathbb{R}^+ \)，  
即 \( a < c \)。

---

##### 定理1.26（加法保序性 addition preserves order）：
\[
(a < b) \Rightarrow (a + c < b + c)
\]
**证明**：  
\( (b + c) - (a + c) = b - a \in \mathbb{R}^+ \)，  
因此 \( a + c < b + c \)。

---

##### 定理1.27（正数乘法保序性 multiplication by positive number preserves order）：
\[
(c > 0 \text{ 且 } a < b) \Rightarrow (a c < b c)
\]
**证明**：  
\( b c - a c = (b - a) c \in \mathbb{R}^+ \)，  
因为 \( b - a \in \mathbb{R}^+ \) 且 \( c \in \mathbb{R}^+ \)。

---
