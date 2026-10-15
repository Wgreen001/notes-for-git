# Git & GitHub Learning Journal (SDEV143)

## Chapter 9: Quick Start with GitHub

**Key takeaways**
- GitHub is a cloud-based hosting platform built around Git. It stores remote repositories so developers can collaborate from anywhere.
- A remote repository is simply a Git repository stored online instead of on my local machine.
- Linking a local repository to GitHub uses a remote URL called `origin`.
- Once linked, I can push my commits to GitHub and pull updates from others.
- GitHub is not Git — Git is the version control tool, GitHub is the collaboration platform.

**Commands to remember**
git remote add origin <URL>
git remote -v
git push -u origin main
git pull
git clone <URL>


**My difficulties / notes:**  
Understanding remotes was confusing at first. The idea that my local repo and GitHub repo are separate but connected helped. Also, remembering that `origin` is just a nickname for the remote URL. The first push often requires authentication, which can fail if GitHub credentials aren’t set up correctly.

---

## Git & GitHub Relationship (Diagram Assignment)

**Key takeaways**
- Git handles **local version control**: working directory, staging area, commits, and project history.
- GitHub handles **remote collaboration**: sharing code, pull requests, issues, and backups.
- Git is distributed — every developer has a full copy of the project history.
- GitHub enables distributed workflows by hosting the shared version of the repository.
- Push = upload commits to GitHub.  
  Pull = download updates from GitHub.  
  Clone = copy a GitHub repo to my machine.

**Concepts to remember**
- Git = tool installed on my computer  
- GitHub = cloud platform that uses Git  
- Git works offline; GitHub requires internet  
- GitHub adds collaboration features Git alone doesn’t have

**My difficulties / notes:**  
The diagram helped me visualize how Git and GitHub communicate. The arrows (push, pull, clone) made the workflow clearer. The biggest challenge was remembering that GitHub doesn’t “run Git” — it *hosts* Git repositories. Git does the version control; GitHub provides the environment for teamwork.

---

## Beyond the Content (Module 3)

Things worth remembering that aren’t directly in the textbook:
- Remote repositories allow multiple developers to work together without overwriting each other’s changes.
- GitHub adds tools like pull requests, code reviews, issues, and project boards.
- Keeping a journal helps me track what confused me and how I solved it.
- Authentication issues are common — PATs (personal access tokens) are required for pushing.
- The Git workflow is becoming more familiar: modify → stage → commit → push.
