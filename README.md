# Getting Started with FE project set up

## Setup Scripts
 ```
+ npm create-react-app feSetUp
+ npm i -D eslint eslint-config-airbnb
+ npx eslint --init                                |------------------------------------------> Config .eslintrc.json`
+ npm i -D --save-exact prettier                   |------------------------------------------> Config .prettierrc.json
+ npm i -D eslint-config-prettier                  |------------------------------------------> Add prettier to the last of extends in .eslintrc.json:
                                                                                        Turns off all eslint rules that are unnecessary or might conflict with Prettier, eslint only check code syntax style while Prettier check code formatting
+ npm i -D concurrently                            |------------------------------------------> Multiple script running
```

> It will take a little time the first time.  Be patient.

- npm i webpack webpack-cli html-webpack-plugin webpack-dev-server babel-loader css-loader -D

### Running Storybook
Start the storybook locally on port 3000.

```
npm start
```

## Merging/Releases
The versioning is also automated via a [conventional commit](https://www.conventionalcommits.org/en/v1.0.0/#summary) as the commit message for your squashed commit to master.

Examples: 

For a patch release

`fix: correct the import mistakes we messed up (#1234)`

For a minor release

`feat: add a new feature that we all love and need (#1234)`

## Code Quality
JS code is linted by [ESLint](https://eslint.org/) while our SCSS code is linted by [Stylelint](https://github.com/stylelint/stylelint).

Code quality checks are run on every commit and every push to origin.

You can also be run manually via the following commands:

* `npm run lint:js`
* `npm run lint:css`

## Unit Tests

```npm test```

React components should take full advantage of [jest snapshots](https://jestjs.io/docs/en/snapshot-testing) to test dom structure, props, and attributes.

### Words

- --save-exact ensures that everyone will install the same version of prettier to avoid inconsistency
- npm:format meaning npm run format
- concurrently: using for multiple scripts with chalk package color
- beta.emojipedia.org: for icon in bash
