# Git Cheat Sheet & Guide

A comprehensive reference for Git commands, workflows, and best practices.

## 🚀 Quick Reference

### Essential Daily Commands
```bash
git status                    # Check current status
git add .                     # Stage all changes
git add filename.txt          # Stage specific file
git commit -m "message"       # Commit with message
git push                      # Push to remote repository
git pull                      # Pull latest changes
```

## 📁 Repository Setup & Navigation

### Initial Setup
```bash
git init                      # Initialize new repository
git clone <url>               # Clone existing repository
git remote add origin <url>   # Add remote repository
git remote -v                 # View remote repositories
```

### Know Where You Are (Critical for Multiple Repos!)
```bash
pwd                          # Show current directory
git remote -v                # Show which repository you're connected to
git branch                   # Show current branch
git status                   # Show repository status
```

**💡 Pro Tip**: Always run `pwd && git remote -v` before making changes to avoid pushing to wrong repo!

## 📝 Making Changes

### Staging Changes
```bash
git status                   # See what's changed
git add filename.txt         # Stage specific file
git add .                    # Stage all changes
git add *.py                 # Stage all Python files
git reset filename.txt       # Unstage specific file
git reset                    # Unstage all files
```

### Committing Changes
```bash
git commit -m "Add new feature"              # Commit with message
git commit -m "Fix bug in data processing"  # Descriptive message
git commit --amend -m "Updated message"      # Change last commit message
```

### Good Commit Message Examples
```bash
git commit -m "Add entity resolution pipeline with LangGraph"
git commit -m "Fix CSV loading encoding issue"
git commit -m "Update README with installation instructions"
git commit -m "Remove sensitive data from .env file"
```

## 🌐 Working with Remote Repositories

### Pushing Changes
```bash
git push                     # Push to current branch
git push origin main         # Push to main branch
git push -u origin main      # Push and set upstream (first time)
git push --force             # Force push (use carefully!)
```

### Pulling Changes
```bash
git pull                     # Pull latest changes
git pull origin main         # Pull from specific branch
git fetch                    # Download changes without merging
```

## 🌿 Branching & Merging

### Creating & Switching Branches
```bash
git branch                   # List all branches
git branch feature-name      # Create new branch
git checkout feature-name    # Switch to branch
git checkout -b feature-name # Create and switch to new branch
git checkout main            # Switch back to main
```

### Merging Branches
```bash
git checkout main            # Switch to main branch
git merge feature-name       # Merge feature branch into main
git branch -d feature-name   # Delete merged branch
git branch -D feature-name   # Force delete branch
```

## 🔍 Viewing History & Changes

### Commit History
```bash
git log                      # View commit history
git log --oneline            # Compact view
git log --graph --oneline    # Visual graph
git show                     # Show last commit details
git show <commit-hash>       # Show specific commit
```

### Viewing Changes
```bash
git diff                     # Show unstaged changes
git diff --staged            # Show staged changes
git diff HEAD~1              # Compare with previous commit
```

## 🔧 Fixing Mistakes

### Undoing Changes
```bash
git checkout -- filename.txt    # Discard changes to file
git reset HEAD filename.txt     # Unstage file
git reset --soft HEAD~1         # Undo last commit (keep changes)
git reset --hard HEAD~1         # Undo last commit (lose changes)
git revert <commit-hash>        # Create new commit that undoes changes
```

### Dealing with Merge Conflicts
```bash
git status                      # See conflicted files
# Edit files to resolve conflicts
git add .                       # Stage resolved files
git commit                      # Complete the merge
```

## 🔒 Security & Sensitive Data

### .gitignore Best Practices
```bash
# Always ignore these in your .gitignore:
.env                    # Environment variables
*.key                   # API keys
__pycache__/           # Python cache
.DS_Store              # macOS files
node_modules/          # Node.js dependencies
*.csv                  # Large data files (if too big for GitHub)
```

### If You Accidentally Committed Sensitive Data
```bash
git rm --cached .env           # Remove from tracking
git commit -m "Remove .env from tracking"
git push
```

## 📊 Repository Management

### Checking Repository Health
```bash
git status                     # Overall status
git log --oneline -10          # Last 10 commits
git remote -v                  # Remote connections
git branch -a                  # All branches
```

### Cleaning Up
```bash
git clean -n                   # Preview what will be deleted
git clean -f                   # Delete untracked files
git gc                         # Garbage collect (optimize repo)
```

## 🏗️ Multi-Repository Workflow (Your Setup)

### Working with Multiple Repos
```bash
# Always check where you are first!
pwd && git remote -v

# For Coursework
cd /Users/arodriguez/Coursework
git status
git add .
git commit -m "Add week 5 assignments"
git push

# For Research
cd /Users/arodriguez/Research
git status
git add .
git commit -m "Update entity resolution pipeline"
git push
```

### Avoid Common Multi-Repo Mistakes
```bash
# ❌ BAD: Forgetting to check location
git add .
git commit -m "Add research"
git push  # Might go to wrong repo!

# ✅ GOOD: Always verify first
pwd && git remote -v  # Check location and repo
git status             # See what's changed
git add .
git commit -m "Add research findings"
git push
```

## 🚨 Emergency Situations

### "I'm lost and don't know what's happening"
```bash
pwd                           # Where am I?
git status                    # What's the repo status?
git remote -v                 # Which repository?
git log --oneline -5          # Recent commits
```

### "I made a mistake and need to undo"
```bash
git status                    # See current state
git stash                     # Save changes temporarily
git reset --hard HEAD         # Reset to last commit
git stash pop                 # Restore saved changes if needed
```

### "I have merge conflicts"
```bash
git status                    # See conflicted files
# Open files and look for <<<<<<< ======= >>>>>>> markers
# Edit to keep what you want
git add .                     # Mark conflicts as resolved
git commit                    # Complete the merge
```

## 🎯 Best Practices for Your Research Work

### Daily Workflow
1. **Start of day**: `cd /path/to/project && git pull`
2. **Before changes**: `git status` to see current state
3. **After changes**: `git add . && git commit -m "descriptive message"`
4. **End of session**: `git push`

### Commit Message Guidelines
```bash
# Good examples for your research:
git commit -m "Add multi-agent entity resolution system"
git commit -m "Fix Neo4j connection timeout issue"
git commit -m "Update README with dataset download instructions"
git commit -m "Add PowerPoint presentation to project"

# Bad examples:
git commit -m "stuff"
git commit -m "changes"
git commit -m "update"
```

### Before Computer Transfer
```bash
# Make sure everything is pushed
git status                    # Should show "working tree clean"
git push                      # Push any remaining changes
git log --oneline -5          # Verify recent commits are there
```

## 🔗 Useful Aliases (Optional)

Add these to your `~/.zshrc` for convenience:
```bash
alias gs='git status'
alias ga='git add .'
alias gc='git commit -m'
alias gp='git push'
alias gl='git log --oneline'
alias whereami='pwd && git remote -v'
```

## 📚 Common Scenarios for Your Work

### Adding a New Research Paper/Project
```bash
cd /Users/arodriguez/Research
mkdir new-project
cd new-project
# Add your files
git add .
git commit -m "Add new research project: [project name]"
git push
```

### Updating Existing Research
```bash
cd /Users/arodriguez/Research
# Edit your files
git add .
git commit -m "Update entity resolution with improved accuracy metrics"
git push
```

### Adding Coursework
```bash
cd /Users/arodriguez/Coursework
# Add homework files
git add .
git commit -m "Add CIS_5730 Assignment 2: Blockchain analysis"
git push
```

---

## 🆘 Quick Help Commands

```bash
git help                      # General help
git help <command>            # Help for specific command
git <command> --help          # Alternative help format
```

**Remember**: When in doubt, run `git status` - it tells you exactly what Git thinks is happening!

---

*Keep this file handy and reference it whenever you're unsure about Git commands. Practice makes perfect!*