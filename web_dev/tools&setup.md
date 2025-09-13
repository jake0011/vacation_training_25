---
title: Setup
nav_order: 2
has_children: false
parent: Web Development
layout: page
header-includes:
- \pagenumbering{gobble}
---

# Setup

### Why this matters
A small upfront investment in tooling and environment setup saves you hours of frustration later. The goal here is a reproducible environment that lets you focus on learning HTML/CSS, not fighting your tools.

### Accounts you should create (one-time)
- GitHub — for hosting code and collaborating.

### Recommended tools
- **Text editor:** Visual Studio Code (VS Code). Lightweight, extensible, and widely used in industry.
- **Browser(s):** Chrome/Edge or Firefox (both include excellent devtools).
- **Git:** Version control (we’ll cover Git in a dedicated page).
- **Optional but helpful:** Live Server extension (for instant preview of your web pages).

### complete installation checklist.
- [ ] Install VS Code
- [ ] Install Git (verify with `git --version`)
- [ ] Create a GitHub account.
- [ ] Install Live Server extension in VS Code

---

## Introduction to Git & GitHub

### what is Git?
 - When you write your code, it’s usually sitting on your computer. it’s fine until your laptop dies, or you want to show it to a friend, or maybe you need to collaborate with others. This is where **Git** and **GitHub** come in.  
 - Git is a distributed version control system. It lets you track changes, create branches, collaborate safely, and roll back mistakes. Think of it as a save-history + collaboration layer for your code.

### local vs remote
- Git first hosts your work locally before allowing you to push it to a remote location on the internet.
- **Local repo:** the `.git` folder in your project — history on your machine.
- **Remote:** GitHub/GitLab/Bitbucket — a hosted copy for sharing and collaboration.

### common git workflow (simple)
1. `git init` — create a repo (or `git clone <repo-url>` to get an existing one)
2. Edit files
3. `git add .` — stage changes
4. `git commit -m "short, descriptive message"` — snapshot
5. `git push origin main` — send changes to remote

### some other essential git commands
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

git init                       # create new repo
git clone <url>                # clone remote repo
git status                     # show changed files
git add <file|.>               # stage changes
git commit -m "message"        # save local snapshot
git branch                     # list branches
git branch feature-xyz         # create branch
git checkout feature-xyz       # switch branch
git merge feature-xyz          # merge branch into current
git pull origin main           # fetch + merge remote changes
git push origin branch-name    # publish branch
git remote -v                  # show remotes
```

Read more about git here: https://git-scm.com/doc

### what is GitHub?
GitHub is like the *social media for code*.  
- you have a profile (just like Facebook or LinkedIn).  
- you can upload your projects (called repositories, or “repos” for short).  
- others can see your code, give feedback, or even contribute.  

But it’s not just for showing off your work. gitHub is powered by **Git**(as discussed earlier.)

### why are we using GitHub in this training?
1. **Backups** — so that your code won’t vanish if your machine fails.  
2. **Sharing** — so I can check your projects, and you can see mine.  
3. **Proof of work** — employers and schools often look at GitHub to see what you’ve built.  
4. **Collaboration** — Later in your journey, you’ll work with others on the same project without “sending files over WhatsApp.”  

By the end of this training, you should have a GitHub profile that’s not empty, but filled with your projects — something you can proudly put on your CV.  

### some key terms you’ll hear me say
- **Repository (Repo):** A project folder on GitHub.  
- **Commit:** A “snapshot” of your project at a point in time.  
- **Push:** Sending your local code up to GitHub.  
- **Pull:** Getting the latest version of the code from GitHub to your computer.  

You don’t have to memorize these now, you’ll get the hang of them as we use them.  

### example  
Imagine you’re building a small website:  
1. You create the files on your laptop.  
2. You tell Git to “track” those files.  
3. You push them to GitHub.  
4. Now, from anywhere in the world, you (or I) can pull that project back.  

that's all for the setup and tools needed for this training.

### assignment  
1. Create a GitHub account if you don’t already have one.  
2. Explore your GitHub dashboard — click around to see repositories, issues, pull requests.  
3. Write a one-paragraph answer in your notes: *Why do you think employers value seeing a GitHub profile when hiring developers?*  

