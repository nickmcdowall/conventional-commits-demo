[![semantic-release](https://img.shields.io/badge/semantic-release-e10079.svg?logo=semantic-release)](https://github.com/semantic-release/semantic-release)

# Conventional Commits Demo
[![GitHub release](https://img.shields.io/github/release/nickmcdowall/conventional-commits-demo)](https://github.com/nickmcdowall/conventional-commits-demo/releases)
[![Automated Release](https://github.com/nickmcdowall/conventional-commits-demo/actions/workflows/release.yml/badge.svg)](https://github.com/nickmcdowall/conventional-commits-demo/actions/workflows/release.yml)

A project that uses the [semantic-release](https://github.com/semantic-release/semantic-release) github [action](https://github.com/marketplace/actions/action-for-semantic-release) to automate the github release process (including the semantic versioning and changelog) based purely on the commit message conventions.

## Build

Install the custom git hook to help validate you commit messages
```shell
./gradlew installGitHooks
```

Now you can have a play with creating valid commits and triggering semantic releases when you push!

# Releated links
* [Conventional commits specification](https://www.conventionalcommits.org/en/v1.0.0/)
* [Semantic Release repository](https://github.com/semantic-release/semantic-release)
* [Semantic Release Github Action](https://github.com/marketplace/actions/action-for-semantic-release)

## Files of interest
* [release.yml](.github/workflows/release.yml) : The github workflow file (needs to include additional plugins used in the `.releaserc.yaml` file )
* [.releaserc.yaml](.releaserc.yaml) : The configuration file for semantic-release

### Custom githooks
Repository specific hooks are in the .githooks directory so that they can be committed and shared
Git will need to be configured on each users' machine to add the `.githooks` directory with `git config core.hooksPath .githooks`