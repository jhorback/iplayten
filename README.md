# &lt;ipt&gt;

 * This application uses Node, Polymer, and Firebase. 
 * Install these before running tasks.

## Environments
> Production - [iplayten.com](https://iplayten.com)

> Staging - [iplayten-staging.firebase.com](https://iplayten-staging.firebaseapp.com)



# Npm tasks (npm run ...)

## Build
* **polybuild** - Generates the build files by running `polymer build` which is configured by `polymer.json`.

## Serve
* **polyserve** - Opens the root index page by running `polymer serve -o`. Uses the static staging configuration.
* **fireserve** - Runs polybuild, sets the firebase alias to staging, then runs a local firebase server.

## Test
* **polytest** - Runs all tests using `polymer test`.

## Doc
* **polydoc** - Generates the `analysis.json` (used by the documentation).

## Deploy
* **push-staging** - Pushes the current state to the staging url. (builds, but skips the tests).
* **deploy-staging** - Runs tests, polybuild, and firebase deploy in the staging environment. (https://iplayten-staging.firebaseapp.com)
* **deploy-production** - Runs tests, polybuild, and firebase deploy on default (PUSHES TO PRODUCTION). (https://iplayten.com)

# Polymer tasks
Notable Polymer cli commands that can be run directly.
* **polymer serve -o** - Run this to serve the static app locally using the polymer server.
* **polymer test** - Runs all polymer tests: `tests/index.html`.
* **polymer build** - Builds the poylmer app. Uses the `polymer.json` build configuration.
* **polymer analyze > analysis.json** - Outputs the `analysis.json` for element documentation.

# Firebase tasks
* **firebase use** - Lists all aliases for the current environment.
* **firebase use {default}** - Sets the environment for Firebase to use. Currently, it can be "default" or "staging".
* **firebase deploy** - Deploys the current codebase to the environment currently in "use".
* **firebase deploy -P staging** - The -P flag sets the environment to deploy to.
* **firebase deploy --only hosting, functions, database, storage, firestore** - Limits the firebase deploy to only the stated features.
* **firebase open** - Shows a list of firebase console screens to open
