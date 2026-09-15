# first-GitHub-action-workflow

# =========================================================================
# EXPLANATION OF GITHUB ACTIONS WORKFLOW
# =========================================================================

# 🏷️ THE NAME
# This is the title of my automation script. It will show up on the 
# "Actions" tab of your GitHub webpage so you can track its progress.
name: Muhammad Nasir

# ⚡ STEP 1: THE TRIGGER
# This tells GitHub exactly when to run this script. 
# It will ONLY run when code is pushed or merged directly into the 'main' branch.
# Pushing to other branches (like 'dev') will be ignored.
on:
  push:
    branches: [ main ]

# 💻 STEP 2: THE ENVIRONMENT
# A "job" is a collection of tasks. You named this job "demo".
# 'runs-on: ubuntu-latest' tells GitHub to turn on a temporary, clean, 
# and fast Linux virtual computer in the cloud to do the work.
jobs:
  demo:
    runs-on: ubuntu-latest

    # 🗣️ STEP 3: THE ACTION STEPS
    # This is the sequential to-do list for the Linux computer.
    steps:
      # This is the name of your first (and only) step.
      - name: Greeting
        
        # The 'run' keyword tells the Linux computer to type a command into its terminal.
        # 'echo' simply means "print this text on the screen".
        # When you check GitHub, you will see this exact message in the logs!
        run: echo "hello from github action lesson"
