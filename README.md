# Unit Testing Lab — Starter Code

Practice testing an Express API with Jest and Supertest, using a mocked module to control product data and simulate failures.

## Setup

Install Node.js and npm, then install the project dependencies:

```bash
npm install
```

## Project files

- `index.js`: Express application with a placeholder for the products route.
- `getProducts.js`: Async function that returns sample products.
- `index.test.js`: Starter test file with comments marking where to add your mock and tests.

## Exercise

1. Implement `GET /products` in `index.js`.
2. Call `getProducts()` and return its result as JSON with status `200`.
3. Handle errors with status `500` and a JSON response shaped like `{ "error": "error message" }`.
4. Mock `./getProducts` in `index.test.js` using Jest.
5. Test a successful response, an empty product list, and a rejected promise.

Use `mockResolvedValue()` for successful results and `mockRejectedValue()` to simulate errors. Reset mocks between tests so each test runs independently.

The app is exported as `{ app }`. Supertest can send requests directly to this app, so the tests do not need a fixed port or manual server lifecycle hooks.

## Run tests

```bash
npm test
```

Run tests in watch mode:

```bash
npm test -- --watch
```

Run tests and generate a coverage report:

```bash
npm test -- --coverage
```

Review the terminal summary for statement, branch, function, and line coverage. Open `coverage/lcov-report/index.html` in your browser for the detailed report. Use it to identify untested code paths and add tests for them.

The route and test cases are intentionally unfinished for this exercise.

## Git

Keep `node_modules/` and `.history/` out of version control. Install dependencies locally with `npm install`.
