## Predicate Logic

### What is Predicate Logic?
Predicate logic (also called first-order logic) is an extension of propositional logic. While propositional logic deals with complete statements that are simply true or false, predicate logic lets us look inside statements to examine their structure.

**Key difference:**
**- Propositional logic:** "John is tall" is just one statement (true or false)
**- Predicate logic:** "John is tall" breaks into "x is tall" where x = John

### Predicate
A predicate is a property or relation that describes something about an object. Think of it as a function that returns true or false.

Examples:
- P(x) = "x is a student"
- Q(x) = "x is tall"
- R(x, y) = "x is taller than y"

The letters in parentheses are variables, they're placeholders for actual objects.

### Domain (Universe of Discourse)
The domain is the set of all possible values that variables can take. You must always specify the domain.

Example: If we say P(x) = "x is even"
- Domain could be: all integers, all natural numbers, or just {1, 2, 3, 4, 5}

### Propositional Functions
When you have a predicate with variables like P(x), it's called a **propositional function** because it becomes a proposition (true or false) once you substitute actual values for the variables.

Example:
- P(x) = "x > 5" (this is not true or false yet)
- P(7) = "7 > 5" = True (now it's a proposition)
- P(3) = "3 > 5" = False (also a proposition)

### QUANTIFIERS
Quantifiers are symbols that tell us "how many" objects in the domain satisfy a predicate. There are two main types.

#### 1. Universal Quantifier (∀)

**Symbol:** ∀ (read as "for all" or "for every")

**Meaning:** The predicate is true for every element in the domain.

**Format:** ∀x P(x) Read as: "For all x, P(x)" or "For every x, P(x) is true"

**Examples:**
- Let P(x) = "x is mortal" and domain = all humans. ∀x P(x) means "All humans are mortal" ✓ (TRUE)
- Let Q(x) = "x is even" and domain = all integers. ∀x Q(x) means "All integers are even" ✗ (FALSE, because 3 is not even)
- Let R(x) = "x² ≥ 0" and domain = all real numbers. ∀x R(x) means "For all real numbers, the square is non-negative" ✓ (TRUE)

**Important:** ∀x P(x) is FALSE if even one element in the domain doesn't satisfy P(x). That one element is called a **counterexample.**

#### 2. Existential Quantifier (∃)

**Symbol:** ∃ (read as "there exists" or "for some")

**Meaning:** The predicate is true for at least one element in the domain.

**Format:** ∃x P(x) Read as: "There exists an x such that P(x)" or "For some x, P(x) is true"

**Examples:**
- Let P(x) = "x is prime" and domain = {1, 2, 3, 4, 5}. ∃x P(x) means "There exists a prime number in the set" ✓ (TRUE, because 2, 3, 5 are prime)
- Let Q(x) = "x < 0" and domain = all positive integers. ∃x Q(x) means "There exists a positive integer less than zero" ✗ (FALSE)
- Let R(x) = "x² = 16" and domain = all real numbers. ∃x R(x) means "There exists a real number whose square is 16" ✓ (TRUE, x = 4 or x = -4)

**Important:** ∃x P(x) is TRUE if at least one element satisfies P(x). It doesn't have to be all of them, just one or more.

### Translation from English
**Universal indicators:** all, every, each, any, none (none = "for all... not")

Examples:
- "All students study" → ∀x (Student(x) → Studies(x))
- "Every number is positive" → ∀x (Positive(x))
- "No cats are dogs" → ∀x (Cat(x) → ¬Dog(x))

**Existential indicators:** some, there exists, at least one, there is

Examples:
- "Some students are smart" → ∃x (Student(x) ∧ Smart(x))
- "There is a prime number" → ∃x (Prime(x))
- "At least one person passed" → ∃x (Passed(x))

### COMBINING QUANTIFIERS
You can use multiple quantifiers in one statement.

Example 1: ∀x ∃y (x < y)
- Domain: integers
- "For every integer x, there exists an integer y such that x < y"
- Meaning: Every integer has a larger integer (TRUE)

Example 2: ∃x ∀y (x ≤ y)
- Domain: positive integers
- "There exists an integer x such that for all integers y, x ≤ y"
- Meaning: There's an integer smaller than or equal to all others (TRUE, x = 1)

NB: Order matters! ∀x ∃y is different from ∃y ∀x

### NEGATION OF QUANTIFIERS

**Rules:**
- ¬(∀x P(x)) ≡ ∃x ¬P(x). "Not all x satisfy P" = "There exists an x that doesn't satisfy P"
- ¬(∃x P(x)) ≡ ∀x ¬P(x). "There doesn't exist an x that satisfies P" = "All x don't satisfy P"

Example 1:
- Statement: "All students passed" = ∀x Passed(x). Negation: "Not all students passed" = ∃x ¬Passed(x) which means "At least one student failed".
- Statement: "Some dogs are brown" = ∃x Brown(x). Negation: "No dogs are brown" = ∀x ¬Brown(x) which means "All dogs are not brown"

### NESTED QUANTIFIERS
When you have multiple quantifiers, read from left to right.

Example: ∀x ∃y (x + y = 0)
- Domain: integers
- Read: "For every integer x, there exists an integer y such that x + y = 0"
- Meaning: Every integer has an additive inverse (TRUE)

