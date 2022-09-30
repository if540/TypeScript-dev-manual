# TypeScript-dev-manual
TypeScript 開發手冊

- [定義函式可有一個或多個參數類型(multiple arguments?)](https://stackoverflow.com/questions/64773876/interface-for-function-with-multiple-arguments)
  ```ts
  // T 限制多參數類型
  type OneOrMore<T> = { 0: T } & Array<T>;
  type MyFunction = (...args: OneOrMore<string>) => void;
  ```
  
  ```ts
  // 不限制參數類型
  type MyFunction = (...args: any) => void;
  ```
