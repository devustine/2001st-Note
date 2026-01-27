##  Propositional Logic

### What is Propositional Logic?
Propositional logic (also called Boolean logic, propositional calculus or zero-order logic) is simply about statements that are either **true** or **false**. no in-between. Think of it like light switches, they're either ON or OFF.

**Examples of propositions:**
- "A football is spherical in shape" → TRUE
- "3 + 9 = 24" → FALSE
- "Miva is an open university" → TRUE

These are propositions because we can clearly say if they're true or false.

### What are Logical Connectives?
Logical connectives are simply the symbols or words we use to connect simple statements together to form more complex statements. Think of them like the glue that joins sentences together.

**Why Do We Need Them?**
Instead of having separate statements like:
- "It is raining"
- "I will carry an umbrella"

We can connect them:
- "It is raining **AND** I will carry an umbrella"
- "IF it is raining, **THEN** I will carry an umbrella"

### Logical Operators (The Building Blocks)
These are like mathematical symbols (+, -, ×) but for logic:

#### 1. NOT (Negation) - Symbol: ¬ or !
This flips the truth value, makes true become false, and false become true.

**Example:**
- If P = "It is raining" (TRUE)
- Then ¬P = "It is NOT raining" (FALSE)

#### 2. AND (Conjunction) - Symbol: ∧
Both things must be true for the result to be true.

**Example:**
- P = "I have money" (TRUE)
- Q = "The store is open" (TRUE)
- P ∧ Q = "I have money AND the store is open" (TRUE)

If either one is false, the whole thing is false.

#### 3. OR (Disjunction) - Symbol: ∨
At least one thing must be true for the result to be true.

**Example:**
- P = "I can pay with cash" (FALSE)
- Q = "I can pay with card" (TRUE)
- P ∨ Q = "I can pay with cash OR card" (TRUE)

#### 4. XOR (Exclusive OR) - Symbol: ⊕
Only one can be true, not both.

**Example:**
- Like a door - it's either open OR closed, not both!

#### 5. IMPLIES (Implication) - Symbol: →
"If P, then Q"
- P → Q means: If P is true, then Q must be true
- Example: "If it rains (P), then the ground is wet (Q)"
- This is only false when P is true but Q is false

#### 6. BICONDITIONAL (If and only if) - Symbol: ↔
Both must have the same truth value.

**Example:**
- P ↔ Q means: P is true exactly when Q is true
- Like "You pass the exam if and only if you score 50% or above"

### Truth Tables
Truth tables show all possible combinations of true/false values and their results. Think of it as a multiplication table but for logic!

#### Example for AND (∧):
| P | Q | P ∧ Q | Explanation |
|---|---|-------|-------------|
| T | T | T | Both true = True |
| T | F | F | One false = False |
| F | T | F | One false = False |
| F | F | F | Both false = False |

#### Example for OR (∨):
| P | Q | P ∨ Q | Explanation |
|---|---|-------|-------------|
| T | T | T | At least one true = True |
| T | F | T | At least one true = True |
| F | T | T | At least one true = True |
| F | F | F | All false = False |

### Java Logical Operators
In programming (specifically Java), we use these operators:

#### && (AND)
```java
boolean hasTicket = true;
boolean gateIsOpen = true;
boolean canEnter = hasTicket && gateIsOpen;  // TRUE
```

#### || (OR)
```java
boolean isMember = false;
boolean hasCoupon = true;
boolean getDiscount = isMember || hasCoupon;  // TRUE
```

### ! (NOT)
```java
boolean isRaining = true;
boolean isSunny = !isRaining;  // FALSE
```

**Short-Circuit Evaluation:** Java is smart! With &&, if the first part is false, it doesn't even check the second part (because the result will be false anyway). Same with ||, if the first part is true, it stops checking.

### Simple Propositions vs Compound Propositions

#### Simple Propositions (Atomic Propositions)
A simple proposition is a single statement that cannot be broken down into smaller statements. It's like an atom - the smallest unit!

**Characteristics:**
- Contains NO logical connectives (no AND, OR, NOT, etc.)
- Makes one single claim
- Can only be true or false
- Cannot be divided further

**Examples:**
- "The sky is blue" → Simple
- "Lagos is in Nigeria" → Simple
- "5 is greater than 3" → Simple
- "It is raining" → Simple
- "Miva is an open university" → Simple

We usually represent simple propositions with single letters:
- P = "It is raining"
- Q = "The ground is wet"
- R = "I will carry an umbrella"

#### Compound Propositions (Molecular Propositions)
A compound proposition is formed by combining two or more simple propositions using logical connectives. It's like a molecule made of atoms!

**Characteristics:**
- Contains logical connectives (AND, OR, NOT, IMPLIES, etc.)
- Made up of two or more simple propositions
- Can be broken down into smaller parts
- Truth value depends on the simple propositions and connectives used

**Examples:**
- It is raining **AND** the ground is wet
- I will study **OR** I will fail
- It is **NOT** snowing
- IF you study hard, **THEN** you will pass
- The car is red **OR** blue, **AND** it is fast


### What are De Morgan's Laws?
De Morgan's Laws are two rules that show you how to correctly distribute the NOT operator over AND and OR statements. They're named after Augustus De Morgan, a mathematician who formalized these rules. It is a powerful tool used to simplify complex conjunctions in propositional logic.

### The Two Laws

#### Law 1: NOT (P AND Q)
**Formula:** ¬(P ∧ Q) ≡ ¬P ∨ ¬Q

**In plain English:** "NOT (P AND Q)" is the same as "(NOT P) OR (NOT Q)"

**What it means:** When you say something is NOT (both A and B), you're saying either A is false OR B is false (or both are false).

#### Law 2: NOT (P OR Q)
**Formula:** ¬(P ∨ Q) ≡ ¬P ∧ ¬Q

**In plain English:** "NOT (P OR Q)" is the same as "(NOT P) AND (NOT Q)"

**What it means:** When you say something is NOT (A or B), you're saying both A is false AND B is false.

### Truth Assignments and Environments
This is just a fancy way of saying: "Give each variable a value, then calculate the result."

**Example:** If P = TRUE, Q = TRUE, R = FALSE What is: (NOT(P AND Q)) OR (R XOR NOT(Q))?

Let's solve it step by step:
1. P AND Q = TRUE AND TRUE = TRUE
2. NOT(P AND Q) = NOT(TRUE) = FALSE
3. NOT(Q) = NOT(TRUE) = FALSE
4. R XOR NOT(Q) = FALSE XOR FALSE = FALSE
5. FALSE OR FALSE = FALSE

### Logical Equivalence
Two formulas are equivalent if they always give the same result, no matter what values you plug in.

### Important Equivalences to Remember

#### 1. De Morgan's Laws (Super important!)
- NOT(P AND Q) = (NOT P) OR (NOT Q)
- NOT(P OR Q) = (NOT P) AND (NOT Q)

#### 2. Double Negation
- NOT(NOT P) = P

#### 3. Material Implication
- (P → Q) = (NOT P) OR Q

#### 4. Distributive Laws
- P AND (Q OR R) = (P AND Q) OR (P AND R)
- P OR (Q AND R) = (P OR Q) AND (P OR R)

#### 5. Absorption Laws
- P OR (P AND Q) = P
- P AND (P OR Q) = P

### Satisfiability
A proposition is satisfiable if there's at least ONE way to make it true.

**Example: (P OR Q) is satisfiable because:**
- When P = TRUE, Q = FALSE → Result is TRUE ✓

A proposition is unsatisfiable if there's NO way to make it true (it's always false).
**Example: (P AND NOT P) is unsatisfiable because:**
- P can't be both true and false at the same time!

**NB:** A tautology is a statement that is always true, no matter the truth value of its variables.





----

**Disclaimer:** These notes are intended for learning and revision purposes only and may simplify certain concepts. They must not be used for exam malpractice or any form of academic dishonesty. Use of these notes is entirely the responsibility of the student, and official course materials should be consulted for authoritative guidance.
