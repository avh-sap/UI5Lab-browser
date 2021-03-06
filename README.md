![UI5Lab Logo](https://github.com/UI5Lab/UI5Lab-central/blob/master/docs/media/UI5LabLogoPhoenix.png)

# What is it
UI5Lab is a community driven repository for UI5 Custom Control Libraries. It's purpose is to make it easy for everyone to share, retrieve and use UI5 Custom Controls. Contributions welcome!

# UI5Lab-browser
This repository contains a browser to display custom libraries and control examples on the UI5Lab homepage. The app implemented in UI5 can also be used for testing control samples and previewing libraries during development. Have a look at our [documentation](http://ui5lab.io/docs/) for more details. 

#### Setup

Run the following commands to test or develop this project:

1. Install node.js (get it from [nodejs.org](http://nodejs.org/)).

> **Note:** If working behind a proxy, you need to configure it properly (HTTP_PROXY / HTTPS_PROXY / NO_PROXY environment variables)

2. Clone the repository and navigate into it

```sh
git clone https://github.com/UI5Lab/UI5Lab-browser
cd UI5Lab-browser
```

3. Install all npm dependencies (also installs all bower dependencies)

```sh
npm install
```

4. Run npm start to a local server (have a look into `Gruntfile.js` to see all the tasks).

```sh
npm start
```

5. Open the browser with the following URL: [http://localhost:8080/test-resources/ui5lab/browser/index.html](http://localhost:8080/test-resources/ui5lab/browser/index.html)

> **Note:** To test the browser, one or more libraries should be defined as a dependency and registered in the libraries.json file. See the UI5Lab-central project for more details

#### Publishing the to npm

The library project and the central project reference the browser via npm module. In order to publish a new version to npm follow these steps:

1. Maintain the package.json file and increase the version number


2. Run grunt build to create a library preload and the CSS theme build for your library artifacts. Everything (minified and unminified sources) will be created in the ```dist``` folder, ready to be published and consumed by other projects

```sh
grunt build
```

3. Publish your package to npm, be sure to include only the metadata and the dist folder to keep the package size small (see .npmignore file for details) 

```sh
npm publish
```

> **Note:**  Official UI5Lab packages have to be published with the user ```ui5lab```, if you do not have permission ask a member the UI5Lab core team 


# Directions

* [Homepage](https://ui5lab.io) - the single point of entry for UI5Lab
* [Documentation](https://ui5lab.io/docs) - project overview and tutorials
* [Browser](https://ui5lab.io/browser) - all UI5Lab libraries and examples
* [Demo](https://ui5lab.github.io/UI5Lab-app-simple/index.html) - an example app consuming simple UI5Lab controls

# Troubleshooting

Issues can be created either in this repository or in any of the contributor repositories depending on where the error came from.
Be sure to include enough details and context to reproduce the issue and follow up with you. 

# Contact

We organize this project in [Slack Channel #UI5Lab](https://openui5.slack.com/messages/UI5lab).
If you are interested in what we do and discuss, join with this [invitation link](http://slackui5invite.herokuapp.com/) or visit the homepage [https://ui5lab.io](https://ui5lab.io).

*The UI5Lab Community*
