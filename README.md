


## Conventional Commits
For specification see: https://www.conventionalcommits.org/en/v1.0.0/

## Steps
* Install nvm
  * ```curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash```
* Install node
  * `nvm install node` 
* Created account in npm registry
  * https://www.npmjs.com/
  * Looks like this was only required when the npm publish plugin was being used (by default). Now that it's not included in explicit plugins I believe this step can be ignored.
* Create `GITHUB_TOKEN` variable
  * containing a personal token with push access to the repo so that the tags and release (with changelog) can be auto-generated

TODO
* Add Github action to automate the release versioning etc.
* Test when integrated with maven central releasing