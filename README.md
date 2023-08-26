# Getting Started with FE project

This project is a boilerplate code for front end project

## Setup Scripts

- npm create-react-app feSetUp
- npm i -D eslint eslint-config-airbnb
- npx eslint --init -> config .eslintrc.json
- npm i -D --save-exact prettier -> config .prettierrc.json
- npm i -D eslint-config-prettier -> Add prettier to the last of extends in .eslintrc.json:
Turns off all eslint rules that are unnecessary or might conflict with Prettier, eslint only check code syntax style while Prettier check code formatting
- npm i -D concurrently  -> multiple script running

- npm i webpack webpack-cli html-webpack-plugin webpack-dev-server babel-loader css-loader -D

### Words

- --save-exact ensures that everyone will install the same version of prettier to avoid inconsistency
- npm:format meaning npm run format
- concurrently: using for multiple scripts with chalk package color
- beta.emojipedia.org: for icon in bash
