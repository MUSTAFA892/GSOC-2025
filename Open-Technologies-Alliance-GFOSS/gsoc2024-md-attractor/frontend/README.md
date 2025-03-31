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


# Installation Issue

When running `npm install`, you may encounter the following error:

```
npm error code ERESOLVE
npm error ERESOLVE could not resolve
npm error
npm error While resolving: react-vis-network@1.0.0
npm error Found: react@18.3.1
npm error node_modules/react
npm error   react@"^18.3.1" from the root project
npm error   peer react@"^18.0.0" from @testing-library/react@13.4.0
npm error   node_modules/@testing-library/react
npm error   @testing-library/react@"^13.4.0" from the root project
npm error   7 more (react-dom, react-graph-vis, react-loader-spinner, ...)
npm error
npm error Could not resolve dependency:
npm error peer react@"^16.0.0" from react-vis-network@1.0.0
npm error node_modules/react-vis-network
npm error   react-vis-network@"^1.0.0" from the root project
npm error
npm error Conflicting peer dependency: react@16.14.0
npm error node_modules/react
npm error   peer react@"^16.0.0" from react-vis-network@1.0.0
npm error   node_modules/react-vis-network
npm error   react-vis-network@"^1.0.0" from the root project
npm error
```

This error occurs because there is a conflict between the version of `react` installed in your project (`react@18.3.1`) and the peer dependency required by the `react-vis-network` package (`react@^16.0.0`).

### Resolution

To resolve this issue, use the following command to bypass the peer dependency conflict:

```bash
npm install --legacy-peer-deps
```

### Explanation

- The `--legacy-peer-deps` flag tells npm to ignore the peer dependency conflicts and install the packages anyway.
- This is useful when you're working with packages that have not been updated to support the latest versions of their dependencies, or when you're using specific versions of libraries that are incompatible with the latest versions.
 