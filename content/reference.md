# Quick reference

## Other cheatsheets

* [Detailed 2-page Git
  cheatsheet](https://aaltoscicomp.github.io/cheatsheets/git-the-way-you-need-it-cheatsheet.pdf)
* [Interactive Git cheatsheet](http://www.ndpsoftware.com/git-cheatsheet.html)
* [Very detailed 2-page git
  cheatsheet](https://aaltoscicomp.github.io/cheatsheets/git-the-way-you-need-it-cheatsheet.pdf)


## Glossary

:::::{glossary}

alias
   With aliases you can define your own shortcuts for Git commands.

bare repository
   A copy of a repository that only is only the `.git`
   directory: there are no files actually checked out.  Directory names
   usually like `something.git`

branch
   One line of work.  Different branches can exist at the same time
   and split/merge.  Committing on a branch updates that branch.

clone
   As a verb, the process of making a copy of a repository locally.
   It brings in all history and all files.  (As a noun, the copy that
   was made when cloning).

commit
   As a verb, the process of recording more changes.
   As a noun, the name of the record of changes.
   A commit is identified by something such as `554c187`.

conflict
   When a merge has changes that affect the same lines,
   git can not automatically figure out what to do.  It presents the
   conflict to the user to resolve.

fetch
   Update your view of another repository

fork
   As a noun: a one person's copy of a repository.
   As a verb: making that copy.
   As a verb on GitHub: Making a copy of a repository linked to the
   original.  It is easy to send changes to the original

git
   Implementation of a version control system. Currently the most popular one.

git hook
   Code that can run before or after certain actions, for
   example to do tests before allowing you to commit.

GitHub repository
   The files from the Git repository, but also other things from
   GitHub such as access permissions, issues, and pull requests.

hash
   Unique reference of any commit or state.  Comes from [hash
   functions](https://en.wikipedia.org/wiki/Hash_function) such as MD5
   or SHA1.

HEAD
   Pointer to the most recent commit on the current branch.

issue
   Within a web repository like GitHub, discussion of a topic, for
   example a problem or improvement suggestion.  These are a property
   of the web platform and not of the Git program itself.

main
   Default name for main branch on GitLab and GitHub.
   In this lesson we configure Git so that the default branch is
   called **main** to be more consistent with GitHub and GitLab.

master
   Default name for main branch on Git. Depending on the configuration and service,
   the default branch is sometimes **main**.
   In this lesson we configure Git so that the default branch is
   called **main** to be more consistent with GitHub and GitLab.

merge
merging
   Bringing changes from one branch into another, either as a noun or
   verb.

origin
   Default name for a remote repository.

origin/NAME
   A branch name which represents a remote branch.

pull
   Getting changes from another copy to your own copy.  `git pull`
   does this fetch, and also tries to automatically merge.

pull request
   A GitHub concept: change proposal.  A proposal to merge one branch
   into another.  Usually used to contribute code back to
   {term}`upstream`.  In Gitlab, called "**merge request**".

push
   Send a branch from your current repository to a remote repository

remote
   Roughly, another git repository on another computer.  A
   repository can be linked to several other remotes.

repository
   One collection of files managed by Git.  It contains entire history
   of all files managed by git.  GitHub has one repository as one
   GitHub repository.  VS Code has one repository as one directory you
   can open.  The command line has one repository as one directory.

staging area
   Place files go after `git add` and before `git commit`

tag
   Like a {term}`branch` in that it points to a commit for reference.
   It is designed to be permanent an not updated.

upstream
   The original repository from which the code comes.  If you
   {term}`fork` the repository, it is your upstream and it is easy to
   send changes back to there.

version control system
   A system that records changes to a file or set of files over time so that
   you can recall specific versions later.

VS Code
   A text editor and development environment by Microsoft.  It's quite
   popular, partly because it is powerful and easy to use.  [VS
   Codium](https://vscodium.com/) is the same but without Microsoft
   tracking.

working directory
workspace
   the actual files you see and edit
:::::

## Commands we use

Setup:

* `git config`: edit configuration options
* `git init -b main`: create new repository with `main` as the default branch
* `git clone URL [TARGET-DIRECTORY]`: Make a copy of existing
  repository at &lt;url&gt;, containing all history.

See our status:

* `git status`: see status of files - use often!
* `git log`: see history of commits and their messages, newest first
* `git graph`: see a detailed graph of commits.  Create this command
  with `git config --global alias.graph "log --all --graph --decorate --oneline"`
* `git diff`: show difference between working directory and last commit
* `git diff --staged`: show difference between staging area and last commit
* `git show COMMIT`: inspect individual commits
* `git remote [-v]`: List all remotes

General work:

* `git add FILE`:
  - Add a new file
  - Add a file to staging
* `git commit`: record a version, add it to current branch
* `git commit --amend`: amend our last commit
* `git branch`: show which branch we're on
* `git branch NAME`: create a new branch called "name"
* `git restore FILE`: restore last committed/staged version of FILE, losing unstaged changes
* `git switch --create BRANCH-NAME`: create a new branch and switch to it
* `git switch BRANCH-NAME`: Make a branch active.
* `git revert HASH`: create a new commit which reverts commit HASH
* `git reset --soft HASH`: remove all commits after HASH, but keep their modifications as staged changes
* `git reset --hard HASH`: remove all commits after HASH, permanently throwing away their changes
* `git merge [BRANCH-NAME]`: Updates your current branch with
  changes from another branch.  By default, merges to the branch is is
  tracking by default.
* `git grep PATTERN`: search for patterns in tracked files
* `git annotate FILE`: find out when a specific line got introduced and by whom
* `git bisect`: find a commit which broke some functionality
* `git push [REMOTE-NAME] [BRANCH:BRANCH]`: Send commits and
  update the branch on the remote.
* `git pull [REMOTE-NAME] [BRANCH-NAME]`: Fetch and then merge
  automatically.  Can be convenient, but to be careful you can fetch
  and merge separately.
* `git fetch [REMOTE-NAME]`: Get commits from the remote.  Doesn't
  update local branches, but updates the remote tracking branches
  (like origin/NAME).
* `git remote add REMOTE-NAME URL`: Adds a new remote with a
  certain name.
