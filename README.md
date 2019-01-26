# GrumPHP Tasks
[![All Contributors](https://img.shields.io/badge/all_contributors-2-orange.svg?style=flat-square)](#contributors)

Requires NPM packages too!

Example package.json
```json
{
  "dependencies": {
    "eslint": "^4.1.1",
    "eslint-config-standard": "^10.2.1",
    "eslint-plugin-promise": "^3.5.0",
    "eslint-plugin-standard": "^3.0.1"
  }
}
```



Example `grumphp.yml`

```yaml
parameters:
  git_dir: .
  bin_dir: vendor/bin
  tasks:
    eslint: ~
services:
  task.eslint:
    class: Stickee\GrumPHP\ESLint
    arguments:
      - '@config'
      - '@process_builder'
      - '@formatter.raw_process'
    tags:
      - {name: grumphp.task, config: eslint}

```

## Installation

```
composer require stickee/grumphp-tasks
```
and then either
```
yarn add eslint eslint-config-standard eslint-plugin-promise eslint-plugin-standard
```

or 

```
npm install --save eslint eslint-config-standard eslint-plugin-promise eslint-plugin-standard
```

## Contributors

Thanks goes to these wonderful people ([emoji key](https://github.com/all-contributors/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
| [<img src="https://avatars3.githubusercontent.com/u/570639?v=4" width="100px;" alt="Martin Meredith"/><br /><sub><b>Martin Meredith</b></sub>](https://www.sourceguru.net)<br />[💻](https://github.com/Mezzle/grumphp-tasks/commits?author=mezzle "Code") [👀](#review-mezzle "Reviewed Pull Requests") [🤔](#ideas-mezzle "Ideas, Planning, & Feedback") [📖](https://github.com/Mezzle/grumphp-tasks/commits?author=mezzle "Documentation") | [<img src="https://avatars2.githubusercontent.com/u/401928?v=4" width="100px;" alt="Chris Ivens"/><br /><sub><b>Chris Ivens</b></sub>](http://www.joltbox.co.uk)<br />[💻](https://github.com/Mezzle/grumphp-tasks/commits?author=chrisivens "Code") [👀](#review-chrisivens "Reviewed Pull Requests") [🤔](#ideas-chrisivens "Ideas, Planning, & Feedback") |
| :---: | :---: |
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!