# Testing

## Why test?

- Check it will work with unexpected user inputs
- Check for "edge" cases
- Check the code works later on when a small part might be changed

## TDD Test Driven Development

- Instead of making funcions and then testing them, do it the other way round:

**Decide on the criteria of the test that your code needs to pass, and then create the function in order to pass the test, with the minimum amount of code possible**

## How to?

1. Get QUnit going as a good test environment.
2. Use QUnit Documentation as a good frame for the html, not forgetting to make the tests.js file as well.

  ```html
  <!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>QUnit Example</title>
  <link rel="stylesheet" href="https://code.jquery.com/qunit/qunit-2.1.1.css">
</head>
<body>
  <div id="qunit"></div>
  <div id="qunit-fixture"></div>
  <script src="https://code.jquery.com/qunit/qunit-2.1.1.js"></script>
  <script src="tests.js"></script>
</body>
</html>
```

3. Within the tests.js file have the example code from QUnit to test the tests are working properly:

  ```js
QUnit.test( "hello test", function( assert ) {
  assert.ok( 1 == "1", "Passed!" );
});
```

4. QUnit tests:

  Assert.ok, as seen above, takes 2 arguments, the first one is just a simple boolean test that passes if true (or truthy) and the second one just a message.

  ```js
  assert.equal(functionIAmTesting(),"Known answer","Output Message")
```

  Asssert.equal takes 3 arguments, the function you are testing, the solution and a message to show when the test runs. This is pretty solid/most used.

  ```js
  assert.deepEqual(functionIAmTesting(),"Known answer","Output Message")
```

  deepEqual does much th same, but will ensure objects are compared properly.

5. More information and QUnit documentation can be found [here](http://api.qunitjs.com/).
