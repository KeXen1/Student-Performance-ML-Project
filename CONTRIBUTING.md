# Contributing Guide

This document explains how we collaborate on this project. Read it before pushing any code.

---

## Git Workflow

We use a feature-branch workflow. Nobody pushes directly to main.

### Step-by-step for every task:

Pull the latest main branch first:

git checkout main  
git pull origin main  

Create a branch for your work:

git checkout -b dev/your-module-name  

Use branch names listed in the README (e.g., dev/preprocessing, dev/model-training, dev/evaluation).

Do your work. Write code, test it, make sure it runs correctly.

Commit with a clear message:

git add .  
git commit -m "Add data preprocessing with encoding and scaling"  

Good commit messages describe what you did, not that you did something.

Good: "Add Random Forest model with cross-validation"  
Bad: "updated files" or "stuff"  

Push your branch:

git push origin dev/your-module-name  

Open a Pull Request (PR) on GitHub:

- Go to the repo on GitHub  
- You'll see a banner saying your branch was recently pushed → click Compare & pull request  
- Title: what the PR does (e.g., "Add model training notebook and results")  
- Description: briefly explain what you implemented and what results to check  
- Assign a reviewer  
- Wait for review before merging into main  

---

## Code Standards

### File naming

Notebooks: notebooks/01_data_preprocessing.ipynb  
Scripts (if used): scripts/module_name.py  
Models: models/model_name.pkl  
Plots: results/plots/plot_description.png  

---

### Python / Notebook style

- Use clear, descriptive variable names (e.g., X_train, y_pred)  
- Keep notebooks organized:
  - Data loading  
  - Preprocessing  
  - Training  
  - Evaluation  
- Add comments for important steps, not obvious ones  
- Avoid hardcoding file paths specific to your machine  

---

### Notebook Requirements

Every major step should have its own notebook:
- Data preprocessing  
- Feature selection  
- Model training  
- Model evaluation  

Each notebook should:
- Run from top to bottom without errors  
- Include outputs (plots, metrics)  
- Have short explanations in markdown cells  

---

## Visualizations

When creating plots:

- Use clear titles and axis labels  
- Keep graphs readable  
- Save important plots to results/plots/  
- Use descriptive file names  

Example:  
model_accuracy_comparison.png  

---

## If You Hit a Merge Conflict

Don't panic. This usually means two people edited the same file.

git checkout main  
git pull origin main  
git checkout dev/your-branch  
git merge main  

# Fix conflicts in your editor (look for <<<<<<< markers)

git add .  
git commit -m "Resolve merge conflict with main"  
git push origin dev/your-branch  

If you're stuck, ask the team.

---

## Questions?

Ask in the group chat before spending hours stuck on something.
