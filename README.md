
#test from zheng

# VSCode-GitHub-and-Portfolio-Block1

## Overview

This first part of Block 1 introduces the tools and working environment that will be used throughout the course.

---

## Learning Objectives

### Basic Objectives

The following objectives are fundamental to the course. You are expected to complete the exercises to develop core technical proficiency.

- Set up VS Code, Git/GitHub, and the Python programming environment  
- Become familiar with procedures for accessing course materials and uploading your work to GitHub  

### Advanced Objectives

The following objectives contribute to the assessment, which involves creating and maintaining a GitHub profile. This will help you build a portfolio for future coursework and professional use.

- Create a GitHub profile `README.md` page using VS Code  
- Create Portfolio 1 for the Block 1 exercises  

---

## Learning Resources

You will need to download and install the following software.

### Visual Studio Code

- Download: https://code.visualstudio.com/Download

Recommended activities:
1. Explore core functions: https://code.visualstudio.com/docs  
2. Follow Python setup instructions: https://code.visualstudio.com/docs/python/python-quick-start  
3. Explore built-in and AI extensions: https://code.visualstudio.com/docs/intelligentapps/overview  

Recommended extensions:
- Python  
- Jupyter  
- GitHub Copilot  
- Markdown Shortcuts  
- Code Spell Checker  

### Python

Choose one distribution:
- Anaconda: https://www.anaconda.com/download  
- Miniconda: https://www.anaconda.com/docs/getting-started/miniconda/install  

### Git

- Download and install Git: https://git-scm.com/install  

### Video Resources (Optional)

- Geographic Software Design playlist:  
  https://www.youtube.com/@giswqs  

- Installing Visual Studio Code, Git, and Miniconda:  
  https://www.youtube.com/watch?v=9zmXL2ppves  

---

# Exercises 1

The following exercises should be completed during and after your engagement with the learning resources.

---

## Create a GitHub Profile Page (`README.md`)

### Step 1: Create the Repository on GitHub

Create a public repository that will act as your GitHub profile page.

Steps:
1. Log in to GitHub  
2. Click **New repository**  
3. Set:
   - Repository name: your exact GitHub username (e.g. `YangWang-Glasgow`)  
   - Public: enabled  
   - Initialize with README: enabled  
4. Click **Create repository**  

---

### Step 2: Clone the Repository

#### Option A: VS Code (GUI)

1. Open VS Code  
2. Press `Ctrl + Shift + P` (or `Cmd + Shift + P` on macOS)  
3. Select **Git: Clone**  
4. Paste:
   ```
   https://github.com/your-username/your-username.git
   ```
5. Choose a local folder and click **Open**  

#### Option B: Terminal

```bash
cd your-folder
git clone https://github.com/your-username/your-username.git
```

---

### Step 3: Edit `README.md`

1. Open `README.md` in VS Code  
2. Write content using Markdown  

Template resources:
- https://github.com/abhisheknaiidu/awesome-github-profile-readme  
- https://github.com/coderjojo/creative-profile-readme  

Markdown references:
- https://www.markdownguide.org/cheat-sheet  
- https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet  

Markdown preview in VS Code:
- `Ctrl + Shift + V`  
- `Ctrl + K` then `V`  

---

### Step 4: Commit and Push Changes

1. Open the **Source Control** panel  
2. Stage changes (`+`)  
3. Write a commit message (e.g. `update README.md`)  
4. Click **Commit**  
5. Click **Push** or **Sync**  
6. Check your GitHub profile page for updates  

---

## Submission Instructions

- Post your GitHub profile link on the Moodle forum  
- The repository must be public  
- Submissions are visible to all students  

---

# Exercises 2

## Setting Up a Python Environment in VS Code (Using Conda)

This exercise explains how to set up a Python environment in VS Code using Anaconda or Miniconda.

---

### Step 1: Install the Python Extension

1. Open VS Code  
2. Go to Extensions (`Ctrl + Shift + X`)  
3. Search for **Python** (Microsoft)  
4. Click **Install**  

---

### Step 2: Check Conda Installation

Open the VS Code terminal and run:

```bash
conda --version
```

If a version number appears, Conda is installed correctly.

---

### Step 3: Create a Conda Environment

```bash
conda create -n course-env python=3.13.1
conda activate course-env
```

You should see `(course-env)` in the terminal prompt.

Note that, if you cannot active course-env, try to switch to 'Command Prompt' by 
- press Ctrl + Shift + P
- Select the terminal profile, type:
```
Terminal: Select Default Profile
```
- From the list, select:
```
Command Prompt
```
- Open a new terminal by
Terminal → New Terminal or press Ctrl + `

You should now see a prompt like: C:\Users\... (not PS C:\...) 
- Activate Conda
```
conda activate course-env
```
You should see: (course-env) C:\Users\...


---



### Step 4: Select the Interpreter in VS Code

1. Press `Ctrl + Shift + P`  
2. Select **Python: Select Interpreter**  
3. Choose:
   ```
   conda | course-env | Python 3.13.1
   ```

---

### Step 5: Install Required Packages

```bash
conda install numpy pandas matplotlib
```

Always activate the environment before installing packages.

---

### Step 6: Test the Environment

Create `test.py`:

```python
import numpy as np
import pandas as pd

print(np.__version__)
print(pd.__version__)
```

Run:

```bash
python test.py
```

---

### Step 7: Use Jupyter Notebooks

```bash
conda install jupyter
```

Open a `.ipynb` file and select **course-env** as the kernel.
