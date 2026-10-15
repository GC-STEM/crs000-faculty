# CS-000 | 1-1 Setup Tasks

In this activity, you will set up your **course development environment** (CDE). Complete these one-time setup tasks **before the end of Week 1** or before starting **Repository Activities**.

## Table of Contents <!-- omit from toc -->

1. [Set up your GitHub account](#set-up-your-github-account)
2. [Set up your development tools](#set-up-your-development-tools)
3. [Set up your course repository](#set-up-your-course-repository)
4. [Temporary Holding Area](#temporary-holding-area)

## Set up your GitHub account

A personal GitHub account is **{{optional | recommended | required}}** for this course. You will use your GitHub account to store and manage your course repositories throughout your degree program and showcase selected projects to prospective employers.

To set up your GitHub account, select the option that best describes your situation:

- [**I don't have a GitHub account or don't want to use an existing one**](https://github.com/GC-STEM/.github/wiki/GitHub-Setup#create-a-new-github-account).

- [**I already have a GitHub account I want to use, but haven't set it for up for SNHU coursework yet**](https://github.com/GC-STEM/.github/wiki/GitHub-Setup#configure-your-github-account).

- [**I have already set up my GitHub account for SNHU coursework**](https://github.com/GC-STEM/.github/wiki/GitHub-Setup#verify-your-github-account).

## Set up your development tools

### Remote development environment

Use [{{remote development environment}}](./platforms/rde.md), the **{{recommended | required}} development environment** for this course. It serves as the reference environment for course instructions and examples.

Development tools are pre-installed. You just need to configure some personal settings.

### Local development environment

Install and configure the development tools on your own computer. You must have a publisher-supported version of your operating system and access to an administrator account to approve installations when required. You do not need to use an administrator account for your coursework.

- [**Windows**](./platforms/windows.md)
- [**macOS**](./platforms/macos.md)
- [**Linux**](./platforms/linux.md)

### Cloud development environment

Use browser-based development tools with no installation. These options are useful if you **join the course late, need to get started quickly, or cannot install software** on your device (such as a work or library computer, Chromebook, or tablet).

These tools are generally better for **temporary or occasional use** than regular coursework. For long-term use, choose your course's recommended development environment unless instructed otherwise.

- [**GitHub Codespaces**](./platforms/codespaces.md) — A full cloud development environment for writing, running, testing, and debugging code, including terminal access. **Monthly usage limits apply.**

- [**VS Code for Web**](./platforms/vscode.dev.md) — A free browser-based code editor for editing files and saving changes to GitHub. **Cannot run or debug code or execute terminal commands.** No usage limits.

## Set up your course repository

A [**GitHub repository**](https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories) stores your course files and tracks changes to them. In this phase of the setup tasks, you will create two connected copies: one in your course development environment (CDE) and one in your personal GitHub account.

Run the following commands in a Bash terminal (**Git Bash** on Windows).

### Create your local copy

[Cloning a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) copies its files and history to your computer or virtual desktop. Your local copy will remain connected to the official course repository through a [remote](https://docs.github.com/en/get-started/git-basics/managing-remote-repositories) named `upstream`, allowing you to receive course updates.

<!-- ci:command-test id=clone-course-repo fixture=empty-repos expect=repo -->
```bash
mkdir -p "$HOME/Repos"
git clone --origin upstream https://github.com/GC-STEM/cs000.git "$HOME/Repos/cs000"
cd "$HOME/Repos/cs000"
git remote -v
```

### Create your GitHub copy

Use the [GitHub CLI](https://docs.github.com/en/github-cli/github-cli/about-github-cli) to create a **private repository** in your personal GitHub account and upload your local copy. This repository belongs to you and will store your coursework indefinitely.

**Git** connects your local copy to your personal repository on GitHub through a remote named `origin`. You will use `origin` to save your work to GitHub and `upstream` to receive official course updates.

<!-- ci:command-test id=create-personal-repo fixture=existing-repo expect=repo -->
```bash
cd "$HOME/Repos/cs000"
gh api --method PUT user/starred/GC-STEM/cs000
gh repo create cs000 --private --source=. --remote=origin --push
git remote -v
```

### Connect with GC-STEM

GitHub is also a social network where you can share ideas, explore projects, and learn from others. [GC-STEM](https://github.com/GC-STEM) is SNHU's official GitHub organization for its [online STEM degree programs](https://www.snhu.edu/online-degrees/stem), offering opportunities to connect with faculty and fellow students.

Run the following commands to [**follow GC-STEM**](https://docs.github.com/en/get-started/exploring-projects-on-github/following-organizations). You'll see its public activity, including new repositories and discussions, on your GitHub dashboard.

<!-- ci:command-test id=connect-with-gc-stem fixture=existing-repo expect=repo -->
```bash
cd "$HOME/Repos/cs000"
gh api graphql -f query='mutation($id:ID!){followOrganization(input:{organizationId:$id}){id}}' -f id="$(gh api orgs/GC-STEM --jq .node_id)"
```

---

## Temporary Holding Area

<!-- ci:command-test id={{unique-descriptive-test-name}} fixture={{empty-repos|existing-repo}} expect={{repo|part-a}} -->
```bash
code "$HOME/Repos/cs000"
```

> [!IMPORTANT]
> Now that you have completed setting up your platform, perform all remaining activities in your course development environment (CDE), not on GitHub.
