# hubot-pr-fc

A Hubot script that list / merge the pull request. (for FaithCreates Inc.)

This script inspired by [hubot-list-pr][gh:bouzuya/hubot-list-pr] and [hubot-merge-pr][gh:bouzuya/hubot-merge-pr].

This is the forked repository. The original repository is [hubot-pr][gh:bouzuya/hubot-pr].

## Installation

    $ npm install 'https://github.com/bouzuya/hubot-pr-fc/archive/{VERSION}.tar.gz'

## Examples

    bouzuya> hubot help pr
      hubot> hubot pr [<user>/]<repo> - list pull requests
      hubot> hubot pr [<user>/]<repo> #<N> - merge a pull request
      hubot> hubot pr [<user>/]<repo> <issueNo> - merge a pull request

    (list)
    bouzuya> hubot pr hitoridokusho/hibot
      hubot> #1 pull request 1
               https://github.com/hitoridokusho/hibot/pull/1
             #2 pull request 2
               https://github.com/hitoridokusho/hibot/pull/2
    (merge)
    bouzuya> hubot pr hitoridokusho/hibot #2
      hubot> #2 pull request 2
             hitoridokusho:master <- bouzuya:add-hubot-merge-pr
             https://github.com/hitoridokusho/hibot/pull/2
             OK ? [yes/no]
    bouzuya> yes
      hubot> merged: hitoridokusho/hibot#2 : Pull Request successfully merged

    (merge)
    bouzuya> hubot pr hitoridokusho/hibot 3
      hubot> #3 ISSUE-3 issue title
             hitoridokusho:master <- bouzuya:add-hubot-merge-pr
             https://github.com/hitoridokusho/hibot/pull/3
             OK ? [yes/no]
    bouzuya> yes
      hubot> merged: hitoridokusho/hibot#3 : Pull Request successfully merged

    (HUBOT_PR_DEFAULT_USERNAME=hitoridokusho)
    (list)
    bouzuya> hubot pr hibot
      hubot> #1 pull request 1
                 https://github.com/hitoridokusho/hibot/pull/1
             #2 pull request 2
                 https://github.com/hitoridokusho/hibot/pull/2
    (merge)
    bouzuya> hubot pr hibot #2
      hubot> #2 pull request 2
             hitoridokusho:master <- bouzuya:add-hubot-merge-pr
             https://github.com/hitoridokusho/hibot/pull/2
             OK ? [yes/no]
    bouzuya> no
      hubot> canceled: hitoridokusho/hibot#2

See [`src/scripts/pr.coffee`](src/scripts/pr.coffee) for full documentation.

## License

MIT

## Development

### Run test

    $ npm test

### Run robot

    $ npm run robot


## Badges

[![Build Status][travis-badge]][travis]
[![Dependencies status][david-dm-badge]][david-dm]

[travis]: https://travis-ci.org/bouzuya/hubot-pr-fc
[travis-badge]: https://travis-ci.org/bouzuya/hubot-pr-fc.svg?branch=master
[david-dm]: https://david-dm.org/bouzuya/hubot-pr-fc
[david-dm-badge]: https://david-dm.org/bouzuya/hubot-pr-fc.png
[gh:bouzuya/hubot-pr]: https://github.com/bouzuya/hubot-pr
[gh:bouzuya/hubot-list-pr]: https://github.com/bouzuya/hubot-list-pr
[gh:bouzuya/hubot-merge-pr]: https://github.com/bouzuya/hubot-merge-pr
