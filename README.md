# surge-github-autorelease

This node module will deploy your statics via surge to view your changes easily after either pull request or regular commit to master.

For pull request, the url of the preview is added to the Github commit status section. Otherwise the preview url is `https://${domain}.surge.sh`.

#### Quick Start
All you have to do is to add surge-github-autorelease as a dev dependency `npm install surge-github-autorelease --save-dev` and run `surge-github-autorelease` with the appropriate arguments in your release script, for example in your `package.json` file, in the `release` script add: `surge-github-autorelease -r $REPO_SLUG -s $STORYBOOK_DIST -b . -p $PULL_REQUEST -t $GITHUB_API_TOKEN -d $DOMAIN;`

#### `Arguments`

| Argument name            | Description                             | Example            |
| ------------------------ | ---------------------------------------- |------------------ |
| -o                     | Repo Owner Name  |wix|
| -n                     | Repo Name  |wix-style-react|
| -b                     | Root path to build agent root directory| . |
| -s                     | static files directory                          | storybook-dist|
| -p                     | Pull request number                          |1455|
| -t                     | Github authentication token                          |ad2jhdjhShi10axK0NENEK0bcnshd|
| -d                     | Domain                          |wix-wix-style-react|

#### Status Example

![example](https://snag.gy/S2qgBj.jpg)
