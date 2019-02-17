# ubports-mirscreencast

[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

## Getting `semantic-release` working

Main purpose here is to get `semantic-release` working.

* Not yet but have just set tags up to `v0.0.4` on the commits so far.
* ~Not triggered when pushing direct to `master`.~
    * Actually, it does.
    * Stuck at `The commit should not trigger a release`, probably because of the commit messages not matching the right format, something like `fix(pencil): stop graphite breaking when too much pressure applied`.
    * OK, got to `v0.0.5` automatically with the commit message done properly!
* Trying with all sorts of updated settings and token authentication.
* Trying `language: minimal`.
    * That didn't work but the next step up did: `language: generic`.

## Types and the relative version bumps

Based upon https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#type:

Type|Description|Bump (default)|Customised
-----|-----|-----|-----
`feat`|A new feature|0.1.0|
`fix`|A bug fix|0.0.1|
`docs`|Documentation only changes|0.0.0|0.0.1
`style`|Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)|0.0.0|0.0.1
`refactor`|A code change that neither fixes a bug nor adds a feature|0.0.0|0.0.1
`perf`|A code change that improves performance|0.0.1|
`test`|Adding missing or correcting existing tests|0.0.0|0.0.1
`chore`|Changes to the build process or auxiliary tools and libraries such as documentation generation|0.0.0|

* Adding `BREAKING CHANGE` to the footer of the extended description of the commit message will **always** trigger a `major` version change, no matter which type has been used.

The last two columns in table above were unnecessary and was because I had come across the following while researching, from the offshoot GitLab-based project:

https://www.npmjs.com/package/semantic-release-gitlab#major-version-zero:

> ### Major Version Zero
> 
> When the `major` version, the first number in `major.minor.patch`, of a semantic version string, is zero, `semantic-release-gitlab` will increment the version number following a different set of rules.
> 
> In this scenario, incrementing the `major` version will increment what is traditionally the `minor` number in the semantic version string, while incrementing the `minor` or `patch` version will increment the `patch` number in the semantic version string.
> 
> Note: To release a version `1.0.0` of your library you must create a `1.0.0` tag manually on your GitLab project.
> 
> When the `major` version is greater than zero, `semantic-release-gitlab` will switch back to it's default behavior of following semantic versioning. (Which uses the `inc` function provided by the `semver` package.)

## Plugins working

* `changelog` working (had to enable the `git` plugin as well).

## `FORMULA`

* Testing the plan to update the `version` automatically.

## Testing the types displayed in the release notes

Noticed that not all of the types are displayed (excpet for breaking chages).
Doing a series of commits here to push in one go, to see what comes through after the PR:

* `feat`
* `fix`
* `docs`
* `style`
* `refactor`
