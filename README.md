# react-project-sonar

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

##First, let’s install the command-line interface for sonar-scanner:

```
npm install sonar-scanner --save-dev
```


Then in package.json, add the following lines to scripts:

```diff
   "scripts": {
		"start": "react-scripts start",
		"build": "react-scripts build",
		"test": "react-scripts test",
		"eject": "react-scripts eject",
+		"build:sonar": "npm run build && npm run sonar",
+		"sonar": "cross-var sonar-scanner -Dsonar.projectVersion=$npm_package_version"
	}
```

And create sonar-project.properties, add the following lines to properties:

```
	sonar.host.url=http://soanrhost:port
	sonar.login=019d1e2e04easdasdasdasdasdasdaerwer
	sonar.projectKey=headwaytechs:react-project-starter
	sonar.projectName=React web app analyzed by SonarQube
	sonar.projectVersion=1.0.0
	sonar.branch=develop
	sonar.log.level=info
	 
	sonar.language=js
	sonar.sources=src
	sonar.sourceEncoding=UTF-8
	sonar.javascript.file.suffixes=.js,.jsx

	# Optional
	sonar.tests=src
	 
	# To import the LCOV report
	#SINCE SONARQUBE 6.2 WITH SONARJS 2.19+
	# comma-separated list of paths to LCOV coverage report files
	sonar.javascript.lcov.reportPaths=coverage/lcov.info,coverage2/lcov.info 
	#WITH OTHER VERSIONS(REMOVED SINCE SONARJS 4.0)
	sonar.javascript.lcov.reportPath=coverage/lcov.info
	sonar.javascript.lcov.itReportPath=coverage/lcov.info
	#Force Coverage to 0 (REMOVED SINCE SONARJS 4.0)
	sonar.javascript.forceZeroCoverage=true
```


## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

### `npm run sonar`

Publish the sonar report for test coverage on the sonar server.<br />
Your app will show coverage and code quality on sonar server!

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
