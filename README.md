[![Build Status](https://travis-ci.org/ibm-cloud-solutions/hubot-ibmcloud-app-management.svg?branch=master)](https://travis-ci.org/ibm-cloud-solutions/hubot-ibmcloud-app-management)
[![Coverage Status](https://coveralls.io/repos/github/ibm-cloud-solutions/hubot-ibmcloud-app-management/badge.svg?branch=master)](https://coveralls.io/github/ibm-cloud-solutions/hubot-ibmcloud-app-management?branch=master)
[![Dependency Status](https://dependencyci.com/github/ibm-cloud-solutions/hubot-ibmcloud-app-management/badge)](https://dependencyci.com/github/ibm-cloud-solutions/hubot-ibmcloud-app-management)
[![npm](https://img.shields.io/npm/v/hubot-ibmcloud-app-management.svg?maxAge=2592000)](https://www.npmjs.com/package/hubot-ibmcloud-app-management)

# hubot-ibmcloud-app-management

A hubot script for management of your the IBM Cloud apps.

## Getting Started
* [Usage](#usage)
* [Commands](#commands)
* [Hubot Adapter Setup](#hubot-adapter-setup)
* [Cognitive Setup](#cognitive-setup)
* [Development](#development)
* [License](#license)
* [Contribute](#contribute)

## Usage

Steps for adding this to your existing hubot:

1. `cd` into your hubot directory
2. Install the app management functionality with `npm install hubot-ibmcloud-app-management --save`
3. Add `hubot-ibmcloud-app-management` to your `external-scripts.json`
4. Add the necessary environment variables:
```
export HUBOT_BLUEMIX_API=<Bluemix API URL>
export HUBOT_BLUEMIX_ORG=<Bluemix Organization>
export HUBOT_BLUEMIX_SPACE=<Bluemix space>
export HUBOT_BLUEMIX_USER=<Bluemix User ID>
export HUBOT_BLUEMIX_PASSWORD=<Password for the Bluemix use>
```

5. Start up your bot & off to the races!

## Commands <a id="commands"></a>
- `hubot app help` - Show available commands for app management.
- `hubot app delete [app]` - Delete an app.
- `hubot app list` - List apps.
- `hubot app logs [app]` - Show logs for an app.
- `hubot app restage [app]` - Restage an app.
- `hubot app restart [app]` - Restart an app.
- `hubot app scale [app]` - Scale an app to change instances, memory, and disk space.
- `hubot app start [app]` - Start an app.
- `hubot app status [app]` - Get status for an app.
- `hubot app stop [app]` - Stop an app.

## Hubot Adapter Setup

Hubot supports a variety of adapters to connect to popular chat clients.  For more feature rich experiences you can setup the following adapters:
- [Slack setup](https://github.com/ibm-cloud-solutions/hubot-ibmcloud-app-management/blob/master/docs/adapters/slack.md)
- [Facebook Messenger setup](https://github.com/ibm-cloud-solutions/hubot-ibmcloud-app-management/blob/master/docs/adapters/facebook.md)

## Cognitive Setup

This project supports natural language interactions using Watson and other Bluemix services.  For more information on enabling these features, refer to [Cognitive Setup](https://github.com/ibm-cloud-solutions/hubot-ibmcloud-nlc/blob/master/docs/cognitiveSetup.md).

## Development

Please refer to the [CONTRIBUTING.md](https://github.com/ibm-cloud-solutions/hubot-ibmcloud-app-management/blob/master/CONTRIBUTING.md) before starting any work.  Steps for running this script for development purposes:

### Configuration Setup

1. Create `config` folder in root of this project.
2. Create `env` in the `config` folder, with the following contents:
```
export HUBOT_BLUEMIX_API=<Bluemix API URL>
export HUBOT_BLUEMIX_ORG=<Bluemix Organization>
export HUBOT_BLUEMIX_SPACE=<Bluemix space>
export HUBOT_BLUEMIX_USER=<Bluemix User ID>
export HUBOT_BLUEMIX_PASSWORD=<Password for the Bluemix use>
```
3. In order to view content in chat clients you will need to add `hubot-ibmcloud-formatter` to your `external-scripts.json` file. Additionally, if you want to use `hubot-help` to make sure your command documentation is correct. Create `external-scripts.json` in the root of this project
```
[
    "hubot-help",
    "hubot-ibmcloud-formatter"
]
```
4. Lastly, run `npm install` to obtain all the dependent node modules.

### Running Hubot with Adapters

Hubot supports a variety of adapters to connect to popular chat clients.

If you just want to use:
 - Terminal: run `npm run start`
 - [Slack: link to setup instructions](https://github.com/ibm-cloud-solutions/hubot-ibmcloud-app-management/blob/master/docs/adapters/slack.md)
 - [Facebook Messenger: link to setup instructions](https://github.com/ibm-cloud-solutions/hubot-ibmcloud-app-management/blob/master/docs/adapters/facebook.md)


## License

See [LICENSE.txt](https://github.com/ibm-cloud-solutions/hubot-ibmcloud-app-management/blob/master/LICENSE.txt) for license information.

## Contribute

Please check out our [Contribution Guidelines](https://github.com/ibm-cloud-solutions/hubot-ibmcloud-app-management/blob/master/CONTRIBUTING.md) for detailed information on how you can lend a hand.
