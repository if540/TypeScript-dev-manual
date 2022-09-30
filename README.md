# TypeScript-dev-manual
TypeScript 開發手冊

- [定義函式可有一個或多個參數類型(multiple arguments?)](https://stackoverflow.com/questions/64773876/interface-for-function-with-multiple-arguments)
  ```ts
  type OneOrMore<T> = { 0: T } & Array<T>;
  type MyFunction = (...args: OneOrMore<string>) => void;
  ```
