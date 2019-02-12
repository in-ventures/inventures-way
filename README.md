# **Inventures Software Development Way**

**This is a live document - no dogma, no final truth - it's up tu us to keep it relevant**

**Objective**

To spend less time finding bugs, solving merge conflicts, re-inventing the whell so we can spend more time developing great experiences for our clients (and doing whatever else we want) 

------------------------
Here we define rules and alignments to collaborate and ensure we give our users high quality user experiences.

This guideline is structured around 2 sections: set-up and ongoing, each divided in several chapters as follows:

* Setup
	* Setting-up your machine
	* Services accounts
	* Visual Studio Code configuration
	* Git configuration

* Ongoing
	* Team management tools: Trello & Slack
	* Dos and don'ts when developing
	* Git flow practices


------------------------

## Setup

### Setting-up your machine

At Inventures we use the software most recent versions **with long term support**. Align with the team on the specific tools and versions to be used, but most likely you will need to have:

* git
* node (do not use odd versions)
* npm
* yarn
* nvm
* mongoDB
* postgreSQL
* angular/cli
* Visual Studio Code
* Robo 3T

### Services accounts

You have to sign up with your inventures email to all the services that you will use. **You must "log in with Google"** to keep our clients information safe. The services might change over time and could be project specific, yet very likely you will need to sign up to

* Bitbucket
* NPM
* Github
* Trello
* Slack
* AWS
* Google Cloud
* Azure


### Git configuration and safety considerations

Simply, make sure before you do anything in a new project, that you create your branch (details regarding branch usage covered in subsequent section) a .gitignore file, making sure you at least add: 

* .env - To avoid the risk of committing credentials
* .node_modules - Then repo will be massive and that will remain in the history
* /dist - Distribution files

**Do not** hardcode any credential or password in a file that you are not including into the .gitignore file. Otherwise we will be left exposed by having that info committed in our branches history

See a .gitignore file example inside the example folder

### Visual Studio Code Configuration

//TODO

------------------------


## Ongoing

### Team management tools: Trello & Slack

// TODO

### Dos and don'ts when developing

**Dos**
* DRY: do not repeat yourself, i.e. factor your code in reusable modules
* TYPINGS: use typings as much as posible so to prevent type injection erros
* Use Merge Squash for pull request to make it easier to find different pull requests

**☠️ don'ts 🚨**
* Use <any> in TypeScript - if there is no work-around be ready to have a good explanation
* Send a pull request without ensuring you have the most up to date versión of the development branch
* Use production environment variables in you local environment


### Git flow practices

We follow Atlasian git flow practices ([here you can read more details](https://confluence.atlassian.com/bitbucketserver/using-branches-in-bitbucket-server-776639968.html)) 

#### Branch structure:
* **Permament Branches:**
	* **master**: Contains the production version of the code.
	* **staging**: Contains the stagging version of the code. This might differ from *dev* since the we might want to lock a stagging stage whilst keep working on additiona features. This branch deploys to *stagging* 
	* **dev**: Development branch. Contains the most up to date version of the code. All approved features merge into this branch
* **Temporary branches**
	* **feature/{developer_name}/{feature_name}**: Temprorary branch created by each developer to work on a specific new feature. It branches from, and merges back into, the dev branch using pull requests. Please use descriptive names for the feature and avoid adding commits not related to the named feature.
	* **bugfix/{developer_name}/{bug_name}**: Used to fix a release branch without interrupting changes in the development branch, thus it branches out from the *master*. Changes should be merged into the *master* **and** *dev* branches.
	* **hotfix/{developer_name}/{hot_bug_name}**: Used to quickly fix a Production branch without interrupting changes in the development branch, thus it branches from *master*. Changes should be merged into the *master* **and** *dev* branches.
