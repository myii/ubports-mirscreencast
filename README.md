# ubports-mirscreencast

## Getting it working

Main purpose here is to get `semantic-release` working.

* Not yet but have just set tags up to `v0.0.4` on the commits so far.
* ~Not triggered when pushing direct to `master`.~
    * Actually, it does.
    * Stuck at `The commit should not trigger a release`, probably because of the commit messages not matching the right format, something like `fix(pencil): stop graphite breaking when too much pressure applied`.
    * OK, got to `v0.0.5` automatically with the commit message done properly!
* Trying with all sorts of updated settings and token authentication.
* Trying `language: minimal`.

## Types and the relative version bumps

Based upon https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#type:

Type|Description|v0.x.x|v1.x.x+
-----|-----|-----|-----
`feat`|A new feature|0.1.0|
`fix`|A bug fix|0.0.1|
`docs`|Documentation only changes|0.0.0|
`style`|Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)||
`refactor`|A code change that neither fixes a bug nor adds a feature||
`perf`|A code change that improves performance|0.0.1|
`test`|Adding missing or correcting existing tests||
`chore`|Changes to the build process or auxiliary tools and libraries such as documentation generation||
