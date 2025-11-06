<!---
{
  "id": "60b25ba1-4dd1-4ab9-a0b4-95408b08f6dc",
  "depends_on": [],
  "author": ["Tabea Röthemeyer","Stephan Bökelmann"],
  "first_used": "2025-04-02",
  "keywords": ["learning", "exercises", "github", "git"]
}
--->

# Git: Fork and Contribute on Github

## 1) Introduction
When developers want to share their projects, they use platforms designed specifically for collaboration — similar to social networks, but specialized for code. **GitHub** is one of the most prominent examples: it hosts and manages Git repositories, while also providing tools for version control, collaboration, and community building. GitHub adds layers of functionality on top of Git, such as issue tracking, wikis, project boards, and — most importantly — **pull requests**.

Pull requests are at the heart of collaborative development. They allow developers to propose changes, discuss them, request reviews, and eventually merge them into a mainline branch. A pull request ties two branches together: the source (with the proposed changes) and the target (where the changes should go). In this way, GitHub structures not only the flow of code, but also the communication around it.

But what happens when you don’t have write access to the original repository?

This is where **forks** come in. A fork is your **personal copy** of another user's repository — one that lives under your own account. You can modify it freely, create branches, commit changes, and push code just like any other Git repo. And once you're ready, you can open a **pull request** from your fork back to the original repository, proposing that your changes be included.

Forking is a core concept in open source workflows. It allows global collaboration without compromising repository integrity. The original repository remains protected, while contributors can still share improvements, bugfixes, or experiments.

Behind the scenes, a fork is simply a full Git clone — but hosted on GitHub and linked to the original repository. This "social fork" relationship enables features like pull requests across repositories, comparisons, and visibility into shared contributions.

In essence, GitHub turns Git's decentralized architecture into a global collaborative ecosystem — one where anyone can fork, contribute, and participate, even without explicit access rights.

### 1.1) Further Readings and Other Sources
- [Where do I start with Git and GitHub](https://docs.github.com/en/get-started/start-your-journey/about-github-and-git#where-do-i-start)
- [About Git and GitHub](https://docs.github.com/en/get-started/start-your-journey/about-github-and-git)
- [Reddit discussion: Why is GitHub so important](https://www.reddit.com/r/learnprogramming/comments/wg463w/why_is_github_so_important/)
- Talk: *The Future of Programming* by Bret Victor — philosophical context on collaboration and tooling.
- [GitHub Docs: About forks](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

## 2) Tasks

1. **Explore the STEMgraph Organization on GitHub**  
   Visit the public repositories of the STEMgraph organization:  
   👉 [https://github.com/STEMgraph/repositories](https://github.com/STEMgraph/repositories)  
   Browse the available projects and pick one that:
   - contains a small bug (e.g. a typo or logical mistake),
   - could benefit from an enhancement (e.g. clearer instructions or additional explanation), or
   - is missing something (e.g. a README section or link).

   **Tip**: Focus on repositories that contain Markdown exercises, as these are ideal for first contributions.

2. **Fork the Repository to Your GitHub Account**  
   - Open the chosen repository in your browser.
   - Click the **“Fork”** button in the upper-right corner.
   - GitHub will create a full copy of the repository under your username.

   ⚠️ This fork is now *your own remote* version of the project — you can push to it freely.

3. **Clone the Fork Locally**  
   On your computer, run the following (replace `<your-username>` and `<repo-name>` accordingly):
   ```bash
   git clone git@github.com:<your-username>/<repo-name>.git
   cd <repo-name>
   ```

4. **Create a New Branch for Your Changes**  
   It's best practice not to work directly on the `main` or `master` branch:
   ```bash
   git checkout -b improve-exercise
   ```

5. **Make Your Edits and Commit Them**  
   - Edit files as needed (e.g. fix typos, clarify instructions, improve formatting).
   - Stage and commit your changes:
     ```bash
     git add .
     git commit -m "Fix typos and improve clarity in exercise"
     ```

6. **Push the Branch to Your Fork**  
   ```bash
   git push origin improve-exercise
   ```

7. **Create a Pull Request (PR) to the Original Repository**  
   - Navigate to your fork on GitHub.
   - GitHub will usually show a banner offering to create a **Pull Request** — click the button `Compare & pull request`.
   - In the PR form:
     - Provide a clear title (e.g. "Improved instructions in README").
     - In the description, briefly explain what you changed and why.
     - Be polite and concise.

   Example:
   > Hello,  
   > I made a few improvements to the exercise text to fix grammar and make some instructions easier to follow. I hope this helps future readers!  
   > Best,  
   > *Your Name*

8. **Wait for Feedback or Merge**  
   Maintainers of the upstream project might:
   - Accept your PR and merge it directly,
   - Request changes or give feedback,
   - Or explain why they might not merge it.

   That’s normal — contributing is also about communication.



**Optional (Advanced)**: After your PR has been merged, you can [configure the upstream remote](https://docs.github.com/en/get-started/quickstart/fork-a-repo#syncing-your-fork) to keep your fork in sync:
```bash
git remote add upstream https://github.com/STEMgraph/<repo-name>.git
git fetch upstream
git merge upstream/main
```

## 3) Questions

1. **What is the difference between a GitHub fork and a local Git clone?**  
   Hint: Think about ownership, visibility, and where the copy lives.

2. **Why should you create a new branch before editing, even in your own fork?**  
   How does this help keep your work clean and modular?

3. **What happens when you push changes to your fork, but the original repository has changed in the meantime?**  
   How can you make sure your pull request will not cause merge conflicts?

4. **How can you update your fork to reflect changes from the upstream repository?**  
   Try to describe the purpose of `git remote add upstream` and `git fetch`.

5. **Why do open-source maintainers prefer contributions via pull requests rather than giving direct write access?**  
   Think in terms of trust, control, and quality assurance.

6. **What information should a good pull request contain?**  
   Consider both the technical and the social aspects (e.g., commit message, explanation, tone).


## 4) Advice

Contributing via forks and pull requests is the foundation of open source development. It allows for **distributed, asynchronous collaboration** without compromising the integrity of the original project. The workflow you practiced here is not just a technical necessity — it reflects values like transparency, discussion, and collective improvement.

Every contribution, no matter how small, is a chance to learn, communicate, and shape software that others depend on. Start small, be kind in your messages, and don’t be afraid to open that first pull request — it's how everyone begins.
