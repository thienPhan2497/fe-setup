# Getting Started with FE project set up

<p align="center">
  <img alt="AXL" src="magic-logo.jpg" width=300/>
</p>

> Enhance your code quality

## Setup Scripts

``` scripts
+ npm create-react-app feSetUp
+ npm i -D eslint eslint-config-airbnb
+ npx eslint --init                                |------------------------------------------> Config .eslintrc.json
+ npm i -D --save-exact prettier                   |------------------------------------------> Config .prettierrc.json
+ npm i -D eslint-config-prettier                  |------------------------------------------> Add prettier to the last of extends in .eslintrc.json:
                                                                                        Turns off all eslint rules that are unnecessary or might conflict with Prettier, eslint only check code syntax style while Prettier check code formatting
+ npm i -D concurrently                            |------------------------------------------> Multiple script running
+ npx mrm@2 lint-staged                            |------------------------------------------> Config pre-commit, this will install both husky and lint-staged

+ npm i -D eslint-plugin-import                    |------------------------------------------> Config .eslintrc.json with more rules and should be used with typescript
```

> It will take a little time the first time.  Be patient.

- npm i webpack webpack-cli html-webpack-plugin webpack-dev-server babel-loader css-loader -D

### Running Storybook

Start the storybook locally on port 3000.

``` dev
npm start
```

## Merging/Releases

The versioning is also automated via a [conventional commit](https://www.conventionalcommits.org/en/v1.0.0/#summary) as the commit message for your squashed commit to master.

Examples:

For a patch release

`fix:🐛 Correct the import mistakes we messed up (#1234)`

For a minor release

`feat:✨ Add a new feature that we all love and need (#1234)`

Using emoji [Gitmoji](https://gitmoji.dev/)

``` emo
"🐛 Fix: Fixed bug"
"🚀 Successfully merge"
"📄 Doc: Updated"
"✨ Introduce new features"
"✅ Add, update, or pass tests"
"♻️ Refactor code"
```

## Code Quality

JS code is linted by [ESLint](https://eslint.org/) while our SCSS code is linted by [Stylelint](https://github.com/stylelint/stylelint).

Code quality checks are run on every commit and every push to origin.

You can also be run manually via the following commands:

- `npm run lint:js`
- `npm run lint:css`

## Unit Tests

```npm test```

React components should take full advantage of [jest snapshots](https://jestjs.io/docs/en/snapshot-testing) to test dom structure, props, and attributes.

### Words

- --save-exact ensures that everyone will install the same version of prettier to avoid inconsistency
- npm:format meaning npm run format
- concurrently: using for multiple scripts with chalk package color
- beta.emojipedia.org: for icon in bash

### Useful Links

- [Git Hooks and Husky](https://www.git-tower.com/blog/git-hooks-husky/)
- [ESLint, Prettier and Husky](https://dev.to/ivadyhabimana/setup-eslint-prettier-and-husky-in-a-node-project-a-step-by-step-guide-946)
- [Pre-commit Hook](https://prettier.io/docs/en/precommit.html)
- [LintStyle css](https://dev.to/nausaf/set-up-linting-and-formatting-for-code-and-scss-files-in-a-nextjs-project-43fb)
