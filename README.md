# JavaScript Testing Starter

A practice project for unit testing plain JavaScript with Vitest. `src/` holds small functions written as lessons and exercises (assertions, positive/negative and boundary testing, async code, setup/teardown, mocking), and `tests/` holds the tests written so far.

## Tech stack

- JavaScript (ES modules)
- Vitest (test runner)
- Vite
- `delay` (simulates slow I/O in the fake service modules)

## What the code does

- `src/intro.js` - `max(a, b)`, `fizzBuzz(n)` and `factorial(n)`
- `src/core.js` - functions for later lessons: coupons and discount calculation, user input and username validation, price range and driving-age checks, an async `fetchData`, a `Stack` class, `createProduct`, `isStrongPassword` and `getDiscount`
- `src/mocking.js` - functions that depend on external services, intended for mocking practice: currency conversion, shipping info, page-view tracking, order submission, sign-up and login emails, and time-based checks (`isOnline`)
- `src/libs/` - fake analytics, currency, email, payment, security and shipping services. They log to the console, return random values or wait 3 seconds, which is why tests should mock them

## Tests

`tests/intro.test.js` covers `src/intro.js`:

- `max` - first argument larger, second argument larger, and equal arguments
- `fizzBuzz` - multiples of 3 and 5, of 3 only, of 5 only, and other numbers returned as strings
- `factorial` - a normal case (`3` gives `6`) and the edge cases `1` and `0` (both give `1`)

`src/core.js` and `src/mocking.js` do not have tests yet.

## Getting started

```bash
npm install
npm test           # run Vitest in watch mode
```

Vitest is listed in `package-lock.json` but not in `package.json`. If `npm test` cannot find it, install it with `npm install -D vitest`.

Other scripts: `npm run dev`, `npm run build` and `npm run preview` run Vite.

No environment variables are required.

## Project structure

```
src/
  intro.js      max, fizzBuzz, factorial
  core.js       Functions for assertion, boundary, async and setup/teardown lessons
  mocking.js    Functions that call the services in libs/
  libs/         Fake external services
tests/
  intro.test.js
```
