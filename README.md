# Git Commands Repository 🚀

[![GitHub](https://img.shields.io/badge/GitHub-Commands-blue)](https://github.com/abhijitray7810)
[![Git](https://img.shields.io/badge/Git-Reference-orange)](https://git-scm.com/)

A comprehensive collection of Git commands, problem statements, and solutions for daily practice and professional reference.

## 📋 Table of Contents

- [About](#about)
- [Repository Structure](#repository-structure)
- [Daily Topics](#daily-topics)
- [Getting Started](#getting-started)
- [How to Use](#how-to-use)
- [Contributing](#contributing)
- [Author](#author)

## 🎯 About

This repository serves as a **complete reference guide** for Git version control system. It contains:

- ✅ Essential Git commands with detailed explanations
- ✅ Real-world problem statements and scenarios
- ✅ Step-by-step solutions and best practices
- ✅ Daily learning modules for systematic Git mastery

Perfect for beginners learning Git and professionals looking for quick command references.

## 📁 Repository Structure

```
git-commands-repo/
├── Day-01/          # Set Up Git Repository on Storage Server
├── Day-02/          # Git Cherry Pick
├── Day-03/          # Clone Git Repository on Storage Server
├── Day-04/          # Fork a Git Repository
├── Day-05/          # Delete Git Branch
├── Day-06/          # Staging a File for Commit
├── Day-07/          # Creating and Initializing a Git Repository
├── Day-08/          # Cloning a Bare Repository
├── Day-09/          # Checking out Master Branch
├── Day-10/          # Branching, Merging and Pushing
├── Day-32/          # Git Rebase
├── Day-33/          # Resolve Git Merge Conflicts
└── README.md
```

Each day folder contains:
- `Command.md` or `Commands.md` - Detailed command reference
- `Questions.md` - Problem statements and scenarios (where applicable)

## 📚 Daily Topics

### Foundation (Days 1-10)

| Day | Topic | Description |
|-----|-------|-------------|
| 01 | Repository Setup | Initialize Git repository on storage server |
| 02 | Cherry Pick | Selectively apply commits from one branch to another |
| 03 | Clone Repository | Clone existing repositories from remote servers |
| 04 | Fork Repository | Create personal copies of repositories |
| 05 | Delete Branch | Remove local and remote branches safely |
| 06 | Staging Files | Add files to staging area for commit |
| 07 | Git Initialization | Create and set up new Git repositories |
| 08 | Bare Repository | Clone and work with bare repositories |
| 09 | Branch Checkout | Switch between branches and manage branch states |
| 10 | Branch Operations | Create, merge, and push branches |
 
### Advanced Topics (Days 30+)

| Day | Topic | Description |
|-----|-------|-------------|
| 32 | Git Rebase | Rewrite commit history and maintain clean logs |
| 33 | Merge Conflicts | Resolve conflicts during branch merging |

## 🚀 Getting Started

### Prerequisites

- Git installed on your system ([Download Git](https://git-scm.com/downloads))
- Basic command line knowledge
- A GitHub account (for remote operations)

### Installation

1. **Clone this repository:**
   ```bash
   git clone https://github.com/abhijitray7810/git-commands-repo.git
   ```

2. **Navigate to the repository:**
   ```bash
   cd git-commands-repo
   ```

3. **Explore daily topics:**
   ```bash
   cd Day-01
   cat Command.md
   ```

## 💡 How to Use

### For Beginners
1. Start with **Day-01** and progress sequentially
2. Read the problem statements in each day's folder
3. Practice commands in a test repository
4. Review solutions and best practices

### For Quick Reference
1. Use the [Daily Topics](#daily-topics) table to find specific commands
2. Navigate directly to the relevant day folder
3. Copy and adapt commands for your use case

### For Practice
1. Read the problem statement
2. Attempt to solve using Git commands
3. Compare with provided solutions
4. Experiment with variations

## 📖 Example Usage

### Day 02: Cherry Pick Example
```bash
# View commits
git log --oneline

# Cherry pick a specific commit
git cherry-pick <commit-hash>

# Resolve conflicts if any
git add .
git cherry-pick --continue
```

### Day 05: Delete Branch Example
```bash
# Delete local branch
git branch -d branch-name

# Force delete local branch
git branch -D branch-name

# Delete remote branch
git push origin --delete branch-name
```

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a new branch:**
   ```bash
   git checkout -b feature/new-command
   ```
3. **Add your changes**
4. **Commit with descriptive message:**
   ```bash
   git commit -m "Add: Day-XX with new Git command"
   ```
5. **Push to your fork:**
   ```bash
   git push origin feature/new-command
   ```
6. **Create a Pull Request**

### Contribution Guidelines
- Follow existing folder structure
- Include clear command explanations
- Add practical problem statements
- Test all commands before submitting
- Use proper markdown formatting

## 📝 Future Topics

Planned additions:
- Git Stash operations
- Git Tags and Releases
- Git Submodules
- Git Hooks
- Advanced Git workflows
- Git troubleshooting guide

## 🔗 Useful Resources

- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)

## 👤 Author

**Abhijit Ray**
- GitHub: [@abhijitray7810](https://github.com/abhijitray7810)

## 📄 License

This project is open source and available for educational purposes.

## ⭐ Show Your Support

If you find this repository helpful:
- Give it a ⭐ star
- Fork it for your own reference
- Share it with others learning Git

---

**Last Updated:** November 2024

**Status:** 🟢 Actively Maintained

*Happy Git Learning! 🎉*
