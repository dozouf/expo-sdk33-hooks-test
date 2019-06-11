# expo-sdk33-hooks-test

This is just a demonstration of an Expo SDK 33 project initialized with the bare-minimum template updated so Jest would run (rename `.babelrc` to `babel.config.js` and refactor appropriately) and modified to include a simple `useState()` hook in `App.js`. Upon running the basic render test supplied by the template, I receive the following error:

```
yarn run v1.15.2
$ jest
 FAIL  __tests__/App.js (11.431s)
  × renders correctly (37ms)

  ● renders correctly

    Invariant Violation: Hooks can only be called inside the body of a function component. (https://fb.me/react-invalid-hook-call)

      10 |
      11 | export default function App() {
    > 12 |   const [value, setValue] = useState(false);
         |                             ^
      13 |   return (
      14 |     <View style={styles.container}>
      15 |       <Text style={styles.welcome}>Welcome to React Native!</Text>

      at invariant (node_modules/react/cjs/react.development.js:88:15)
      at resolveDispatcher (node_modules/react/cjs/react.development.js:1436:28)
      at useState (node_modules/react/cjs/react.development.js:1461:20)
      at App (App.js:12:29)
      at mountIndeterminateComponent (node_modules/react-test-renderer/cjs/react-test-renderer.development.js:6889:13)
      at beginWork (node_modules/react-test-renderer/cjs/react-test-renderer.development.js:7389:16)
      at performUnitOfWork (node_modules/react-test-renderer/cjs/react-test-renderer.development.js:10149:12)
      at workLoop (node_modules/react-test-renderer/cjs/react-test-renderer.development.js:10181:24)
      at renderRoot (node_modules/react-test-renderer/cjs/react-test-renderer.development.js:10267:7)
      at performWorkOnRoot (node_modules/react-test-renderer/cjs/react-test-renderer.development.js:11135:7)

  console.error node_modules/react-test-renderer/cjs/react-test-renderer.development.js:8075
    The above error occurred in the <App> component:
        in App

    Consider adding an error boundary to your tree to customize error handling behavior.
    Visit https://fb.me/react-error-boundaries to learn more about error boundaries.

Test Suites: 1 failed, 1 total
Tests:       1 failed, 1 total
Snapshots:   0 total
Time:        15.033s
Ran all test suites.
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```

If you know what's wrong with the code I edited or that came with the bare-minimum template, please let me know.
