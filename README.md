# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `yarn build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

# 
# 

# Setting Up React onto GitHub Pages Steps

*Notes from: https://www.youtube.com/watch?v=ctLFWAanxcI*

## Step 1 - Set up Yarn and React on local computer

> Do NOT setup Github repository and link it to the local folder yet 

1. Create a folder on your desktop Example: new1
2. Open up VS code and open up terminal and navigate into that folder
3. Then type in the terminal: 
`npm i -g yarn` 
6. Create the react app now locally by typing in the terminal:
`npx create-react-app hello-world` 
> The hello-world will be the name of the folder locally but will not show up later in GitHub
7. Go into the folder now by typing in terminal:
`cd hello-world` 
8. To test out the starter React code on Localhost type in terminal:
`yarn start` 
> go to localhost:3000 in web browser. To exit the terminal in deploying locally type in `ctrl + C`

## Step 2 - Remove GitHub Credentials
1. Open up Credential Manager on Windows
2. Click on Windows Credentials
3. Remove any github credentials
4. Make sure you are signed into your account on a web browser (not in incognito mode) where you want the file to be uploaded to. You want to do this because once we start adding the files to github it will ask to connect with a GitHub account you are signed into in your browser.

## Step 3 - Setup GitHub Repository
1. Create a new repository by going to your web browser and log into your account. Call it for example:
`github-pages-create-react-app`
> Keep all the other settings to default. Add a description if you want.
2. Go back to the terminal and if you haven't closed the localhost and hold down the keys:
`ctrl + C`
3. Then type in terminal: 
`yarn add gh-pages` 
4. Add all the files to github by typing in terminal:
`git add .`
5. Then Type in the terminal:
`git commit -m "first commit"`
> this will just add a comment whenuploading to github.
6. Then type in the terminal:
`git push -u origin master`

> If this doesn't work then run \
`git remote add origin <URL>` \
`git push origin master`
> It will then ask you to log into your GitHub account. Make sure you are logged into the right account on the browser.
7. Refresh teh github page to see the files that have been added to GitHub. It should be there.
8. In Github go to Settings > GitHub Pages 
*under sources set it to master branch
9. Then save the settings. This will give you a URL for your github pages site. Save the URL we will need it for the next step.

## Step 4 - Editing Package.json file
1. Open the Package.json file
2. add the homepage key and this is where you will add in the URL:\
![Homepage](https://raw.githubusercontent.com/reportex-development/react-base-template/master/public/code-homepage.png)
> You can check the package.json file that was done for this one to see where it was placed.
4. Add a predeploy and a deploy script as well.\
![Script](https://raw.githubusercontent.com/reportex-development/react-base-template/master/public/code-scripts.png)
5. Save the file.
6. Now we can add the changes to GitHub. Go back to the terminal and type:
`git add .`
6. Add a comment in terminal:
`git commit -m "Add GitHub Pages Config."`
7. To deploy to GitHub pages you then need to type into the terminal:
`yarn run deploy`
> It might ask for your github username and password if you aren't already logged in.
8. Go to the web browser and open up the link now. You will only see readme file text right now. We will need to change the Source in GitHub which will be in the next step.

## Step 5 - Changing the GitHub Source
1. Go to GitHub settingsand go to GitHub pages and go to the source section. Change the source to the 
`gh-pages branch`
2. Save the settings.
3. Go to the website url now. This might take a few minutes. But once you refresh the site it should show the react symbole. 
4. Every time you do changed in the file you need to type in terminal:
`yarn run deploy`
5. Then go back to the browser and wait a minute or two then refresh the page and it should show up.
