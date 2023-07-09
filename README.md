# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

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

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

# Tutorial And Notes

## Creating A React App

To create a react app, run the following command

`npx create-react-app react-admin`

The `react-admin` is the name of the project. This code requires `npx` being installed. It will throw an error if it isn't. You can install `npx` using the following command: `npm install -g npx`

## Install Supporting Libraries

This tutorial is built on [Material UI](https://mui.com), an onpen-source library for creating UI elements. The instructions for installing it are on the website. The code is:

`npm install @mui/material @emotion/react @emotion/styled @mui/x-data-grid @mui/icons-material react-router-dom@6 react-pro-sidebar formik yup @fullcalendar/core @fullcalendar/daygrid @fullcalendar/timegrid @fullcalendar/list @nivo/core @nivo/pie @nivo/line @nivo/bar @nivo/geo`

This installs all the libraries used to design the Dashboard including

1. React Router
2. React Pro Sidebar
3. Formik
4. Yup
5. Full Calendar (https://fullcalendar.io/)
6. Nivo (https://nivo.rocks/)

## Delete Unnecessary Files

There some files which are created as part of the setup which will be deleted. These include:

- setupTests.js
- reportWenVitals.js
- logo.svg
- App.test.js
- App.css

Following this, go to `index.js` and remove references to the deleted files

## Edit App.js, index.js and index.css

Open `App.js` and remove the default code. This includes the imports and the Components used to display the default home page. Also, change the appName value from 'App' to 'app'.

Following that, open `index.js` and import BrowserRouter. This will allow us to use React Router and set up Routes.

After importing BrowserRouter, wrap up <App /> in <BrowserRouter>. This will leave `index.js` looking like this:

```import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';
import { BrowserRouter } from 'react-router-dom';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </React.StrictMode>
);
```

### Edit index.css

Go to Google Fonts and search for _Source Sans 3_. The video actually says _Source Sans Pro_ but I wasn't able to locate that. Add a Regular 400, 600 and 700. Select the @import, copy the URL and paste it in index.css

### Add Mock Data

Create a folder called `data` in the src directory and copy the mock data from the [Github link](https://github.com/ed-roh/react-admin-dashboard/tree/master/src/data) in the YouTube video description.

## Run the App

Run the app using `npm start`. This will start the server and give you a set URLs which looks like this:

Local: http://localhost:27133  
 On Your Network: http://172.21.48.1:27133

These can be used to access the App on the web. Please note that running `npm start` can bring prompts about selecting the PORT NUMBER. Accept and proceed.

## Organize Your Files & Folders
