Follow steps from https://jestjs.io/docs/getting-started
1. Install Jest
```bash
npm install jest
```
2. Configure `package.json` to support `npm test`:
```json
"scripts": {
  "test": "jest"
}
```
3. Run `npm test`. There should be a warning that there are no tests.
4. Create `app/sum.js` and `__tests__/sum.test.js`
  - Copy from https://jestjs.io/docs/getting-started
  - Update require path on line 1 to `require(''../app/sum.js')`
5. Run `npm test`. The test should pass.
6. Copy the below edge case test to `__tests__/sum.test.js`
```js
test('throws an error for 1 + hello', () => {
  expect(() => sum(1, 'hello'))).toThrowError('hello is not a number!');
});

test('throws an error for hello + 1', () => {
  expect(() => sum('hello', 1))).toThrowError('hello is not a number!');
});
```
  - Notice the extra function inside of expect. This is necessary to test exceptions.
7. Run `npm test`. The new tests should fail.
