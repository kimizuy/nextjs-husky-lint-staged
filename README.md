# Next.js + husky + lint-staged example

This example based [with-eslint](https://github.com/vercel/next.js/tree/canary/examples/with-eslint) and using `next@canary` version.

## How to use

Install it and run:

```
yarn
yarn dev
```

## You can also see how `yarn lint --file` works.

Change `pages/index.js` as follows:

```
const Home = () => (
  <div>
    <script src="https://fake-script.com" />
    {/* ↓ change this line to "Test" */}
    <p>Test</p>
  </div>
);

export default Home;
```

Commit file changes:

 ```
 git add . && git commit -m "test"
 ```

Then, you can get this error (It's OK!):

```✖ lint --max-warnings=0 --file failed without output (ENOENT).```






