# HungryHub Project Notes

## Backend Setup 
- Open terminal
    - Type `npm init -y`
        - this will install the package.json file so that different npm packages can be installed. 
    - Type `npm i express cors dotenv mongodb mongoose`
        - express: it's used on the backend to handle the API requests that come from the frontend.
        - cors: it helps to configure the backend to accept or block requests that come from different domains and ports and stuff like that. 
        - dotenv: it's used to load environment variables. 
        - mongodb and mongoose: used to help interact with the database in a developer friendly way from the backend code. 
    - Type `npm i ts-node typescript nodemon @types/express @types/cors @types/node --save-dev`
        - typescript: it's going to install typescript into the project and will provide a config file which will enable adjustment of typescript settings.
        - nodemon: it will allow hot-reloading which means that whenever changes are made to the backend code the server will automatically restart and provide the latest changes. 
        - the `@types...` provides the types for the previously installed packages which helps get intellisense and stuff like that. 
    - Open package.json file in order to change some properties
        - go to the main property and change from `"main": "index.js"` to
        `"main": "./src/index.ts"`
        - go to the scripts and delete the properties and instead it should say `"scripts": { "dev" : "nodemon" },`
- Open up the terminal again
    - Type `npx tsc --init`
- Go back into the VSCode explorer
    - Create a new folder called `src`
    - Inside of the `src` folder create a new file called `index.ts`
        - Inside the `index.ts` folder it will be used to 
            - Initialize Express 
            - Add API routes
            - Add connections to Stripe and MongoDB
            - Define roots
            - Start the server
- Go to the `index.ts` file inside the `src` folder
    - There are notes there to understand what was typed up
- Go to the terminal
    - Type `npm run dev` and below are the results
    ![Example](https://i.imgur.com/7YFSuya.png)
    - It just shows that it is following where I told it to go in the `package.json` file has the console message. 
- Open up a browser tab
    - Type `localhost:7000/test` and below are the results
    ![Example](https://i.imgur.com/nFjGMFx.png)
    - It proves that the backend server has started and that I make requests.

## Frontend Setup


