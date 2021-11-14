
# Conventional Commits Demo
[![GitHub release](https://img.shields.io/github/release/nickmcdowall/conventional-commits-demo)](https://github.com/nickmcdowall/conventional-commits-demo/releases)
[![semantic-release](https://img.shields.io/badge/semantic-release-e10079.svg?logo=semantic-release)](https://github.com/semantic-release/semantic-release)
[![Automated Release](https://github.com/nickmcdowall/conventional-commits-demo/actions/workflows/release.yml/badge.svg)](https://github.com/nickmcdowall/conventional-commits-demo/actions/workflows/release.yml)

Demonstration project (non node) that uses the conventional commits specification along with the semantic-release tool
to automate release versioning and release notes based on the git commit messages.

## Conventional Commits
For git message specification see: https://www.conventionalcommits.org/en/v1.0.0/

For node plugin that does the work see: https://github.com/semantic-release/semantic-release

## Steps

### Run locally
* Install nvm
  * ```curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash```
* Install node
  * `nvm install node` 
* Create `GITHUB_TOKEN` variable
  * containing a personal token with push access to the repo so that the tags and release (with changelog) can be auto-generated

### Run via Github Action
* Add an action in the workflows directory that uses the semantic-release action
  * See `.github/workflows/release.yml` for an example
