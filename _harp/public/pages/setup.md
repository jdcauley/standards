Every new project or maintenance client at Cuberis gets a dedicated Github repository. This provides a project with a usable history and is part of our deployment process.

To create a new repository a Development Team Member will log into Github and with in the Cuberis account create a new repository.

![Add a New Repo](http://localhost:9000/assets/img/add-new-repo.jpg)

Once the new repo is created the developer can make their initial commit.

If creating a new project the initial commit should include baseline boilerplate files for the project which may include basic WP or Drupal files along with any other frameworks or plugins that are part of project baselines. This initial commit should take place before any additional CSS, JS or HTMl are added to the project.

If the repo is for a maintenance account or a new support client the initial commit should include all files as they were initially provided, before any updates or changes are made.

### .gitignore Files

Using an appropriate .gitignore file is critical.

Cuberis' default .gitignore files are include in project baselines but may also be found on the  [Cuberis Gists Page](https://gist.github.com/cuberis).

### Branches

Cuberis has a specific branching structure for developing, staging and shipping code.

#### Development

The primary primary branch for Development is the 'dev' branch. This branch should only ever have working code and should be the primary branch that work is merged into.

The dev branch as sub branches labeled to indicate purpose.
- **bug/branch-name** : These branches are specifically for dealing with a collection of smaller bug, they may be ended with the day the work is being done or the type of work, ie. jan26, css-updates, js-errors.
- **issue/issue-number** : Branches prepended with issue/ are for specific larger scale issues reported in Github.
- **feature/feature-name** : These branches are used in primary production as well as for ongoing development of new features.

### Deployments

Code that is ready for deployment to Production is pushed to the Master branch of the project. That branch is then deployed to the appropriate production server, presently via [DeployHQ](https://cuberis.deployhq.com/).
