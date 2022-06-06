###Install Dependencies

npm install

### Test

We use Karma with the Jasmine test framework to run unit tests. Try them with

`ng test`

This will start a persistent process which will re-run tests whenever the `.js`
compiled files are changed. If you have the watch process running, that will
trigger the tests to run whenever you change the `.ts` source files.

You can see the Karma configuration at `karma.conf.js`. A few things are notable:

 - It grabs Angular by including the `angular2` and `testing.js` files from
 `node_modules/angular2/bundles/`.

 - The compiled JavaScript files at `src/**/*.js` are served and watched but _not_ included.
 This means that Karma will not run them automatically.

 - To get file imports to work correctly in Karma, we must include `systemjs`
 from the node_modules folder, as well as the helper file `karma-test-shim.js`.
 This shim file uses System.js to load the JavaScript files which Karma served
 but did not automatically run.

the e2e folder holds the end-to-end tests
 # tictactoe_test
