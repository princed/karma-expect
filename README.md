karma-expect
============

> [Expect](https://github.com/LearnBoost/expect.js/) for [Karma](http://karma-runner.github.io)

Motivation
----------

You should use it only if you want run tests in **IE8 and lower**, otherwise consider [karma-chai](https://github.com/xdissent/karma-chai/), which provides more complete [Chai](http://chaijs.com/) BDD and TDD API.

Also this module is heavily inspired by [karma-chai](https://github.com/xdissent/karma-chai/).

Installation
------------

Install the module from npm:

```sh
$ npm install karma-expect --save-dev
```

Add `expect` to the `frameworks` key in your Karma configuration:

```js
module.exports = function(karma) {
  karma.set({

    # frameworks to use
    frameworks: ['mocha', 'expect']

    # ...
  });
};
```


Usage
-----

Expect.js assertions are available in the tests:

```js
describe('karma tests with expect', function() {
  it('should expose expect method', function() {
    expect('foo').to.not.equal('bar');
  });
});
```