Cuberis used GitHub for GIT based version control, project specific documentation, and issues/bug management. This provides the advantage of consolidating the history, documentation and project code in a single location. These repositories can be shared with clients provided they have or create a GitHub account.

Cuberis maintains an account at [Code School](https://codeschoole.com) for team member use. There are several course on understanding and using GIT.

### .gitignore Files

Using an appropriate .gitignore file is critical.

The .gitignore file is critical, particularly in a GIT based deployment solution as it will prevent GIT or DeployHQ from overwriting environment specific files.

### Branches

Cuberis has a specific branching structure for developing, staging and shipping code.

#### Development

The primary primary branch for Development is the 'dev' branch. This branch should only ever have working code and should be the primary branch that work is merged into.

The 'dev' branch as sub branches labeled to indicate purpose.
- **bug/branch-name** : These branches are specifically for dealing with a collection of smaller bug, they may be ended with the day the work is being done or the type of work, ie. jan26, css-updates, js-errors.
- **issue/issue-number** : Branches prepended with issue/ are for specific larger scale issues reported in Github.
- **feature/feature-name** : These branches are used in primary production as well as for ongoing development of new features. There may be more than one of these branches to a feature as one may include backend or functional code while the other contains frontend.
- **styles/general** : This branch and associated branches are for the creation and implementation of general purpose CSS/JS that are not directly associate with specific components.
