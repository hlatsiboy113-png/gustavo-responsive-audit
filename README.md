# Understanding Git & Developer Communication: What I Wish I Knew Early

## Introduction
I had no web development knowledge when I started the iHub Web Development Program - I only knew of the concepts of HTML, JavaScript, Python and CSS. Neverknew of the various collaboration tools that existed, I initially thought tools like Git, GitHub, and VS Code were all part of the same system. I followed commands with guidance from AI, the lectures and Google without understanding their purpose, which led to confusion—especially when working in team environments.

Over time, I realized that both technical understanding (Git) and communication play a critical role in how effectively developers collaborate.

This document covers:
- Core Git learnings
- Real-world communication scenarios in development teams
- The professional impact of communication in software environments

---

## Learning 1: Git vs GitHub vs VS Code vs Git Bash

### Key Distinction

- Git → Version control system (tracks changes locally)  
- GitHub → Remote platform for collaboration  
- VS Code → Code editor where development happens  
- Git Bash → Tool to run Git commands  
- Bash → Command-line environment  

### Why This Matters
Understanding these roles prevents confusion when:
- Debugging errors  
- Managing branches  
- Collaborating with others  

### Example Workflow
1. Write code in VS Code  
2. Track changes using Git  
3. Run commands in Git Bash  
4. Push to GitHub for collaboration  

---

## Learning 2: The Staging Area Is a Filter

- Git staging allows selective commits  
- Prevents messy commit history  
- Improves debugging  

### Key Practice
Avoid:
git add .

Instead:
- Stage only relevant files  
- Keep commits focused  

---

## Learning 3: Branching Enables Safe Development

- Branches isolate work  
- Prevent breaking stable code  

### Example
git checkout -b feature/login

### Key Practice
- One branch per feature  
- Keep main stable  

---

## Learning 4: Pull Requests Are Communication

Pull Requests (PRs) are not just for merging—they are communication tools.

### Good PR Includes:
- What changed  
- Why it changed  
- How to test  

### Example
## What this PR does
- Adds login validation

## How to test
- Enter invalid email
- Check error message

---

## Learning 5: Merge Conflicts Require Decision-Making

Merge conflicts happen when Git cannot decide between changes.

### Key Practice
- Read both versions  
- Understand intent  
- Resolve carefully  

---

# Developer Communication Scenarios

## Scenario 1: Miscommunication in Slack About a Bug

### Situation  
A developer notices a bug in production but sends a vague Slack message:
"The site is broken."

### Problem  
- No context provided  
- No steps to reproduce  
- No urgency level  

### Improved Communication  
"🚨 Bug on checkout page  
Issue: Payment button not responding  
Steps: Add item → Go to checkout → Click pay  
Expected: Payment processes  
Actual: No response  
Priority: High (affects transactions)"

### Cause-and-Effect  
- Clear message → Faster team response  
- Specific details → Easier debugging  
- Defined priority → Better task management  

---

## Scenario 2: Poorly Written GitHub Pull Request

### Situation  
A developer submits a PR on GitHub with the description:
"Updated stuff"

### Problem  
- No explanation of changes  
- Reviewers must read all code manually  
- Slows down approval process  

### Improved PR Example  
## What this PR does
- Refactors login validation logic
- Fixes email format bug

## Why
- Previous validation allowed invalid emails

## How to test
- Enter invalid email format
- Ensure error message displays

### Cause-and-Effect  
- Clear PR → Faster reviews  
- Less back-and-forth → Increased productivity  
- Better documentation → Easier future maintenance  

---

## Scenario 3: Task Misalignment in ClickUp

### Situation  
A developer receives a task in ClickUp:
"Fix UI issue"

### Problem  
- No design reference  
- No acceptance criteria  
- No clarity on expected outcome  

### Improved Task Description  
Task: Fix navbar alignment on mobile  
Details: Navbar overlaps logo on screens < 768px  
Expected Outcome: Proper spacing and alignment  
Reference: Figma design link  
Priority: Medium  

### Cause-and-Effect  
- Clear task → Correct implementation  
- Defined expectations → Less rework  
- Proper references → Faster completion  

---

# Professional Implications of Communication

## 1. Communication Builds or Breaks Trust
Clear and structured communication:
- Shows professionalism  
- Builds reliability within a team  

Poor communication:
- Creates confusion  
- Reduces confidence in your work  

Impact: Developers who communicate clearly are trusted with more responsibility.

---

## 2. Communication Directly Affects Team Efficiency
Good communication:
- Reduces unnecessary back-and-forth  
- Speeds up development cycles  
- Improves collaboration  

Poor communication:
- Causes delays  
- Leads to repeated mistakes  
- Increases frustration in teams  

Impact: Teams with strong communication ship faster and produce higher-quality software.

---

# Conclusion

Technical skills alone are not enough in software development.

Understanding:
- Git workflows  
- Tool responsibilities  
- Clear communication practices  

is what separates a beginner from a professional developer.

---

# Author
Mahlatse Mokgawa  
Date: 26 April 2026  

---

# Tags
#Git #GitHub #WebDevelopment #SoftwareEngineering #Communication #DeveloperSkills


