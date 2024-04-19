# eslint-config-wikimedia-typescript

ESLint config for TypeScript following [Wikimedia code conventions](https://www.npmjs.com/package/eslint-config-wikimedia) - the idea is to make this repository here obsolete in the medium term and upstream these rules.

## Release instructions

To make a new release:

1. Bump the version number in a pull request.
   (Edit `package.json` manually, then run `npm install` to update the version number in `package-lock.json`.)
   The usual commit message is “Bump version to <var>1.2.3</var>”.
   [Example pull request](https://github.com/wmde/eslint-config-wikimedia-typescript/pull/48).

1. Get that pull request reviewed and merged.

1. Tag the merge commit locally. A “lightweight” tag is usually enough:
   `git pull`, then <code>git tag v<var>1.2.3</var></code>.

1. Push the tag. <code>git push origin v<var>1.2.3</var></code>

1. Turn it into a proper release on GitHub:
   [draft a new release](https://github.com/wmde/eslint-config-wikimedia-typescript/releases/new).
   [Example release](https://github.com/wmde/eslint-config-wikimedia-typescript/releases/tag/v0.2.9).

1. Once the GitHub release is published,
   it should be automatically published to NPM via GitHub Actions.

1. Submit a Gerrit change to `labs/libraryupgrader/config`
   to update the version of the package in `releases.json`.
   ([Source](https://gerrit.wikimedia.org/r/c/labs/libraryupgrader/config/+/1021379/); replace with an example once available.)
