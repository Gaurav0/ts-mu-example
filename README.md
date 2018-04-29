# ts-mu-experiment

An experiment in using ember-cli-typescript and module unification together

## Created as follows:

```bash
yarn global add ember-cli#master
MODULE_UNIFICATION=true ember new ts-mu-experiment --yarn
cd ts-mu-experiment

# update ember-source version in package.json
# Remove ember-welcome-page from package.json
# Edit src/routes/applicaton.hbs to remove {{welcome-page}}
yarn

ember install ember-cli-typescript
ember g component some-input

yarn add ember-modules-codemod --dev
./node_modules/.bin/ember-modules-codemod
yarn remove ember-modules-codemod

yarn add ember-modules-migrator --dev
yarn add jscodeshift --dev
./node_modules/.bin/ember-module-migrator

# Add some-input contents from http://www.chriskrycho.com/2017/typing-your-ember-part-1.html 
```


## Prerequisites

You will need the following things properly installed on your computer.

* [Git](https://git-scm.com/)
* [Node.js](https://nodejs.org/)
* [Yarn](https://yarnpkg.com/)
* [Ember CLI](https://ember-cli.com/)
* [Google Chrome](https://google.com/chrome/)

## Installation

* `git clone <repository-url>` this repository
* `cd ts-mu-experiment`
* `yarn install`

## Running / Development

* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).
* Visit your tests at [http://localhost:4200/tests](http://localhost:4200/tests).

### Code Generators

Make use of the many generators for code, try `ember help generate` for more details

### Running Tests

* `ember test`
* `ember test --server`

### Linting

* `yarn lint:js`
* `yarn lint:js --fix`

### Building

* `ember build` (development)
* `ember build --environment production` (production)

### Deploying

Specify what it takes to deploy your app.

## Further Reading / Useful Links

* [ember.js](https://emberjs.com/)
* [ember-cli](https://ember-cli.com/)
* Development Browser Extensions
  * [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
  * [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)
