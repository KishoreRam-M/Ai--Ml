## **1. Uncertain Knowledge**

* **Definition:** Knowledge is uncertain when we **don’t know the outcome for sure** because information is incomplete or imperfect.
* **Example:** A doctor may not be 100% sure if a patient has a disease based on symptoms alone.

---

## **2. Prior Probability**

* **Definition:** The **initial belief** about an event before seeing any new evidence.
* **Example:** If 10% of emails are spam in a dataset, the prior probability of spam is 0.1.

---

## **3. Conditional Probability**

* **Definition:** The probability of an event **given that another event has occurred**.
* **Notation:** $P(A|B)$ = probability of A given B.
* **Example:** Probability an email is spam **given** that it contains the word “free”.

---

## **4. Bayes’ Theorem**

**Statement:** Bayes’ theorem is a formula to **update your belief about an event** after seeing new evidence.

**Formula:**

$$
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
$$

**Where:**

* $P(A|B)$ = Posterior probability (updated belief)
* $P(B|A)$ = Likelihood (chance of evidence if A is true)
* $P(A)$ = Prior probability
* $P(B)$ = Probability of the evidence

**Example:**

* Prior: 10% of emails are spam
* Evidence: Email contains “free”
* Posterior: Updated probability of spam after seeing “free”

---

## **5. How Bayes’ Theorem Helps in Decision Making under Uncertainty**

* Provides a **structured way to update beliefs** with new information.
* Helps **make better decisions** when outcomes are not certain.
* Example:

  * Doctor estimates probability of disease using prior statistics and patient symptoms.
  * Investor updates belief about stock performance after new market data.

---

## **6. Belief Networks (Bayesian Networks)**

* **Definition:** A graphical model that represents **uncertain knowledge** using **nodes and connections**.
* **Nodes** = variables (like symptoms, diseases)
* **Edges** = dependencies between variables
* Shows how **one piece of evidence affects others**.
* Useful for reasoning under uncertainty, e.g., diagnosing disease given multiple symptoms.

**Example:**

* Node: Fever, Cough, Flu
* Connection: Fever and Cough → Flu
* If you observe Fever and Cough, the network calculates the probability of Flu.

---

✅ **Quick Summary:**

* **Uncertain knowledge:** incomplete or imperfect info
* **Prior probability:** initial belief
* **Conditional probability:** probability given evidence
* **Bayes’ theorem:** updates beliefs based on evidence
* **Belief networks:** graphically show how variables influence each other

---

If you want, I can **draw a simple visual diagram of a belief network with Bayes updating**, which makes it **super easy to remember** for exams.

Do you want me to do that?
