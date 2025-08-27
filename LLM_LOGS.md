# LLM Usage Log — Selected Chat Excerpts

This file documents how I used ChatGPT (GPT-5) as a **support tool** during this assignment.  
Scope of help: clarifying coding details, Docker/Jupyter setup, and Git/GitHub troubleshooting.  
I structured the exercise, wrote/edited the learning objectives/instructions, and curated the final notebook and repo.

> Sensitive tokens/links are **redacted** like `[REDACTED]`.

---

## Day 1 — August 25, 2025

### Session 1 — Softmax implementation details
**Prompt (me):**  
“I need to implement a numerically stable softmax that supports both vectors and batches. How should I handle 1D vs 2D arrays?”

**Assistant (excerpt):**
```text
Use the max-shift trick for stability. For 1D: subtract np.max(x). For 2D: subtract row-wise max with keepdims=True, then normalize along axis=1.
```

---

### Session 2 — Unit tests and pedagogy
**Prompt (me):**  
“What tests should I include so learners know if their solution is correct?”

**Assistant (excerpt):**
```text
Check that probabilities sum to 1, outputs are non-negative, and shapes match input. Optionally test invariance to adding a constant shift.
```

---

### Session 3 — Notebook structure
**Prompt (me):**  
“I want the notebook to feel like a DeepLearning.AI lab. How should I order the sections?”

**Assistant (excerpt):**
```text
Use: Title → Learning Objectives → Background → Instructions → Scaffolded code → Tests → Try it yourself → Instructor solution.
```

---

## Day 2 — August 26, 2025

### Session 4 — Docker/Jupyter setup
**Prompt (me):**  
“Help me write a Dockerfile so that running `docker run` automatically starts JupyterLab.”

**Assistant (excerpt):**
```text
Start from python:3.11-slim, install jupyterlab, expose 8888, and launch with:
--ip=0.0.0.0 --port=8888 --no-browser --ServerApp.token= --allow-root
```

---

### Session 5 — Git/GitHub troubleshooting
**Prompt (me):**  
“I’m getting 403 errors when pushing. What’s the right sequence of git commands?”

**Assistant (excerpt):**
```text
git init
git branch -M main
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/<username>/ce-softmax.git
git push -u origin main
```

---

### Session 6 — README polish
**Prompt (me):**  
“My README isn’t rendering well. How can I make it clearer?”

**Assistant (excerpt):**
```text
Separate code blocks for Python vs Bash, close fences properly, and add clear headings: Docker Commands, Goal, Learning Objectives, Instructions, Repo Structure.
```

---

## Notes  
- All secrets (tokens, personal info) are redacted.  
- The assistant was used for **targeted support**; the final content, pedagogy, and structure were curated by me.

