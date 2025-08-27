# First-Order Logic (FOL) Step-by-Step Guide

## Step 0: What is First-Order Logic (FOL)?
FOL is a way to describe things and rules clearly.

| Symbol | Meaning |
|--------|---------|
| ∃      | "there is at least one" → somebody exists |
| ∀      | "for all" → everybody or everything |
| →      | "if … then …" → a rule or promise |
| ∧      | "and" → both things are true |
| ¬      | "not" → something is not true |
| =      | "is the same as" → same thing |

---

## Step 1: The Predicate Format
**Example:** `Took(x, French, s)` is a predicate.

- **x** → the student (the “who”)  
- **French** → the course (the “what”)  
- **s** → the semester (the “when”)  

**In words:** "x took French in semester s"  

**Example:**  
```

x = Alice
s = Spring 2021
Took(Alice, French, Spring2021) → "Alice took French in Spring 2021" ✅

```

**Why we need it:**  
This predicate shows facts about the student, e.g., "If someone is a student and they took French, then they pass French."

---

## Step 2: Some students took French in Spring 2001
**Idea:** At least one student attended French class.

**FOL:**  
```

∃ x (Student(x) ∧ Took(x, French, Spring2001))

```

**Example:** Alice is a student → Alice went to French class ✅

---

## Step 3: Every student who takes French passes it
**Idea:** If a student takes French, they always pass.

**FOL:**  
```

∀ x (Took(x, French, s) → Passes(x, French))

```

**Example:**  
- Bob takes French → Bob passes it ✅  
- Sam takes French → Sam passes it ✅

---

## Step 4: Only one student took Greek in Spring 2001
**Idea:** Exactly one student went to Greek.

**FOL:**  
```

∃ x (Took(x, Greek, Spring2001) ∧ ∀ y (Took(y, Greek, Spring2001) → y = x))

```

**Example:** Charlie is the only student in Greek class ✅

---

## Step 5: The best score in Greek is always higher than the best score in French
**Idea:** Greek always has a higher top score than French.

**FOL:**  
```

∀ s (BestScore(Greek, s) > BestScore(French, s))

```

**Example:** Greek top score = 95, French top score = 90 ✅

---

## Step 6: Everyone who buys a policy is smart
**Idea:** If someone buys insurance, they are smart.

**FOL:**  
```

∀ x ∀ p (Buys(x, p) → Smart(x))

```

**Example:** David buys insurance → David is smart ✅

---

## Step 7: No person buys an expensive policy
**Idea:** Nobody buys very expensive insurance.

**FOL:**  
```

∀ x ∀ p (Expensive(p) → ¬Buys(x, p))

```

**Example:** Expensive policy costs $1000 → nobody buys it ✅

---

## Step 8: There is an agent who sells only to people not insured
**Idea:** One agent sells insurance only to people without insurance.

**FOL:**  
```

∃ a ∀ x ∀ p (Sells(a, p, x) → ¬Insured(x))

```

**Example:** Agent Anna sells to John (not insured) ✅

---

## Step 9: There is a barber who shaves all men who don’t shave themselves
**Idea:** A barber shaves every man who doesn’t shave himself.

**FOL:**  
```

∃ b ∀ x ((Man(x) ∧ ¬Shaves(x, x)) → Shaves(b, x))

```

**Example:** Mike doesn’t shave → barber shaves Mike ✅
```

I can also **add simple diagrams/pictures** for predicates like `Took(x, French, s)` or the barber problem to make it visually intuitive for exams.

Do you want me to create those diagrams next?
