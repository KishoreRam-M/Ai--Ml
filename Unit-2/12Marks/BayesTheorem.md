## **Theorem 1: Bayesian Inference (Updating Beliefs)**

**Statement:**

> Bayesian inference is a method to **update your belief about an event** when new evidence is available.

**Given:**

* Prior belief about an event (how likely it is before new information).
* Evidence or observed data related to the event.

**Then:**

* Update the belief to form a **posterior probability** that reflects both the prior and the new evidence.

**In simple terms:**

> Posterior = Prior belief × How likely the evidence is if the event happens ÷ How likely the evidence is overall

**Example:**

* Prior: 50% chance it will rain today.
* Evidence: dark clouds appear.
* Posterior: Updated chance of rain = 80%.

---

## **Theorem 2: Bayes Rule**

**Statement:**

> Bayes Rule is the **formula behind Bayesian inference** that mathematically combines prior belief and evidence.

**Formula (in words):**

> Probability of Event A given Evidence B =
> Probability of seeing Evidence B if A is true × Probability of A ÷ Probability of B

**Explanation:**

* Prior = Probability of A before seeing B
* Likelihood = Probability of B if A is true
* Evidence probability = Probability of B happening overall
* Posterior = Updated probability of A after seeing B

**Example:**

* Prior: 10% of emails are spam
* Likelihood: “free” appears in 70% of spam emails
* Posterior: Updated chance that an email with “free” is spam

---

## **Theorem 3: Naive Bayes Model**

**Statement:**

> Naive Bayes uses Bayes Rule to **classify items** based on features, assuming the features are **independent**.

**Given:**

* Features of an item (e.g., words in an email).
* Classes for classification (e.g., Spam or Not Spam).

**Then:**

* Calculate probability of each class given the features.
* Select the class with the **highest probability**.

**Steps (Simple Words):**

1. Compute **prior probability** for each class (how common each class is).
2. Compute **likelihood** for each feature given each class.
3. Multiply likelihoods for all features (assuming independence).
4. Multiply by prior probability.
5. Choose the class with **highest resulting probability**.

**Example (Email Spam):**

* Email words: “free”, “money”, “offer”
* Classes: Spam, Not Spam
* Naive Bayes calculates probabilities for each class and **classifies as Spam** if probability is higher

---

### **Summary Table (Beginner-Friendly)**

| Concept            | Meaning                                                        |
| ------------------ | -------------------------------------------------------------- |
| Bayesian Inference | Update beliefs with new evidence                               |
| Prior              | Initial belief before seeing evidence                          |
| Evidence           | New information observed                                       |
| Posterior          | Updated belief after considering evidence                      |
| Bayes Rule         | Formula combining prior and evidence                           |
| Naive Bayes        | Classifier using Bayes Rule, assuming features are independent |

---

## **Theorem 1: Bayes’ Theorem**

**Statement:**

> Bayes’ Theorem provides a way to **update the probability of an event** based on new evidence.

**Formula:**

$$
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
$$

**Where:**

* $P(A|B)$ = Posterior probability (probability of A after observing B)
* $P(B|A)$ = Likelihood (probability of observing B if A is true)
* $P(A)$ = Prior probability (initial belief about A)
* $P(B)$ = Probability of evidence B

**Example:**

* A = “Email is spam”
* B = “Email contains the word ‘free’”
* Then $P(Spam|‘free’)$ = $\frac{P(‘free’|Spam) \cdot P(Spam)}{P(‘free’)}$

---

## **Theorem 2: Naive Bayes Classifier**

**Statement:**

> The Naive Bayes model uses Bayes’ Theorem to **classify items into categories** assuming all features are independent.

**Formula for a class $C_k$ given features $x_1, x_2, ..., x_n$:**

$$
P(C_k \mid x_1, x_2, ..., x_n) = \frac{P(C_k) \cdot \prod_{i=1}^{n} P(x_i \mid C_k)}{P(x_1, x_2, ..., x_n)}
$$

**Where:**

* $C_k$ = A possible class (e.g., Spam or Not Spam)
* $x_1, x_2, ..., x_n$ = Features of the item (e.g., words in an email)
* $P(C_k)$ = Prior probability of class $C_k$
* $P(x_i|C_k)$ = Probability of feature $x_i$ given class $C_k$
* Denominator $P(x_1, ..., x_n)$ = Normalizing constant (can be ignored for comparison)

**Decision rule (choose class with highest probability):**

$$
\hat{C} = \arg\max_{C_k} P(C_k) \cdot \prod_{i=1}^{n} P(x_i \mid C_k)
$$

**Example:**

* Email words = “free”, “money”, “offer”
* Classes = Spam, Not Spam
* Naive Bayes computes probabilities for each class and chooses the class with **highest probability** → predicts **Spam**

---

✅ **Summary:**

* **Bayes’ Theorem** = Update probability based on evidence
* **Naive Bayes** = Classify items using Bayes’ Theorem + independent features assumption
