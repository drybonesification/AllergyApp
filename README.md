# AllergyApp

## Notes for Developers

* Words are scary and there are a lot of them here. How do I get started?

  * Clone this repo to a local directory.
  * Run `npm install` in this local directory to install all the `Node.js`
    dependencies according to the `package.json` file.
  * Edit [VSCode settings file](#vscode-settings-file).
  * Install [VSCode extensions](#vscode-extensions).

* This was initially created using the npm package
  [`create-react-app`](https://github.com/facebookincubator/create-react-app).
  Information about its configuration and gotchas are available at that link.

  * Note: `create-react-app` bundles `Webpack` along with `Jest` (testing) and
    `Enzyme` (testing). If/when we get to the stage of needing to edit these
    configurations, we'll need to `eject` this app and then we'll get a dumpster
    full of configuration files to work with. **Note that `eject` is a one-way
    process.**

* See the `GH_Docs` folder for some quick configuration information (e.g.
  enabling Git Flow in GitKraken)

* Bundled some useful files/directories that will help us in code uniformity and
  quality. These are

  * `.eslintrc` file for configurating ES Linting rules (this will tell you if
    you initialize a variable you don't use, etc.)
  * `.travis.yml` file for connecting up to a
    [Travis-CI](https://travis-ci.org/) service. I'll work with Chuy on setting
    this up, as the free version isn't able to be used on a repo that you don't
    own.
  * `.vscode` directory for launching the Chrome debugging plugin for VSCode

* Added some `devDependencies` to the `package.json` file. These are used for
  code assurance (`eslint`), testing (`codecov` and `mocha`), and Doing Future
  Things(TM) (`react-scripts`).

  ```js
  "devDependencies": {
    "ajv": "^5.5.0",
    "codecov": "^3.0.0",
    "eslint": "^4.12.1",
    "eslint-config-airbnb": "^16.1.0",
    "eslint-config-react-app": "^2.0.1",
    "eslint-plugin-import": "^2.8.0",
    "eslint-plugin-jsx-a11y": "^5.1.1",
    "eslint-plugin-react": "^7.5.1",
    "eslint-plugin-security": "^1.4.0",
    "eslint-watch": "^3.1.3",
    "mocha": "^4.0.1"
  },
  ```

* Added a `dependency` to the `package.json` file. We'll need this for our
  `.env` file **that should never go to the GitHub repo**, which we'll use to
  hold at least two API configuration variables.
  ```js
  "dotenv": "^4.0.0",
  "lodash": "^4.17.4",
  ```

### VSCode Settings File

* Here is a VSCode Settings file (`File -> Preferences -> Settings`) which may
  be useful. It handles the linting options as well as formatting on save. If
  we're not using the same prettifier or not formatting on save, we'll suddenly
  have _thousands_ of changes with each push as each space or comma
  placement/omission will count as another change. We will save tons of pain by
  using this:

  ```js
  {
    "editor.formatOnSave": true,
    "window.zoomLevel": 0,
    "editor.wordWrap": "on",
    "editor.fontSize": 16,
    "prettier.eslintIntegration": true,
    "eslint.enable": true,
    "eslint.packageManager": "npm",
    "eslint.alwaysShowStatus": true,
    "eslint.options": { "configFile": ".eslintrc" },
    "eslint.run": "onType",
    "eslint.validate": ["javascript", "javascriptreact"]
  }
  ```

### VSCode Extensions

* There are also some _exceedingly_ useful VSCode extensions that will make
  development significantly easier. The really useful ones are in **bold**:

  * [**Debugger for Chrome**](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)
  * [**ESLint**](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
  * [HTML CSS Support](https://marketplace.visualstudio.com/items?itemName=ecmel.vscode-html-css)
  * [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
  * [Markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
  * [Preview](https://marketplace.visualstudio.com/items?itemName=searKing.preview-vscode)
  * [**Prettier - Code formatter**](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
  * [**Rainbow Brackets**](https://marketplace.visualstudio.com/items?itemName=2gua.rainbow-brackets)
  * [React/Redux/react-router Snippets](https://marketplace.visualstudio.com/items?itemName=discountry.react-redux-react-router-snippets)
  * [**Syncing**](https://marketplace.visualstudio.com/items?itemName=nonoroazoro.syncing)
