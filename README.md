
# Conventional Commits Demo
[![GitHub release](https://img.shields.io/github/release/nickmcdowall/conventional-commits-demo)](https://github.com/nickmcdowall/conventional-commits-demo/releases)
[![semantic-release](https://img.shields.io/badge/semantic-release-e10079.svg?logo=semantic-release)](https://github.com/semantic-release/semantic-release)

Demonstration project (non node) that uses the conventional commits specification along with the semantic-release tool
to automate release versioning and release notes based on the git commit messages.

## Conventional Commits
For git message specification see: https://www.conventionalcommits.org/en/v1.0.0/

For node plugin that does the work see: https://github.com/semantic-release/semantic-release

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
  * Needs to run something like `npx semantic-release` (locally I needed to override the dry-run mode with `--no-ci`)
* Test when integrated with maven central releasing