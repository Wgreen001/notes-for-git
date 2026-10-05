`# Git & GitHub Learning Journal (SDEV143)

## Chapter 1: Introduction to Git

**Key takeaways**
- Git is a *distributed* version control system (VCS). Older *centralized* VCSs leave teams less organized and developers less productive.
- Most professional teams and open source projects use the same basic Git workflow. Using it solo still boosts productivity.
- No need to understand everything yet; focus on what Git can do for me.

**Questions to keep asking**
- How will Git help me in my projects?
- Which features are the most important?
- Will Git improve my workflow?

**My difficulties / notes:** The abstract part was hard to picture at first: distributed vs. centralized. The key idea is that every developer has a full copy of the project history, so work doesn't depend on one central server.

---

## Chapter 2: Installing and Setting Up Git

**Key takeaways**
- Installation is easy on Windows and even easier on Mac and Linux. If unsure, keep the default options.
- Setup is done once per system. Git signs every action with my name and email, so both must be configured before use.

```
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

**My difficulties / notes:** Easy to forget that name and email must be set before the first commit. Use `git config --list` to check them. Use the same email as my GitHub account so commits are linked to me.

---

## Chapter 3: The Three States of Files

**Key takeaways**
- **Modified:** changed in the Working Directory.
- **Staged:** added to the Staging Area so it can be snapshotted.
- **Committed:** snapshot of the project saved (unmodified + staged files).
- Files from the previous commit that I didn't touch carry into the next commit automatically.
- A modified but *unstaged* file won't be included until I stage it.
- Commit messages: Git opens an external editor, which feels awkward at first but gets easier.

**Commands to remember**
```
git add <file>
git commit -m "message"
git status
```

**My difficulties / notes:** The staging area is the confusing part: why add and then commit? Staging lets me choose exactly what goes into a snapshot. Also easy to forget `git add` and wonder why a change wasn't committed. The default editor (Vim) can trap me; `-m` avoids it.

---

## Chapter 4: Project History

**Key takeaways**
- `git log` lists all previous commits; `git show` displays details of a commit.
- `git diff` compares current modified files to the last commit.
- `.gitignore` keeps unwanted files out of `git status` and prevents accidentally committing secrets such as keys.

**Commands to remember**
```
git log
git show
git diff
```

**My difficulties / notes:** `git diff` shows nothing once a file is staged (use `git diff --staged`). `git log` can fill the screen; press `q` to exit. `.gitignore` doesn't affect files Git is already tracking.

---

## Chapter 5: Navigating, Undoing, and Amending

**Key takeaways**
- I can bring previous versions back into the working directory.
- I can undo and amend commits for small corrections.
- Re-read the first section of this chapter; the three states are essential and I should know them by heart.

**My difficulties / notes:** The risk is mixing up undo commands: some only unstage, some change history. Amending a commit rewrites it, so avoid that after pushing. Check `git status` before and after any undo.

---

## Beyond the Content

Things worth remembering that aren't in the chapters or assignments:
- Run `git status` often; it shows what state everything is in and often suggests the next command.
- Write small, clear commit messages, one change per commit.
- Never commit passwords or API keys; once pushed to GitHub they're hard to fully remove.
- Git (the tool on my computer) and GitHub (the website hosting repos) are different things.
- Pushing needs GitHub authentication (a personal access token or sign-in), which can fail the first time.
