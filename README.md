#**Inventures Software Development Way**

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

// TODO


### Git flow practices

// TODO
