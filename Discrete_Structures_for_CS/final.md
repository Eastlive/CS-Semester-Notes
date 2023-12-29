# 9 relations

自反（Reflexivity）和反对称（Antisymmetry）是关系理论中的两个不同的概念，它们描述了集合中元素之间关系的不同属性。

1. **自反性（Reflexivity）**:
   - **定义**：在数学中，一个关系 \(R\) 在集合 \(A\) 上是自反的，如果集合 \(A\) 中的每一个元素都与自身在关系 \(R\) 下相连。用形式化的语言来说，对于所有 \(a\) 属于 \(A\)，都有 \((a, a) \in R\)。
   - **例子**：例如，"等于" (\(=\)) 是一个自反关系，因为对于任何数 \(a\)，\(a = a\) 总是成立的。

2. **反对称性（Antisymmetry）**:
   - **定义**：一个关系 \(R\) 在集合 \(A\) 上是反对称的，如果对于所有的 \(a\) 和 \(b\) 属于 \(A\)，只要 \((a, b) \in R\) 和 \((b, a) \in R\) 同时成立，那么就必须有 \(a = b\)。简而言之，如果两个不同的元素互相相关，则这种关系不能同时存在。
   - **例子**："小于或等于" (\(\leq\)) 是一个反对称关系，因为如果 \(a \leq b\) 并且 \(b \leq a\)，那么我们可以得出 \(a = b\)。

自反性和反对称性是描述一个关系特性的两个独立方面，它们并不是同一种东西，但可以同时在一个关系中出现。例如，在一个偏序集（如整数集合上的 "小于或等于" 关系）中，关系既是自反的又是反对称的。但也有可能只具备其中一种属性，或者两种属性都不具备。因此，虽然它们都是用来描述集合中元素间关系的特性，但它们描述的是不同的方面。

在数学中，尤其是在集合论和逻辑学中，有几种重要的关系特性用于描述集合元素之间的关系。除了自反性和反对称性之外，还有以下几种：

1. **对称性（Symmetry）**:
   - **定义**：如果一个关系 \(R\) 在集合 \(A\) 上是对称的，那么对于所有 \(a, b\) 属于 \(A\)，只要 \((a, b) \in R\)，就必然有 \((b, a) \in R\)。
   - **例子**："等于" (\(=\)) 关系是对称的，因为如果 \(a = b\)，那么 \(b = a\)。

2. **传递性（Transitivity）**:
   - **定义**：一个关系 \(R\) 在集合 \(A\) 上是传递的，如果对于所有 \(a, b, c\) 属于 \(A\)，只要 \((a, b) \in R\) 和 \((b, c) \in R\)，就必然有 \((a, c) \in R\)。
   - **例子**："小于" (\(<\)) 关系是传递的，因为如果 \(a < b\) 且 \(b < c\)，那么 \(a < c\)。

3. **反自反性（Irreflexivity）**:
   - **定义**：一个关系 \(R\) 在集合 \(A\) 上是反自反的，如果对于所有 \(a\) 属于 \(A\)，\((a, a) \notin R\)。
   - **例子**："小于" (\(<\)) 是一个反自反关系，因为没有任何数 \(a\) 是小于自己的。

4. **非对称性（Asymmetry）**:
   - **定义**：一个关系 \(R\) 是非对称的，如果 \((a, b) \in R\) 意味着 \((b, a) \notin R\)，对所有 \(a\) 和 \(b\)。
   - **例子**："小于" (\(<\)) 关系是非对称的，因为如果 \(a < b\)，则不能有 \(b < a\)。

这些关系特性在数学的不同领域中非常重要，如在定义等价关系、偏序关系和全序关系时。通过组合这些不同的属性，可以定义出更复杂和特定领域的关系类型。例如，一个既是自反的又是对称和传递的关系被称为等价关系。这些关系帮助我们理解和表述数学结构和逻辑概念。

## 9.1

- Q1
  - 给定两个集合A，B，写出满足给定关系的集合R
  - lcm(a,b) = a*b/gcd(a,b) 最小公倍数

- Q3
- 给定一个关系R(集合)，写出其是否满足给定的性质
  - 自反
  - 对称
  - 传递
  - 反对称
  - relation:
    - reflexive(自反)
    - symmetric(对称)
    - transitive(传递)
    - antisymmetric(反对称)
    - irreflexive(反自反)
    - asymmetric(非对称)
    - equivalence(等价)

- Q6
  - 给定一个关系R（如 x+y=0），写出其是否满足给定的性质
    - 自反
    - 对称
    - 传递
    - 反对称： x=2y是反对称的
    - 单词表： rational number 有理数
    
- Q34
  - 关系的计算
  - R_1 ∪ R_2
  
- Q36
  - 关系的composite
  - 中文：复合
  - 符号： ∘
  - R_1 ∘ R_2

## 9.2 n-ary Relations （多元关系）

- Q1
  - 写出给定条件的三元关系

- Q14
  - What do you obtain when you apply the projection P_2,3,5 to the 5-tuple (a, b, c, d, e)?
  - P_2,3,5(a, b, c, d, e) = (b, c, e)
  - P的意思是：projection 投影
  - 5-tuple: 五元组

## 9.3 Equivalence Relations （等价关系）

等价关系（Equivalence Relations）是数学中一种特殊类型的关系，它在集合的元素之间定义了一种等价的概念。等价关系在许多数学分支中都非常重要，特别是在集合论、抽象代数和其他许多领域中。一种关系要想被称为等价关系，必须满足以下三个条件：

1. **自反性（Reflexive）**:
   - 对于集合中的所有元素 \(a\)，\(a\) 与自身在关系中，即 \(aRa\)。

2. **对称性（Symmetric）**:
   - 对于任何两个元素 \(a\) 和 \(b\)，如果 \(aRb\)，则必须有 \(bRa\)。这意味着关系是双向的。

3. **传递性（Transitive）**:
   - 对于任何三个元素 \(a\)、\(b\) 和 \(c\)，如果 \(aRb\) 和 \(bRc\)，则必须有 \(aRc\)。这意味着关系可以“通过”中间元素传递。

当一个关系同时满足这三个条件时，它就形成了集合中元素的等价类。在这种情况下，任何两个具有相同关系的元素都可以认为是在某种意义上相同或等价的。

---

## 关于[a]的说明

设R是集合A上的等价关系。与A中的元素a相关的所有元素的集合称为a的等价类。 a 相对于 R 的等价类由 $[a]_R$ 表示。 当只考虑一个关系时，我们可以删除下标R并为该等价类写[a]。

---

## 只满足自反和对称的关系

一个等价关系通常满足自反性（Reflexive）、对称性（Symmetric）和传递性（Transitive），但如果我们想要构造一个满足自反和对称但不满足传递性的关系，我们可以考虑集合中元素的某种非传递的相似性。

### 例子：朋友关系

假设有一个集合 \( A = \{a, b, c\} \)，代表三个人。我们定义一个关系 \( R \) 来表示“是朋友”，但以一种特定的方式：

- **自反性（Reflexive）**：每个人都是自己的朋友。即对于所有 \( x \in A \)，都有 \( (x, x) \in R \)。
  
- **对称性（Symmetric）**：如果 \( a \) 是 \( b \) 的朋友，那么 \( b \) 是 \( a \) 的朋友。即如果 \( (a, b) \in R \) 那么 \( (b, a) \in R \)。

现在，我们来定义具体的朋友关系：

- \( a \) 是 \( b \) 的朋友，\( b \) 是 \( a \) 的朋友。
- \( b \) 是 \( c \) 的朋友，\( c \) 是 \( b \) 的朋友。
- 但 \( a \) 不是 \( c \) 的朋友，也就是 \( (a, c) \notin R \) 且 \( (c, a) \notin R \)。

在这个例子中，我们看到关系 \( R \) 是自反的和对称的。但它不是传递的，因为尽管 \( a \) 是 \( b \) 的朋友，\( b \) 是 \( c \) 的朋友，但 \( a \) 不是 \( c \) 的朋友。因此，\((a, b) \in R\) 和 \((b, c) \in R\) 但 \((a, c) \notin R\)，违反了传递性。

在现实世界中，朋友关系通常更复杂并且倾向于是传递的，但这个简化的模型提供了一个直观的例子来展示一个关系如何可能是自反的和对称的，但不是传递的。

---

- Q10
   - Suppose that A is a nonempty set and R is an equivalence relation on A. Show that there is a function f with A as its domain such that (x, y) ∈ R if and only if f (x) = f (y).
   - 证明：如果A是一个非空集合，R是A上的一个等价关系，那么存在一个函数f，它的定义域是A，使得(x, y) ∈ R当且仅当f(x) = f(y)。

- Q15
  - 证明一个关系是等价关系

- Q35
  - What is the congruence class $[n]_5$ (that is, the equivalence class of n with respect to congruence modulo 5)when n is
   a) 2
   b) 3?
   c) 6?
   d) −3?
   - 单词： congruence 同余
   - equivalence class 等价类
   - modular arithmetic 模运算

- Q47
  - 证明一个关系是等价关系