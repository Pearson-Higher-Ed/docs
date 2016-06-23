# Contributing to Origami v2 repositories, ElementsSDK, or CompoundsSDK

While each repository has its own README file you should read, some things are the same regardless of which project you are contributing to.

Please adhere to the following guidelines:

- [Issues](#issues)
- [Git Workflow](#git-workflow)
- [Git Commit Message Format](#commit-message-format)


## <a name="issues"></a> Issues

If you find a bug or have a feature request, please open an issue on the Github repository page itself, or consider creating a PR (pull request; follow the steps below).

## <a name="git-workflow"></a> Following the Git Workflow for Pull Requests

In general, we use PRs (pull requests) to add new code to a repository.

Read the [document on NEO](https://neo.pearson.com/docs/DOC-279914) first, but in short: 

* do all your changes in a feature branch 
* use the Commitizen Message format (more below) in your Git commit messages
* use  `rebase` instead of `merge` to stay up-to-date with master (be aware that for the [elements](https://github.com/Pearson-Higher-Ed/elements/) and [compounds](https://github.com/Pearson-Higher-Ed/compounds/) repos, the master branch is called "v0")
* squash your commits. Squashing your commits makes it easier for the Pearson Design group to review your changes.

## <a name="commit-message-format"></a> Git Commit Message Format

We let our release changelogs get automatically written based on our Git commit messages by using the [conventional-changelog](https://github.com/ajoslin/conventional-changelog) format to ensure consistency. You are encouraged to use the [commitizen CLI](https://github.com/commitizen/cz-cli) when committing new code, but if you prefer to write your commit messages manually, follow the Commitizen format:

```
git commit -m "<keyword>: <message>"
```

The keywords are one of the following:

**feat**: A new feature

**fix**: A bug fix

**docs**: Documentation-only changes

**style**: Changes that don't affect the code (whitespace/indenting changes, missing semi-colons etc)

**refactor**: A code change that neither fixes a bug nor adds a feature

**perf**: A code change that improves performance

**test**: Adding missing tests

**chore**: Changes to the build process or auxiliary tools and libraries such as documentation generation


Using the keyword followed by a colon will ensure uptake in the changelogs.

Example:

```
git commit -m "docs: removed various spelling mistakes"
```

When you have finished coding and have pushed up your branch, submit your PR targeting the **master** branch.
