#  Word Embeddings & Debiasing

This project contains Python functions implemented for Natural Language Processing (NLP) tasks, focusing on evaluating cosine similarity between word vectors, performing word analogies, and mitigating biases (such as gender bias) in word embeddings.

---

##  Core Components & Functions

The main tasks implemented in this project include:

### 1. `cosine_similarity`
* **Description:** Evaluates the degree of similarity between two word vectors ($u$ and $v$) using the cosine similarity formula.
* **Feature:** Accurately measures directional alignment regardless of the magnitude or scale of the vectors.

### 2. `complete_analogy`
* **Description:** Solves logical word analogy tasks based on the relation: "A is to B as C is to what?" ($a \to b :: c \to ?$ ).
* **Mechanism:** Compares vector differences (`e_b - e_a` and `e_w - e_c`) to find the word with the highest cosine similarity.

### 3. `neutralize`
* **Description:** Neutralizes gender-neutral words (such as "receptionist" or "scientist") by removing their projection onto the gender bias axis.
* **Mechanism:** Projects the word vector onto the subspace orthogonal to the bias axis.

### 4. `equalize`
* **Description:** Adjusts pairs of gender-specific words (e.g., "man" - "woman", "actor" - "actress") to ensure they are equidistant from the neutral axis while remaining properly normalized.

---

##  Technologies Used
* **Python**
* **NumPy** (For vector and matrix operations)
* **tqdm** (For progress tracking)

---
