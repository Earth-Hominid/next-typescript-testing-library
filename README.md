# Testing

```sh
yarn add @testing-library/react @types/jest babel-jest @testing-library/ \
jest-dom @testing-library/user-event @testing-library/dom -D
```

`touch tsconfig.json`
`touch .babelrc`

- for babel

```json
{
  "presets": ["next/babel"]
}
```

// jest.config.js

```js
module.exports = {
  setupFilesAfterEnv: ['<rootDir>/jest.setup.ts'],
  testPathIgnorePatterns: ['<rootDir>/.next/', '<rootDir>/node_modules/'],
  moduleNameMapper: {
    '\\.(scss|sass|css)$': 'identity-obj-proxy',
  },
  moduleDirectories: ['node_modules', 'src'],
};
```

// jest.setup.ts

```js
import '@testing-library/jest-dom';
```

For CSS,
install identity-obj-proxy

```sh
yarn add identity-obj-proxy -D
```
