# Lec01

classroom name：[https://en.wikipedia.org/wiki/Lip%C3%B3t\_Fej%C3%A9r](https://en.wikipedia.org/wiki/Lip%C3%B3t\_Fej%C3%A9r)

### Three related topics:

* Curry–Howard correspondence: [https://en.wikipedia.org/wiki/Curry%E2%80%93Howard\_correspondence](https://en.wikipedia.org/wiki/Curry%E2%80%93Howard\_correspondence)
* Category theory: [https://en.wikipedia.org/wiki/Category\_theory](https://en.wikipedia.org/wiki/Category\_theory)
* ZFC: [https://en.wikipedia.org/wiki/Zermelo%E2%80%93Fraenkel\_set\_theory](https://en.wikipedia.org/wiki/Zermelo%E2%80%93Fraenkel\_set\_theory)
  * mathematics is built on first-order logic and the axioms of ZF set theory
* Cantor: let's design a theory for collections
  * we build collections using predicates = { x | s.t. x + 2 > 3 }, { x | x ∌ x }
  * in type theory, the notion of predicate comes after collection

### Model of Computation:

1. Combinators by Moses Schönfinkel in 1920
2. Lambda calculus by Alonzo Church in the 1930s
3. The Turing machine by Alan Turing in 1936

### What's the difference between set theory and type theory?

#### Elementhood :

* 3 ∈ ℕ Proposition Python (dynamic type)
* 3 : ℕ Judgement Haskell/Java (static type)

#### Logic :

* Set theory : predicate logic (Prop = Bool)
* Type theory : Explain logic by assign the type of evidence to every proposition.(Prop= type,Carry-Howard Equivalence)
* Predicate Logic: [https://brilliant.org/wiki/predicate-logic/](https://brilliant.org/wiki/predicate-logic/)

#### exp: 2 ∉ 4 ?

2 ∈ 4 for Neumann, but not Zermelo

* Zermelo Construction [https://proofwiki.org/wiki/Definition:Natural\_Numbers/Zermelo\_Construction](https://proofwiki.org/wiki/Definition:Natural\_Numbers/Zermelo\_Construction)
* Von Neumann Construction [https://proofwiki.org/wiki/Definition:Natural\_Numbers/Von\_Neumann\_Construction](https://proofwiki.org/wiki/Definition:Natural\_Numbers/Von\_Neumann\_Construction)

### Implementations (proof assistants):

* **Agda** SWEDISH very similar to Haskell, mainly for type theorists, most features
* **Coq** FRENCH very practical, Chrome, Firefox, Linux kernel (formal semantics)
* **Lean** AMERICAN mathematicians use this, formalisation
* **Idris** SCOTTISH very similar to Haskell, programming

related courses = discrete mathematics (algebra), logic, computability, formal languages, compilers, Haskell/Clean

Discussion: [https://proofassistants.stackexchange.com/questions/43/proof-assistants-for-beginners-a-comparison](https://proofassistants.stackexchange.com/questions/43/proof-assistants-for-beginners-a-comparison)

mathematicians use t.t. to computer check their proofs programmers use t.t. to computer check their programs

### Simple Types

[https://www.cs.nott.ac.uk/\~psztxa/mgs.2021/simple-types.pdf](https://www.cs.nott.ac.uk/\~psztxa/mgs.2021/simple-types.pdf)

[https://www.cs.nott.ac.uk/\~psztxa/mgs.2021/monday.pdf](https://www.cs.nott.ac.uk/\~psztxa/mgs.2021/monday.pdf)

* To define a function with several parameters we use **currying**, that is a function that returns a function:
  * add : N → (N → N)
  * add = x → ( y → x + y)
  * currying: instead of (A × B → C) you write (A → (B → C))
    * \_+\_ : ℕ → (ℕ → ℕ)
    * 3+\_ : ℕ → ℕ
* Instead of returning a function we can also have functions that have functions as input (these are called **higher order functions**).
  * k : (N → N) → N
  * k h = h 2 + h 3
* Some functions work for any type, we call them **polymorphic**.
