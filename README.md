# es6-tooling-no-babel-intro
- Create a new directory (If doing this for the first time)
- npm init --yes
- This creates a package.json file for us

Next we will install our needed dependencies through the terminal
npm i babel-cli@6.26.0 babel-core@6.26.0 babel-preset-env@1.6.1 --save-dev
![npm-init-package-json-step-1](https://user-images.githubusercontent.com/5911897/213965840-207ab991-a1d9-42d8-a442-353e007fc37d.PNG)
___

## Adding dependencies explanation
The first package is the Command Line Interface for Babel
We give it our js file and it will compile it for us
The second is the logic or transpiling code is all implemented
The last one is for targetting specific features which are basicaly plugins
- Like consts let and const or the use of arrow functions
- Presets allow us all of the goodness
The last command  means we are installing these dependencies into our development environment
___

## Package JSON Folder and Locked file, gitignore file explanation
Looking at our folder structure once this all has installed we have the following:
- package-lock.json (is used by NPM)
- node_modules folder holds all the installed dependencies for all of the packages
___

## Add a new file that will be modified by the babel build
Next we can add a new file to our folder called index.js
In the modified `package.json` for the newly added script for running babel 
- We need to create a new build folder in the same directory
- The build will fail if it's not there
- This is a very basic example and all the build will do is add the   `use strict` flag
- It will also change the const variable into a `var` in the built file
![babel-command-to-build-from-the-terminal](https://user-images.githubusercontent.com/5911897/213966016-62799872-45bd-4e4b-95b7-7af409a51fa1.PNG)
___
## Ignoring node_modules 
<b>Add any `.env` file that has authentication into the ignore file always
We run the basic command in the terminal run babel
Note: A bunch of new files will be created that we don't want
- Remove them by adding the `node_modles` int the .gitignore file up top
- Remove any cached modules by entering 
- git rm -r --cached node_modules
- Check by enterting git status in the terminal
___
## In case node_modules are pushed to the repository
Note: The large output of files will no longer be pushed to the repository
- Sometimes we forget to add the files that will be ignored
- This is also important as we don't want to add any keys that someone may use 
- This keys are created in a .env folder (add this to the same .gitignore) file
- This helps to keep credentials secure but is not related to this example here 

- All should be green to commit if not then add git add . 
- Followed by a commit message git commit -m "la di da example message"
- git push (set upstream if it hasn't been set)
