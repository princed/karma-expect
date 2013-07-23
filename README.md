karma-expect
============

> [Expect](https://github.com/LearnBoost/expect.js/) for [Karma](http://karma-runner.github.io)

Motivation
----------

You should use it only if you want run tests in **IE8 and lower**, otherwise consider [karma-chai](https://github.com/xdissent/karma-chai/), which provides more complete [Chai](http://chaijs.com/) BDD and TDD API.

Also this module is heavily inspired by [karma-chai](https://github.com/xdissent/karma-chai/).

Requirements
------------

This module currently requires the `canary` version of Karma:

```sh
$ npm install 'karma@canary' --save-dev
```

Note that the Karma configuration file format has changed since `v0.8`. Use 
`karma init` to generate a fresh config.


Installation
------------

Install the module from npm:

```sh
$ npm install karma-expect --save-dev
```

Add `expect` to the `frameworks` key in your Karma configuration:

```coffee
module.exports = (karma) ->
  karma.configure

    # frameworks to use
    frameworks: ['mocha', 'expect']

    # ...
```


Usage
-----

Expect.js assertions are available in the tests:

```coffee
describe 'karma tests with expect', ->

  it 'should expose the Chai expect method', ->
    expect('foo').to.not.equal 'bar'
```