# Electron-typescript-react Boilerplate
Quick start your typescript react electron application by cloning and installing

## Install guide 

1. Clone the project
2. run `npm install`
3. once the process ends, run `npm start`. Should you want to watch changes in the main directory as well, run `npm run watch`

## About

I've found countless projects running electron typescript or electron react, but never had a boilerplate for both. I decided to just mince them together.

In this project, the execution of all processes is the root, but the project contains two directories.

### Main
The main directory holds the logic for the main electron process. All electron work should be done here.

The src directory should contain all of the typescript logic. The electron.ts file is the base process for how everything operates.
A dist directory is created when the electron process builds during construction. You shouldn't have to worry about this folder at all :)

In watch mode, nodemon checks changes to the src directory and watches ts files. It causes a recompilation everytime the src folder contains a change, and starts the program anew.

### Renderer
The renderer directory holds the logic of the React Typescript application. Should you wish to not have your react project open in a webpage, run the following command in the root:
```
echo "BROWSER=none" > renderer/.env
```
This will disable the react app opening in the browser.

