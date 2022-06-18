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
3. Run `npm test`
4. Create `app/sum.js` and `__tests__/sum.test.js`
  - update require path on line 1 to `require(../app/sum.js)`
5. Run `npm test`
