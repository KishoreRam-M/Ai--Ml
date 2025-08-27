## 🧠 What is a Bayesian Network?

A **Bayesian Network** (also known as a **Belief Network**) is a graphical model that represents the probabilistic relationships among a set of variables. It allows us to model uncertainty and make predictions or decisions based on probabilities.

---

## 🧩 Components of a Bayesian Network

A Bayesian Network consists of:

1. **Nodes**: Each node represents a random variable, which can be discrete or continuous.
2. **Edges (Arrows)**: Directed edges between nodes represent conditional dependencies. An edge from node A to node B indicates that A has a direct influence on B.
3. **Conditional Probability Tables (CPTs)**: Each node has a CPT that quantifies the effect of the parents' nodes on the node itself.

---

## 🔄 How It Works

* **Joint Probability Distribution**: The joint probability distribution of all variables in the network is expressed as the product of the conditional probabilities of each variable given its parents:

  $$
  P(X_1, X_2, \dots, X_n) = \prod_{i=1}^{n} P(X_i | \text{Parents}(X_i))
  $$

* **Inference**: Given some observed evidence, Bayesian Networks can compute the posterior probabilities of other variables. This is done using inference algorithms like Variable Elimination or Junction Tree Algorithm.

---

## 🎯 Applications

Bayesian Networks are widely used in various fields, including:

* **Medical Diagnosis**: Modeling the probabilistic relationships between diseases and symptoms.
* **Risk Assessment**: Evaluating the likelihood of different risk factors leading to an adverse event.
* **Decision Support Systems**: Aiding in making informed decisions under uncertainty.

