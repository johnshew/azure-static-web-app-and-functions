# Azure Static Web App with Azure Functions

[Azure Static Web Apps](https://docs.microsoft.com/azure/static-web-apps/overview) allows you to easily build JavaScript apps. You can now use [Azure Functions](https://docs.microsoft.com/en-us/azure/static-web-apps/add-api?tabs=vanilla-javascript) as well.

For low traffic sites there is no charge - so free to get one of these up and stay running. This example is deployed [here](https://azure-static-web-app-and-functions.shew.net).

## Installation Prerequisites

* Azure account with an active subscription
    * If you don't have an account, you can create one for [free](https://azure.microsoft.com/en-us/free/)
* Visual Studio Code and two extensions
    * [Azure Static Web Apps](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azurestaticwebapps)
    * [Azure Functions](https://marketplace.visualstudio.com/items?itemName=ms-azuretoolsvscode-azurefunctions)
* [node.js](https://nodejs.org/download/) (if you want to test locally)


## Running on Azure
* Clone this directory
* Inside Visual Studio Code, select the Azure logo in the Activity Bar to open the Azure extensions window
* Under Azure Static Web Apps select '+' to add a new one.
    * Choose your subscription, a name, and a region
    * For the framework select 'Custom' with /src as the location of the files and the build out should be blank
* Make any other changes you want, commit, and push it to the server.

The push will kick off the build and deployment process using the embedded github actions.

## Testing and Running Locally
To run locally you will need:

* Azure Static Web Apps CLI
```bash
npm install -g @azure/static-web-apps-cli
```
* Azure Functions Core Tools
```bash
npm install -g azure-functions-core-tools@3
```

From there you can start the app locally
```bash
swa start src --api-location api
```