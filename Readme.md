[![Modus Create](./images/modus.logo.svg)](https://moduscreate.com)

# ModusCreateOrg GitHub Guidelines

This document outlines best practices for hosting public repositories under ModusCreateOrg GitHub organization.

  

Guidelines repository: [https://github.com/ModusCreateOrg/guidelines](https://github.com/ModusCreateOrg/guidelines)

## Content

- Repository should be completely **free of secrets** including API keys, passwords, tokens,.. 
- Commit log is to be free of offensive and unprofessional wording 
- All contributors adhere to Modus Create’s Code of Conduct 
- Do not publish .npmrc file even if empty 
- Supply with a [.gitignore](./.gitignore) file 
- Start with a private repository for new work that is not a fork of an existing public repository, and only switch it to public at the time of blog publication or other approved release 
- Consult the [Modus Labs process document](https://docs.google.com/document/d/1NoeJv9WSSDftQnKCR6oRjOQ3m_-zqCx7ygFwR8Wplx0/edit#heading=h.kczbw613h03g) and add the project to the [Modus Labs tracking spreadsheet](https://docs.google.com/spreadsheets/d/1-h2QCIzImOwn8iBnEZuCs2dOXnE2qLwSZblD09kL5bs/edit#gid=0) in order to start the review process for licensing and publication 

## Intellectual Property

- Modus should have a written consent to use any and all content and media used in the repo, whether accessed or saved as files. This includes Intellectual Property of any from, such as:
    - Content
    - Business logic 
    - Patents 
    - Images 
    - Videos 
    - Fonts 
    - Names 
    - Libraries 
    - Other technologies 

- Project adheres to licenses of projects used (e.g. license comments are not stripped out of production bundles) 
- Project follows legal guidelines set by the owners of IP used (e.g. attribution, references, links, etc.) 
- All rights granted should be written in the Readme explicitly or as a reference (to a file in the repo or outside of it, contract reference, or similar). 

## Readme.md

- Readme.md file should always be included 
- Readme.md file describes the project 
- Links to Modus Create web site and any relevant articles, instructions, or other Modus repos should be present 
- Credit everyone who helped with the project - code contributors, mentors, people you asked for a one-off help, promoters, etc 
- Follow the sample set in [Readme.sample.md](https://github.com/ModusCreateOrg/guidelines/blob/master/Readme.sample.md) 
  

## Package.json

- Add [SPDX](https://www.npmjs.com/package/spdx) compatible license 
- Make sure dependency versions start with ~. That means that major and minor versions are locked down, but patch version is highest available (`major.minor.{patch}` as in `15.6.2`) 
- You can ensure tilde ~ with `npm config set save-prefix='~'` 
- You can ensure a specific version of node by installing it with npm install `node@8.9.10`. This works well on older npm versions, too. 
- Also specify node version in engines property of `package.json`.  
```json
"engines": { "node": "8.9.10" }
```

This allows some automation software to detect the right container to boot up

- Include npm scripts for all useful actions, but be aware of platform differences (e.g. Windows) 
- Homepage is a moduscreate.com page for blog if possible 
- Repository is the github repo link 
- Use `package-lock.json` OR `yarn.lock` (not both) 
  

## License

- License should be provided in the Readme.md 
- [LICENSE](https://github.com/ModusCreateOrg/guidelines/blob/master/LICENSE) file should be in the repo root 
- Licensing to be defined with Principal Thought Leader, Modus Engineering Manager, and/or Legal department 
- Modus licenses Open Source Software under the [MIT License](https://opensource.org/licenses/MIT) unless the software community in question uniformly licenses it under other terms, such as  the Eclipse Public License for Eclipse plugins 
- Licensor is Modus Create 
- License should be listed in `package.json` and similar files 
  

## Author

- Any reference to author’s email should be signed with moduscreate.com email. E.g. `john.doe@moduscreate.com`

## GitHub repository recommendations

- [Protect master branch](https://help.github.com/articles/configuring-protected-branches/)
- [Require at least one review](https://help.github.com/articles/enabling-required-reviews-for-pull-requests/) to merge 

## Codebase quality recommendations

- Use standardized coding style and formatting. Enforce with tooling (e.g. eslint + prettier + husky + lint-staged) 
- Add unit tests. Explain how to add more tests. Show unit test coverage 
- Use CI ([CircleCI](https://circleci.com) is free and easy to set up, plus we run a Jenkins 2.0 server internally at [ci.moduscreate.com](https://ci.moduscreate.com) that is available for use. Automate tests and reporting back to the PR/repo 
- If you use environment variables, provide with a `.env.defaults` file