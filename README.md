# Run Selenium Tests With Jest On Smart UI

## Pre-requisites

Before getting started with Selenium automation testing on LambdaTest, you need to:

* Download and install **NodeJS**. You should be having **NodeJS v6** or newer. Click [here](https://nodejs.org/en/) to download.
* Make sure you are using the latest version of **JavaScript**.
* Install **npm** from the official website by clicking [here](https://www.npmjs.com/).

### Installing Dependencies

```bash
npm i
```

### Running Smart UI test on LambdaTest Cloud 

#### Setting up Your Authentication and Project
Make sure you have your LambdaTest credentials with you to run test automation scripts on LambdaTest Selenium Grid. You can obtain these credentials from the [LambdaTest Automation Dashboard](https://automation.lambdatest.com/build/?utm_source=github&utm_medium=repo&utm_campaign=jest-selenium-webdriver-sample) or through [LambdaTest Profile](https://accounts.lambdatest.com/login/?utm_source=github&utm_medium=repo&utm_campaign=jest-selenium-webdriver-sample).

Set LambdaTest `Username` and `Access Key` in environment variables.
  
  For **Linux/macOS**:
  ```bash
  export LT_USERNAME="YOUR_USERNAME" 
  export LT_ACCESS_KEY="YOUR ACCESS KEY"
  ```
  For **Windows** CMD

```bash
set LT_USERNAME="<Your Username>"
set LT_ACCESS_KEY="<Your Access Key>"
```
  For **Windows** Powershell:
```bash
$env:LT_USERNAME='YOUR USERNAME'
$env:LT_ACCESS_KEY='YOUR ACCESS KEY'
```

Now, navigate to `SmartUI` section from the sidebar and create a new project with the `project type` as the following: 

- **CLI** - For running your `SDK` execution for DOM capture and render on multiple browsers and viewports for comparison.

Set Project Token in environment variables:

For **Linux/macOS**:
  ```bash
  export PROJECT_TOKEN="123456#1234abcd-****-****-****-************"
  ```
  For **Windows** CMD
```bash
set PROJECT_TOKEN="123456#1234abcd-****-****-****-************"
```
  For **Windows** Powershell:
```bash
$env:PROJECT_TOKEN="123456#1234abcd-****-****-****-************"
```

#### Add the Capabilites and Screenshot hook in the test script

- Configure the capabilities 
```js
const capabilities = {
  "browserName": "Chrome",
  "LT:Options": {
    "project": "Smart UI with Jest",
    "build": "jest-sample",
    "w3c": true,
    "plugin": "node_js-jest",
  }
}
```

- Add the Screenshot hook
```js
await smartuiSnapshot(driver, "snapshot-name");
```

#### Run the script
```
npx smartui exec <runCommand> --config <configFilePath>
```

### Running Smart UI test on your local machine

Navigate to `SmartUI` section from the sidebar and create a new project with the `project type` as the following: 

- **CLI** - For running your `SDK` execution for DOM capture and render on multiple browsers and viewports for comparison.

Set Project Token in environment variables:

For **Linux/macOS**:
  ```bash
  export PROJECT_TOKEN="123456#1234abcd-****-****-****-************"
  ```
  For **Windows** CMD
```bash
set PROJECT_TOKEN="123456#1234abcd-****-****-****-************"
```
  For **Windows** Powershell:
```bash
$env:PROJECT_TOKEN="123456#1234abcd-****-****-****-************"
```

#### Add the Screenshot hook in the test script

- Add the Screenshot hook
```js
await smartuiSnapshot(driver, "snapshot-name");
```

#### Run the script
```
npx smartui exec <runCommand> --config <configFilePath>
```


## We are here to help you :headphones:

* Got a query? we are available 24x7 to help. [Contact Us](support@lambdatest.com/?utm_source=github&utm_medium=repo&utm_campaign=jest-selenium-webdriver-sample)
* For more info, visit - [LambdaTest](https://www.lambdatest.com/?utm_source=github&utm_medium=repo&utm_campaign=jest-selenium-webdriver-sample)
