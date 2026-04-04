

## Task 1: The Problem

### What can go wrong?
- Developers can break each other's code
- Merge conflicts can happen often
- Manual deployment can cause human mistakes
- Bugs can go to production without testing
- Rollback is difficult

---

### "It works on my machine" — what it means
It means the code works on the developer’s computer but not on another system or server.

**Why this happens:**
- Different operating system
- Different software versions
- Different environment setup

👉 This is a real problem because the app can fail in production.

---

### Manual deployment limit
- Safe: 1–2 times per day
- More deployments = more chances of errors

---

## Task 2: CI vs CD

### Continuous Integration (CI)
- Developers push code frequently
- Every push runs automatic build and tests
- Bugs are found early

**Example:**
Developer pushes code → tests run automatically → error found → fix before merge

---

### Continuous Delivery (CD)
- Code is automatically built and tested
- Code is ready to deploy anytime
- But deployment is done manually

**Example:**
App is ready, but team clicks a button to deploy

---

### Continuous Deployment
- Everything is automatic
- If tests pass, code goes directly to production

**Example:**
Push code → tests pass → app is live

---

## Task 3: Pipeline Anatomy

### Trigger
- What starts the pipeline
- Example: code push

---

### Stage
- A phase in pipeline
- Example: Build, Test, Deploy

---

### Job
- A task inside a stage
- Example: run tests

---

### Step
- A single command
- Example: install dependencies

---

### Runner
- Machine that runs the job
- Example: GitHub Actions runner

---

### Artifact
- Output of a job
- Example: build files or Docker image

---

## Task 4: CI/CD Pipeline Diagram
