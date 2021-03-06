# haeley-template

```
npm i -D @haeley/template
```

*@haeley/template* is a template repository, developed and intended for [`haeley`](https://github.com/halb3/haeley) real-time rendering framework.

[![npm Version](https://img.shields.io/npm/v/@haeley/template.svg)](https://www.npmjs.com/package/@haeley/template)
[![GitHub Action](https://img.shields.io/github/workflow/status/halb3/template/test.svg)](https://github.com/halb3/template/actions)
[![Coveralls](https://img.shields.io/coveralls/github/halb3/template.svg?logo=coveralls)](https://coveralls.io/github/halb3/template/)
[![CodeFactor](https://img.shields.io/codefactor/grade/github/halb3/template/main.svg?logo=codefactor)](https://www.codefactor.io/repository/github/halb3/template/)
![License](https://img.shields.io/github/license/halb3/template.svg?logo=coveralls)


# Steps to Create a new Repository from this Template

1. Clone or copy this repository.
2. If coveralls should be integrated (required for haeley projects), a `COVERALLS_REPO_TOKEN` is required in order to have the nyc coverage results be reported to coverall during the gh test action (`.github/workflows/test.yml`)
3. Replace all occurences of `template` or `haeley-template` with the new module name.
4. Since git repository information is used for selfreporting the modules version (`about.ts`), at least one commit is required in order to have various scripts (e.g., `build` oder `build:dev`) work.
5. Note: we use gh setup-node@v2 action which supports caching for npm. For this to work, the `package-lock.json` must be part of the repository. The hash of this file is used as a cache reference.
6. If everything is setup, try re-run the last action (which might fail the first time, if the coveralls secret was added after commiting the gh action).

optional: Integration of codefactor: just add the repository... and use the following 'ignore pattern'.:

Settings -> Ignore Files -> Exclude Pattern:
```
vite.config.ts
.github/**
tests/**
```


# Publishing with NPM

1. Log in to your npm account (check with `npm whoami`) using `npm login`
2. Initialize the haeley scope (manually by configuring the package, or using `npm init --scope=haeley`)
3. Commit everything, merge everything, make sure everything works!
4. Decide on required semantic! version change: `npm version patch`, `npm version minor`, or `npm version major`
5. Publish using `npm publish --access public`
