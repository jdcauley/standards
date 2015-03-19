Cuberis use GIT for version control and GitHub for a number of development task. GitHub remote repositories, project development documentation, project issues and development specific discussion. The goal is to keep documentation and discussion in context and project a central location for all information related to development projects. Additionally, deployment of most projects is tied to the Master branch in GitHub in conjunction with DeployHQ.

### .gitignore Files

Using an appropriate .gitignore file is critical.

Cuberis' default .gitignore files are include in project baselines but may also be found on the  [Cuberis Gists Page](https://gist.github.com/cuberis).

### Branches

Cuberis has a specific branching structure for developing, staging and shipping code.

The primary primary branch for Development is the 'dev' branch. This branch should only ever have working code and should be the primary branch that work is merged into.

The 'dev' branch as sub branches labeled to indicate purpose.
- **bug/branch-name** : These branches are specifically for dealing with a collection of smaller bug, they may be ended with the day the work is being done or the type of work, ie. jan26, css-updates, js-errors.
- **issue/issue-number** : Branches prepended with issue/ are for specific larger scale issues reported in Github.
- **feature/feature-name** : These branches are used in primary production as well as for ongoing development of new features. There may be more than one of these branches to a feature as one may include backend or functional code while the other contains frontend.
- **styles/general** : This branch and associated branches are for the creation and implementation of general purpose CSS/JS that are not directly associate with specific components.

### Committing

When working with GIT it is important to commit regularly and to include concise and descriptive commit messages. The goal of commit messages is to provide information about what the commit involved.

https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message

1. First line should include less than 50 characters and act as a title.
2. Never use the <code> -m </code> flag (It encourages abbreviated messages)
3. Messages Should be in present tense (Fix bug vs Fixed Bug)
4. Answer the Following:
  * Why is the change necessary?
  * How does it address the issue?
  * What side effects does this change have?
  * If related to an issue provide a link to that issue

Example Commit Message
