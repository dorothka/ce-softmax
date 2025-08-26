# Softmax Layer Exercise (with Batch Support & Numerical Stability)

This repository contains a coding exercise for learners to implement a numerically stable **softmax** function in Python using NumPy.  
It was created as part of a Curriculum Engineer assignment.

---

## 🎯 Goal
Implement a numerically stable softmax function that works for both a single vector of logits and a batch of logits.

---

## 🎯 Learning Objectives
By completing this exercise, learners will:  

- **Understand the role of softmax** in neural networks and why it is used to convert raw scores (logits) into probabilities.  
- **Implement the softmax function** in Python using NumPy, both for single vectors (1D arrays) and for batches of data (2D arrays).  
- **Apply numerical stability techniques** by subtracting the maximum logit before exponentiation to prevent overflow errors.  
- **Verify correctness** of the implementation with simple unit tests that check properties like “outputs sum to 1” and “softmax is invariant to constant shifts.”  
- **Practice debugging and testing skills** by interpreting failed tests and fixing implementation mistakes.  
- Build confidence in working with **array operations, broadcasting, and vectorization** in NumPy.  

---

## 📋 Instructions for Learners
Open the notebook `softmax_exercise.ipynb` and complete the function:

```python
def softmax(x: np.ndarray) -> np.ndarray:
    # your code here
    raise NotImplementedError("Implement the softmax function")

---

## 🐳 Docker Commands

After cloning the repository, build the Docker image and run JupyterLab as follows:

```bash
git clone https://github.com/<your-username>/ce-softmax.git
cd ce-softmax
docker build -t ce-softmax .
docker run --rm -p 8888:8888 -v $(pwd):/workspace ce-softmax

