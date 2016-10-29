
https://www.codementor.io/nodejs/tutorial/unit-testing-nodejs-tdd-mocha-sinon
https://mochajs.org/


# installtion:
npm install mocha -g

# api
http://chaijs.com/api/bdd/

# testing
describe('name', function(){ ... })

it('some info text', function(err){ ... })

before(function(){ ... }) // run function before all tests in this block.
beforeEach(function(){ ... }) // run function before each tests in this block.

# except
except(...).satisfy(function(...){ return ... }) // user defined compare function
except(...).eql(...) // deep equal
except(...).throw(...) // check if throw an `err` or a `string` or a `regex`.
except(...).change(obj, value) // check if value changed before and after run test.

# pormise
except(<Promise>).eventually // handle promise.then
~~~js
const assert = require('assert');

it('should complete this test', function (done) {
  return new Promise(function (resolve) {
    assert.ok(true);
    resolve();
  })
    .then(done);
});
~~~


