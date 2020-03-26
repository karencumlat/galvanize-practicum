# Basic GitHub

[Atlassian BitBucket](https://www.atlassian.com/git/tutorials)

[Learn Git Branching](https://learngitbranching.js.org/)

## Committing

**git add** command to stage changes for the next commit

**git commit** command to save changes to the repository

```git
git add [file]
git commit -m "Descriptive message"
```

**-m** sets the descriptive message of the commit

```git
git commit -a -m "Build and style homepage"
```

**-a** includes all currently changed files in commit

## Synching

**git fetch** command to fetch commits from a remote repository into local repo (local repo stays the same)

```git
git fetch origin
```

**git push** command to upload local repository content to a remote repo

```git
git push remote-branch-name local-branch-name
```

**git pull** command to fetch and download content from a remote repository and immediately update the local repo to match the content.

```git
git pull origin master
```

## Branching

```git
git branch branch-name
git checkout branch-name
```

or create a new branch and check it out at the same time

```git
git checkout -b branch-name
```

## Merging

let us merge **master** into branch-name

```git
git checkout branch-name
git merge master
```

## How to Write Good Commit Message

[A Note About Git Commit Messages](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) by Tim Pope

[How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/) by Chris Beams

[How to Write Good Commit Messages: A Practical Git Guide](https://www.freecodecamp.org/news/writing-good-commit-messages-a-practical-guide/) by Bolaji Ayodeji

### Here’s a model Git commit message

```git
Capitalized, short (50 chars or less) summary

More detailed explanatory text, if necessary.  Wrap it to about 72 characters or so.  In some contexts, the first line is treated as the subject of an email and the rest of the text as the body.  The blank line separating the summary from the body is critical (unless you omit the body entirely); tools like rebase can get confused if you run the two together.
```

### Subject Line

* Separate subject from body with a blank line
* Limit the subject line to 50 characters
* Capitalize the subject line and each paragraph
* Remove unnecessary punctuation marks
* Do not end the subject line with a period
* Use the imperative mood in the subject line
  * "Fix bug" and not "Fixed bug" or "Fixes bug."

### Body

* Wrap the body at 72 characters
* Use the body to explain what and why vs. how
* Do not assume the reviewer understands what the original problem was, ensure you add it.
* Do not think your code is self-explanatory
* Follow the commit convention defined by your team

* Further paragraphs come after blank lines.
* Bullet points are okay, too. Use hyphen or asterisk followed by a single space, with blank lines in between, but conventions vary here
* Use a hanging indent

### Specify the type of commit

* feat: The new feature you're adding to a particular application
* fix: A bug fix
* style: Feature and updates related to styling
* refactor: Refactoring a specific section of the codebase
* test: Everything related to testing
* docs: Everything related to documentation
* chore: Regular code maintenance.[ You can also use emojis to represent commit types]
