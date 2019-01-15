# Ultraschall
Ultraschall is an open source project which:
- Helps students to create & deploy a whole app from a-z. 
- At the same time the game learns kids the fundamentals of music theory. 

## Prerequisites
This part describes the installation on MacOS, please follow (and add here) tutorials for your Os. We will install a lot of tools in this section. This is probably the most tricky part but you once you have your toolset you can use it with a lot of applications. 

We will build an app with 
- [node.js](https://nodejs.org/en/)
- [mongoDB](https://www.mongodb.com/de)
- [Angular](https://angular.io/)
- [Phaser.io](http://phaser.io/)
- [Docker](https://www.docker.com/) ([docker-machine](https://docs.docker.com/machine/), [compose](https://docs.docker.com/compose/)) & [AWS EC2](https://aws.amazon.com/de/) for deployment
- [Webstorm](https://www.jetbrains.com/webstorm/) or another editor, in the rest of the tutorial I will use webstor, feel free to use any editor.

### node.js (backend)
Node.js is used for the backend. The backend handles more sensitive information like logins and handles the communication with the database. 

We use the node version manager `nvm` to install node.js. Follow this tutorial to 
[Install NVM](https://medium.com/@isaacjoe/best-way-to-install-and-use-nvm-on-mac-e3a3f6bc494d).
After you have installed nvm we install the current node version. At the time of the tutorial we use `11`:

```bash
nvm install 11
nvm use 11
```

#### Git
[Git](https://git-scm.com/) is a version control manager it makes it easier to collaborate, see what changed in the code and to specify milestones.
```bash
brew install git
``` 

##### Gitflow
We use a special workflow: [gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) which makes your development even more organized.
[Install Gitflow](https://github.com/nvie/gitflow/wiki/Mac-OS-X)
```bash
brew install git-flow
```

### MongoDB (database)
MongoDB is database, which helps us to save users, scores etc.
[Install MongoDB on MacOS](https://treehouse.github.io/installation-guides/mac/mongo-mac.html)
We can then run MongoDB with
```bash
mongod
```

### Angular (frontend)
The user is interacting with the frontend. 
First you need to have `Angular-CLI installed` use the command 
```bash
npm install -g @angular/cli
```

#### Phaser.io
[Phaser.io](http://phaser.io/) is framework for games, it makes it easier to do things like levels, player movement etc. We will come to this later.

## Step 1 Creating the app
For every step of the tutorial there is a release on github. So you can basically step in at each step of the tutorial.

### Steps to V1
This are the steps before the first commit was done. You **DON'T** have to do this steps since you will clone this structure:
Creating the application folder and a git repo.
```bash
mkdir ultraschall
webstorm .  
# next step not required if webstorm console is used
cd ultraschall 
```

Create a file name `.gitignore` and add the following
```
.idea
node_modules
.tmp
*.DS_Store
```
Then go back into the console and make the first commit:
```bash
git add --all
git commit -m "INIT"
```