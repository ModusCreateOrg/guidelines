# ModusCreateOrg GitHub guidelines

This document outlines best practices for hosting public repositories under ModusCreateOrg GitHub organization.

## Content

* Repository should be completely free of secrets including API keys, passwords, tokens,..

* Commit log is to be free of offensive and unprofessional wording

* All contributors adhere to Modus Create's Code of Conduct

* Do not publish `.npmrc` file even if empty

* Supply with a `.gitignore` file

## Intellectual Property

* Modus should have a written consent to use any and all content and media used in the repo, whether accessed or saved as files. This includes:

* Ideas

* Patents

* Images

* Videos

* Fonts

* Names

* Libraries

* Other technologies

* Project adheres to licenses of projects used (e.g. license comments are not stripped out of production bundles)

* Project follows legal guidelines set by the owners of IP used (e.g. attribution, references, links, etc.)

## Readme.md

* `Readme.md` file should always be included

* `Readme.md` file describes the project

* Links to Modus Create web site and any relevant articles, instructions, or other Modus repos should be present

* Credit everyone who helped with the project - code contributors, mentors, people you asked for a one-off help, promoters, etc

* Follow the sample set in [Readme.sample.md](./Readme.sample.md)

## Package.json

* Add [SPDX](https://www.npmjs.com/package/spdx) compatible license

* Make sure dependency versions start with `~`. That means that major and minor versions are locked down, but patch version is highest available (`major.minor.{patch}` as `in 15.6.2`)

* You can ensure tilde ~ with `npm config set save-prefix='~'`

* You can ensure a specific version of node by installing it with npm install `node@8.9.10`.This works well on older npm versions, too.

* Also specify node version in engines property of package.json.

`engines: { node: 8.9.10 }`

This allows some automation software to detect the right container too boot up

* Include npm scripts for all useful actions, but be aware of platform differences (e.g. Windows)

* Homepage is a moduscreate.com page for blog if possible

* Repository is the github repo link

* Use `package-lock.json` OR `yarn.lock` (not both)

## GitHub Repo settings

* Protect master branch

* Require at least one review to merge

## Codebase quality recommendations

* Use standardized coding style and formatting. Enforce with tooling (e.g. eslint + prettier + husky + lint-staged)

* Add unit test. Explain how to add more tests. Show unit test coverage

* Use CI (CircleCI is free and easy to set up). Automate tests and reporting back to the PR/repo

* If you use environment variables, provide with a `.env.defaults` file

## License

* License should be provided in the Readme.md

* LICENSE file should be in the repo root

* Licensing to be defined with Principal Thought Leader, Modus Engineering Manager, and/or Legal department

* Modus licenses Open Source Software under the MIT License

* Licensor is Modus Create

* License should be listen in package.json and similar files

## Author

* Any reference to author's email should be signed with moduscreate.com email. E.g. `john.doe@moduscreate.com`
