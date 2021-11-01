---
title: "Testing"
---

[source](https://www.youtube.com/watch?v=FxSsnHeWQBY)

## Testing

- know if your code works
- save time, better code, reduces fear of changing code, when it's covered by tests
- interactive testing - not repeatable
- repeatable, expected results, check the results
- `assert` - true continues, false raises exception
- each test to run independently, when one fails, another one continues,not stops
- good test
  - automated
  - fast
  - reliable - to believe them
  - informative
  - focused - do the least the possible, when it covers code, we should know right away what part of code is broken
- `unittest` - library in python
- test isolation - every test its new test object and is independent of each other
- helper methods by unittest
    - assertEqual() - writes all values in assert
- can make more objects, where parent object can have helper custom assert methods
- `.` - passed, `F` - Assertion failure, `E` - other exception
- `with assertRaises(exception)`
- `setUp(), tearDown()` - invoked before/after each test
- mocks - components depends on each other, replace untested components with mocks, some mockups that replaces real code in testing
- fake implementation of components
- faking libraries (e.g. api calls)
- mock objects - automatic chameleons, can do anything what is said to