# @bodrick/eslint-config

[![npm version](https://badge.fury.io/js/@bodrick/eslint-config.svg)](http://badge.fury.io/js/@bodrick/eslint-config)

This package provides a fork of Airbnb's base JS .eslintrc modified for use with TypeScript, vscode, and prettier.

## Usage

We export multiple ESLint configurations for your usage.

### using @bodrick/eslint-config

Our default export contains all of our ESLint rules, including ECMAScript 6+. It requires `eslint` and `eslint-plugin-import`.

1. Install the correct versions of each package, which are listed by the command:

```sh
npm info "@bodrick/eslint-config@latest" peerDependencies
```

If using **npm 5+**, use this shortcut

```sh
npx install-peerdeps --dev @bodrick/eslint-config
```

If using **yarn**, you can also use the shortcut described above if you have npm 5+ installed on your machine, as the command will detect that you are using yarn and will act accordingly.
Otherwise, run `npm info "@bodrick/eslint-config@latest" peerDependencies` to list the peer dependencies and versions, then run `yarn add --dev <dependency>@<version>` for each listed peer dependency.

If using **npm < 5**, Linux/OSX users can run

```sh
(
  export PKG=@bodrick/eslint-config;
  npm info "$PKG@latest" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG@latest"
)
```

Which produces and runs a command like:

```sh
  npm install --save-dev @bodrick/eslint-config eslint@^#.#.# eslint-plugin-import@^#.#.#
```

If using **npm < 5**, Windows users can either install all the peer dependencies manually, or use the [install-peerdeps](https://github.com/nathanhleung/install-peerdeps) cli tool.

```sh
npm install -g install-peerdeps
install-peerdeps --dev @bodrick/eslint-config
```

The cli will produce and run a command like:

```sh
npm install --save-dev @bodrick/eslint-config eslint@^#.#.# eslint-plugin-import@^#.#.#
```

2. Add `"extends": "@bodrick/eslint-config"` to your .eslintrc.

### @bodrick/eslint-config/legacy

Lints ES5 and below. Requires `eslint` and `eslint-plugin-import`.

1. Install the correct versions of each package, which are listed by the command:

```sh
npm info "@bodrick/eslint-config@latest" peerDependencies
```

Linux/OSX users can run

```sh
(
  export PKG=@bodrick/eslint-config;
  npm info "$PKG" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG"
)
```

Which produces and runs a command like:

```sh
npm install --save-dev @bodrick/eslint-config eslint@^3.0.1 eslint-plugin-import@^1.10.3
```

2. Add `"extends": "@bodrick/eslint-config/legacy"` to your .eslintrc

See [Airbnb's overarching ESLint config](https://npmjs.com/eslint-config-airbnb), [Airbnb's JavaScript style guide](https://github.com/airbnb/javascript), and the [ESLint config docs](https://eslint.org/docs/user-guide/configuring#extending-configuration-files) for more information.

## Improving this config

Consider adding test cases if you're making complicated rules changes, like anything involving regexes. Perhaps in a distant future, we could use literate programming to structure our README as test cases for our .eslintrc?

You can run tests with `npm test`.

You can make sure this module lints with itself using `npm run lint`.
