## Predicate Logic

### What is Predicate Logic?
Think of predicate logic as a more powerful version of regular logic. In regular logic, we can only say things like "It is raining" (true or false). But in predicate logic, we can talk about properties of things and relationships between things.

A **predicate** is basically a statement that contains variables. For example:
- P(x) = "x is a student"
- Q(x) = "x is tall"
- R(x, y) = "x is taller than y"

The variable (x, y, etc.) is like a blank space that you can fill in with actual values.

### What are Quantifiers?
Quantifiers tell us how many things we're talking about. There are two main types:

#### 1. Universal Quantifier (∀) - "For All"
The symbol ∀ means "for all" or "for every." It's used when a statement is true for ALL elements in a group.

**How to read it:**
- ∀x P(x) reads as: "For all x, P(x) is true"
- Or: "Every x has property P"

**Real-life examples:**
Example 1: "All students must pay school fees"
- Let P(x) = "x must pay school fees"
- We write: ∀x P(x)
- This means: Every single student must pay fees

Example 2: "Every human being needs water to survive"
- Let Q(x) = "x needs water to survive"
- We write: ∀x Q(x)
- Domain: All human beings

Example 3: In mathematics - "All even numbers are divisible by 2"
- Let R(x) = "x is divisible by 2"
- We write: ∀x R(x)
- Domain: All even numbers

**Important note:** If even ONE element doesn't satisfy the condition, the whole statement becomes FALSE.

#### 2. Existential Quantifier (∃) - "There Exists"
The symbol ∃ means "there exists" or "there is at least one." It's used when a statement is true for AT LEAST ONE element in a group.

**How to read it:**
- ∃x P(x) reads as: "There exists an x such that P(x) is true"
- Or: "There is at least one x that has property P"
- Or: "For some x, P(x) is true"

**Real-life examples:**
Example 1: "Some students have scholarships"
- Let P(x) = "x has a scholarship"
- We write: ∃x P(x)
- This means: At least one student has a scholarship

Example 2: "There is a student who scored 100% in the exam"
- Let Q(x) = "x scored 100% in the exam"
- We write: ∃x Q(x)
- This means: At least one student achieved this

Example 3: In mathematics - "There exists a prime number greater than 100"
- Let R(x) = "x is a prime number greater than 100"
- We write: ∃x R(x)
- This is TRUE (because 101, 103, etc. exist)

**Important note:** If at least ONE element satisfies the condition, the whole statement becomes TRUE.

### Key Differences

| Feature | Universal (∀) | Existential (∃) |
|---------|---------------|----------------|
| Meaning | ALL elements must satisfy | AT LEAST ONE element must satisfy |
| Keywords | "Every," "All," "Each" | "Some," "There exists," "At least one" |
| Truth Condition | If one fails, statement is FALSE | If one succeeds, statement is TRUE |


### Domain
The domain (also called "universe of discourse") is the complete set of things you're allowed to talk about. When you use quantifiers like ∀ (for all) or ∃ (there exists), you're ONLY talking about things inside your domain. Change the domain, and the truth value of your statement can completely flip.

#### Example 1: "All students are female"
- Your domain contains: {Mary, Jane, Sarah, Elizabeth, ...}
- All of these students are female
- So "∀x Female(x)" is TRUE because EVERY element in your domain is female

#### Example 2: "Students in a mixed school"
- Your domain contains: {Mary, John, Sarah, Michael, Jane, David, ...}
- Some students are male (John, Michael, David)
- So "∀x Female(x)" is FALSE because NOT every element in your domain is female






