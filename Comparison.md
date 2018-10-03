# Things to note

1. After running `npm install --save-dev`, vulnerabilities found 260 vulnerabilities (227 low, 25 moderate, 6 high, 2 critical).
2. Nothing was broken, the application still works the way it used to.

## What was added

End to end testing using Cypress.io test runner.

## What did it fix

The project lacked any test.

## Files added and what it does

  1. cypress.json - When a project is added to Cypress a cypress.json file is created. It contains two variables.
      * viewportHeight - 	Default height in pixels for the application under tests.
      * defaultCommandTimeout - Time, in milliseconds, to wait until most DOM based commands are considered timed out.
  2. The Cypress Folder
      | fixtures
        | example.json - Are used as external pieces of static data that can be used by your tests.
      | integration
        | spec.js - Is the test file.
      | plugins
        | index.js - Used to load plugins.
      | support
        | commands.js -This file is empty.
        | index.js - Imports command.js.

## Files Edited

1. package.json
    Two test build scripts were added to the scripts section.
      test - `npm run test` runs the test without the dashboard.
      test:gui - `npm run test:gui` runs the test with the dashboard.
    Two modules were added to devDependecies section.
      cypress
      lolex
2. store/en/index.js
    Commas were added.
3. src/components/LocaleSwitcher.vue
    `<select v-model="selectedLanguage" data-attr-cy="language">` was added.

## End to End Testing

This was written with Cypress.io test runner. It runs only on Chrome Web Browser. The tests are exercising all methods, except for `find`. Each test grabs the code from the input, evaluates it and compares to the shown output.

Cypress is a JavaScript based end to end testing framework that doesn’t uses selenium at all. It is built on top of mocha which is again a feature-rich JavaScript test framework running on Node.js and in the browser, making asynchronous testing simple and fun. is a front end testing tool built with the modern web. It is easy to Set Up, write, Run and debug tests. Anything that runs in a browser can be tested using Cypress.

## Advantages of Using Cypress

1. Easy and reliable testing for anything that runs on the web.
2. Free and open source.
3. Ability to either stub responses or to let them hit your server.
4. Rich docmentation.
5. Auto reload
6. Easy to debug.
7. Automatic waiting nevwe add sleeps or wait to your tests.
8. Works on Network Layer.

## Disadvantages of Using Cypress

1. It only supports Chrome.
