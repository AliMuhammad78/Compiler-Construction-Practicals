# 🧩 Compiler Construction Practicals

<p align="center">

  <h1 align="center">⚙️ Compiler Construction Practicals</h1>

  <p align="center">
    A collection of practical implementations, assignments, parsing programs,
    and study resources developed while learning <strong>Compiler Construction</strong>.
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/Python-Programs-3776AB?style=for-the-badge&logo=python&logoColor=white">
    <img src="https://img.shields.io/badge/Compiler%20Design-Concepts-8A2BE2?style=for-the-badge">
    <img src="https://img.shields.io/badge/Parsing-Syntax%20Analysis-orange?style=for-the-badge">
    <img src="https://img.shields.io/badge/Grammar-Analysis-2E8B57?style=for-the-badge">
    <img src="https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white">
  </p>

</p>

---

## 📚 About The Repository

**Compiler Construction Practicals** is a collection of practical work completed while studying the **Compiler Construction** subject.

The repository combines **Python implementations, Jupyter notebooks, assignments, questions, solutions, presentations, and reference material** related to compiler design and construction.

The main purpose of this repository is to turn theoretical compiler concepts into working programs and algorithms.

The practical work covers several important areas of compiler construction, including:

* 🔢 Intermediate code generation
* 🔤 DFA construction
* 🧩 Context-free grammar analysis
* 🔍 FIRST and FOLLOW computation
* 🌳 Grammar transformations
* 🚫 Left-recursion elimination
* ✂️ Left factoring
* 📐 LL(1) grammar analysis
* ⚙️ CLR(1) parsing
* 📊 Parsing-table construction

---

## 🎯 Learning Objectives

This repository was created to practice and understand how theoretical concepts from **Compiler Construction** can be implemented programmatically.

The major objectives include:

* Understand the major concepts involved in compiler construction
* Implement compiler-related algorithms using Python
* Analyze context-free grammars programmatically
* Understand lexical and syntax analysis
* Generate intermediate representations
* Construct and analyze finite automata
* Calculate FIRST and FOLLOW sets
* Identify grammar properties
* Transform grammars for parsing
* Understand LL(1) and LR-family parsing techniques
* Construct parsing tables programmatically

---

## 🧠 Practical Questions & Implementations

The `Ppt_Question.ipynb` notebook contains implementations for several compiler-construction questions.

### 🔢 Q16 — Quadruple Generation

**Write a program to generate Quadruple of any input string.**

This practical focuses on **intermediate code generation**, representing operations using quadruples.

A quadruple generally represents an operation using four components:

```text
(operator, argument1, argument2, result)
```

Example:

```text
a + b
```

can be represented conceptually as:

```text
+   a   b   t1
```

---

### 🔤 Q17 — DFA for Strings Ending with `001`

**Write a DFA program for strings ending with `001`.**

This practical demonstrates the construction of a **Deterministic Finite Automaton (DFA)** capable of recognizing strings whose final three symbols are:

```text
001
```

The program provides practical exposure to:

* States
* Transitions
* Start states
* Final/accepting states
* String processing using automata

---

### 🧩 Q18 — Grammar Analysis

**Write a program to check whether a grammar is:**

* Ambiguous
* Left recursive
* LL(1)

This practical focuses on analyzing the structural properties of a grammar.

#### Ambiguity

A grammar is ambiguous when a string can have more than one valid parse structure.

#### Left Recursion

A grammar contains left recursion when a non-terminal can derive a sentential form beginning with itself, for example:

```text
A → Aα
```

Left recursion is particularly important when preparing grammars for predictive parsing.

#### LL(1)

LL(1) parsing uses one-symbol lookahead to select the appropriate production. FIRST/FOLLOW information plays an important role in determining whether a grammar can be handled by an LL(1) parser.

---

### 🔍 Q19 — FIRST and FOLLOW

**Write a program for FIRST and FOLLOW.**

The notebook implements the computation of:

```text
FIRST(A)
FOLLOW(A)
```

for grammar symbols.

These sets are fundamental concepts in syntax analysis and are used in constructing predictive parsing techniques and analyzing LL(1) grammars.

---

### 🔄 Q20 — Left Recursion & Left Factoring

**Write a program to remove Left Recursion and Left Factoring from grammar.**

This practical focuses on transforming grammars into forms that are more suitable for predictive parsing.

### Left Recursion

Example:

```text
A → Aα | β
```

can be transformed into an equivalent non-left-recursive form.

### Left Factoring

Left factoring extracts common prefixes from productions.

For example:

```text
A → αβ₁ | αβ₂
```

can be transformed by factoring the common prefix `α`.

These transformations are commonly used when preparing grammars for LL-style parsing.

---

## ⚙️ CLR(1) Parser

The repository also contains a dedicated notebook:

```text
code/clr(1).ipynb
```

This notebook implements the construction of a **CLR(1) / Canonical LR(1) parser**.

CLR(1) parsing uses LR(1) items containing a production position together with a one-symbol lookahead. The lookahead information helps determine where reductions should be placed in the parsing table.

The implementation covers concepts such as:

```text
Grammar
   ↓
Augmented Grammar
   ↓
LR(1) Items
   ↓
Closure
   ↓
GOTO
   ↓
Canonical Collection
   ↓
CLR(1) Parsing Table
```

> **📝 Note:** The grammar used by the CLR(1) implementation can be modified in the notebook according to the grammar that needs to be parsed.

---

## 🗂️ Repository Contents

```text
Compiler-Construction-Practicals/
│
├── 📁 code/
│   ├── clr(1).ipynb
│   └── Ppt_Question.ipynb
│
└── 📁 files/
    ├── Assignment 02_CC_5.5.26.docx
    ├── CC-054-095-122-ppt-q.docx
    ├── CC-Assignment-01_Spring26.pdf
    ├── CC_095_Assignment_1.pdf
    ├── CC_Assignment02.pdf
    ├── Compilers - Principles, Techniques, and Tools (2006).pdf
    ├── Compiler_Assignment02_Solutions.docx
    └── Final_Presentation_Questions_Sec_A,B,C.docx
```

---

## 📓 Jupyter Notebooks

### `clr(1).ipynb`

A practical implementation of a **CLR(1) parser**, including the generation of LR(1) items and parsing structures.

### `Ppt_Question.ipynb`

Contains implementations related to practical questions:

| Question | Topic                             |
| -------- | --------------------------------- |
| Q16      | Quadruple Generation              |
| Q17      | DFA for Strings Ending with `001` |
| Q18      | Grammar Analysis                  |
| Q19      | FIRST and FOLLOW                  |
| Q20      | Left Recursion & Left Factoring   |

---

## 📁 Assignments & Study Material

The `files` directory contains supporting academic material collected during the Compiler Construction course.

It includes:

* 📝 Assignments
* 📄 Assignment solutions
* ❓ Presentation questions
* 📚 Compiler Construction reference material
* 📑 Course-related documents

These resources provide additional theoretical and practical context for the implementations in the notebooks.

---

## 🛠️ Technologies Used

| Technology                   | Purpose                                    |
| ---------------------------- | ------------------------------------------ |
| 🐍 **Python**                | Implementing compiler algorithms           |
| 📓 **Jupyter Notebook**      | Interactive development and demonstrations |
| 🧠 **Compiler Construction** | Core subject concepts                      |
| 🔤 **Formal Grammars**       | Grammar representation and analysis        |
| 🔄 **Parsing Algorithms**    | Syntax analysis                            |
| 🤖 **Finite Automata**       | DFA-based string recognition               |

---

## 🧭 Topics Covered

### 🔤 Lexical & Automata Concepts

* Deterministic Finite Automata
* State transitions
* String recognition
* Pattern-based language recognition

### 🧩 Grammar & Syntax Analysis

* Context-Free Grammars
* Grammar properties
* Ambiguity
* Left recursion
* Left factoring
* LL(1) analysis

### 🔍 Grammar Sets

* FIRST
* FOLLOW
* Nullable productions
* Predictive parsing concepts

### ⚙️ Parsing

* LR parsing
* LR(1) items
* CLR(1)
* Closure
* GOTO
* Canonical collections
* Parsing tables

### 🔢 Intermediate Code

* Quadruples
* Intermediate representations
* Temporary variables
* Three-address-style concepts

---

## 📈 Conceptual Learning Path

The practical work can be viewed as a progression through the major stages of syntax-oriented compiler construction:

```text
             COMPILER CONSTRUCTION
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
   Finite Automata           Formal Grammars
          │                       │
          ▼                       ▼
         DFA                Grammar Analysis
                                  │
                  ┌───────────────┼───────────────┐
                  ▼               ▼               ▼
              FIRST/FOLLOW    Ambiguity       LL(1)
                                  │
                                  ▼
                       Grammar Transformation
                          │             │
                          ▼             ▼
                    Left Recursion   Left Factoring
                          │
                          ▼
                       Parsing
                          │
                ┌─────────┴─────────┐
                ▼                   ▼
             LL(1)              CLR(1)
                │                   │
                └─────────┬─────────┘
                          ▼
                 Parsing Tables
                          │
                          ▼
              Intermediate Code
                    / Quadruples
```

---

## 🎓 Learning Outcomes

By working through these programs and notebooks, the following concepts can be practiced:

* ✅ Understanding compiler construction fundamentals
* ✅ Working with formal grammars
* ✅ Implementing DFA-based recognition
* ✅ Computing FIRST and FOLLOW
* ✅ Detecting grammar properties
* ✅ Transforming grammars
* ✅ Understanding predictive parsing
* ✅ Understanding LR-family parsers
* ✅ Constructing CLR(1) parsing structures
* ✅ Generating intermediate representations
* ✅ Translating theoretical algorithms into working programs

---

## 📚 Reference

The repository also contains ***Compilers: Principles, Techniques, and Tools* (2006)** as course/reference material.

Compiler construction topics such as grammar transformation, FIRST/FOLLOW, LL parsing, and LR parsing form fundamental parts of compiler design.

---

## 👨‍💻 Author

**Muhammad Ali**

[![GitHub](https://img.shields.io/badge/GitHub-AliMuhammad78-181717?style=flat-square\&logo=github\&logoColor=white)](https://github.com/AliMuhammad78)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Muhammad%20Ali-0A66C2?style=flat-square\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/muhammad-ali-91294a290)
[![Kaggle](https://img.shields.io/badge/Kaggle-ali98muhammad45-20BEFF?style=flat-square\&logo=kaggle\&logoColor=white)](https://www.kaggle.com/ali98muhammad45)

---

<p align="center">

⭐ <strong>Compiler Construction — From Theory to Implementation</strong>

</p>
