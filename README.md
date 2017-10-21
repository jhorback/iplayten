# &lt;ipt&gt;

 * This application uses Node, Polymer, and Firebase. 
 * Install these before running tasks.

## Environments
> Production - [iplayten.com](https://iplayten.com)

> Staging - [iplayten-staging.firebase.com](https://iplayten-staging.firebaseapp.com)



 # Npm tasks
                       
* **npm run polyserve** - Opens the root index page by running `polymer serve -o`.
* **npm run polytest** - Runs all tests using `polymer test`.
* **npm run polydoc** - Generates the `analysis.json` (used by the documentation).
* **npm run polybuild** - Generates the build files by running `polymer build` which is configured by `polymer.json`.
* **npm run stage-push** - Pushes the current state to the staging url. (builds, but skips the tests).
* **npm run stage** - Runs tests, polybuild, and firebase deploy in the staging environment. (https://iplayten-staging.firebaseapp.com)
* **npm run deploy** - Runs tests, polybuild, and firebase deploy on default (PUSHES TO PRODUCTION). (https://iplayten.com)

# Polymer tasks
Notable Polymer cli commands that can be run directly.
* **polymer serve -o** - Run this to serve the static app locally using the polymer server.
* **polymer test** - Runs all polymer tests: `tests/index.html`.
* **polymer build** - Builds the poylmer app. Uses the `polymer.json` build configuration.
* **polymer analyze > analysis.json** - Outputs the `analysis.json` for element documentation.

# Firebase tasks
* **firebase use {default}** - Sets the environment for Firebase to use. Currently, it can be "default" or "staging".
* **firebase deploy** - Deploys the current codebase to the environment currently in "use".
