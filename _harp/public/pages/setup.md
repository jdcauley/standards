
### Getting Started

Cuberis generally uses 2 environments for development of projects. Harp.js for Static sites and templates and Vagrant for PHP environments.

We use the [Varying Vagrant](https://github.com/Varying-Vagrant-Vagrants/VVV) to build PHP projects as a shareable, stable and self containted environment. The documentation on the [Varying Vagrant](https://github.com/Varying-Vagrant-Vagrants/VVV) provides an excellent primer on both [Vagrant](https://www.vagrantup.com/) as well as building projects with in the environment.

We typically use [Harp.js](http://harpjs.com/) when working on static sites or crafting initial templates for its speed and easy of use. Projects are self contained and easy to share within the team via GitHub.

While these tools are prefered Cuberis works to continually evaluate the best tool for internal projects as well as project needs.

Any new or maintenance project gets a GitHub repo for code storage and management. If the client has both a production and maintenance server DeployHQ is set to use the Staging branch for the development server and the master branch for production. This provides a project with a consolidated and readable history and is part of our deployment process.

To create a new repository a Development Team Member will log into Github and with in the Cuberis account create a new repository.

![Add a New Repo](http://cuberis.github.io/standards/assets/img/add-new-repo.jpg)

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

The 'dev' branch as sub branches labeled to indicate purpose.
- **bug/branch-name** : These branches are specifically for dealing with a collection of smaller bug, they may be ended with the day the work is being done or the type of work, ie. jan26, css-updates, js-errors.
- **issue/issue-number** : Branches prepended with issue/ are for specific larger scale issues reported in Github.
- **feature/feature-name** : These branches are used in primary production as well as for ongoing development of new features. There may be more than one of these branches to a feature as one may include backend or functional code while the other contains frontend.
- **styles/general** : This branch and associated branches are for the creation and implementation of general purpose CSS/JS that are not directly associate with specific components.

#### Staging

The 'staging' branch does not have sub branches. This branch primary serves as a testing, and staging branch before anything is pushed to production. Code may sit in this branch until reaching an appropriate deployment branch when it is merged to master.

#### Production

The 'master' branch does not have sub branches. This branch should never be edited and is should be a direct representation/duplication of the code that is in production for any given project. As our deployments are triggered by any push to this branch it is critical that code be properly tested before being merged into master. Merges should only take place as a pull request from staging.

### Deployments

Code that is ready for deployment to Production is pushed to the Master branch of the project. That branch is then deployed to the appropriate production server, presently via [DeployHQ](https://cuberis.deployhq.com/).

#### Setting up a Project in DeployHQ

After logging in at https://cuberis.deployhq.com, in the right sidebar is a Create New Project Widget.

![New DeployHQ Project](http://cuberis.github.io/standards/assets/img/create-new-project-deployhq.png)

This will take you to the following screen where you will name the project accordingly.

![Name Your Project](http://cuberis.github.io/standards/assets/img/name-your-project-deployhq.png)

Under Repository Details, you can authenticate to Github and select the appropriate project

![Repo Details](http://cuberis.github.io/standards/assets/img/repo-details-deployhq.png)
