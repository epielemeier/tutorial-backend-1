# Automated Testing

---

## What is a test?

Acceptance Criteria + Application = Pass or Fail

---

## Why do we test?

- To verify the software does what we want it to do
  - Meets business requirements
  - Responds gracefully when something goes wrong
- Nothing has broken since the last time we tested

---

## Ways to test

### Manual test

### Automated test

---

## Why automated tests?

- Fast
- Consistently repeatable
- Protects working code
- Retains problem domain knowledge

#### "A good software engineer writes good code. A great software engineer writes tests for their code."

---

## "But we don't have time to write tests!"

- Setting expectations
- It will break. When will you find out?
- Fire prevention vs fire fighting
- Technical debt

---

## "Tests are hard, and I'm still not convinced"

- https://phase2online.com/2021/04/06/using-automated-testing-to-confidently-release-software/
- https://phase2online.com/2022/06/13/how-to-write-a-valuable-test-suite/

---

## Kinds of tests

### Unit test

### Integration test
##### End-to-end test

---

## When do we test?

- Unit tests: frequently (CI/CD)
- Integration tests: sometimes less frequently

---

## Github Actions

```yaml
name: RUN UNIT TESTS

on:
    pull_request:
        branches:
            - master
            - dev

jobs:
    jest-unit-test:
    # from https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-nodejs
        runs-on: ubuntu-latest
        steps:
          - uses: actions/checkout@v2
          - uses: actions/setup-node@v3
            with:
              node-version: 16.x
          - run: npm install
          - run: npm run build --if-present
          - run: npm test
```

---

## Definitions
- Test-Driven Development (TDD)
- Behavior-Driven Development (BDD): Given... When... Then...
- Mock (noun)
- Stub (verb)

---

# Demo
- https://github.com/dbnorth/tutorial-backend-1/tree/jest-unit-tests
- https://github.com/dbnorth/tutorial-frontend-1/tree/cypress-integration-tests
- https://github.com/epielemeier/tutorial-backend-1/pull/1
---

Presented via https://play.presenta.cc/view/Of7EOSLCZYe7h
