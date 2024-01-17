# Typescript Types

In typescript we create variables with types. So that we can assign same type of values to that variables.

```ts
let x: number = 34;
```

## Value

Value is a thing that we assign to variable.

```ts
let y: number = 3535;
```

**y** : variable

**number** : type of variable

**=** : assignment operator

**3535** : value that is assigned to variable

## Types in TypeScript

- string - represent text data

- number - represent number

- boolean - represnet true and false
- null- only one value : **null**, intentional absense of value.
  null is falsy value

- undefined - one value **undefined** . default value of uninitialized variable. undefined is falsy value

- Any - skip the type checking

> Avoid using Any type in you code.

- Array - ordered list of data

  ```js
  //syntax
  let arrayName: type[];

  //example
  let numbers: number[] = [12, 2, 4, 46, 57, 678];
  ```

- Object Type- represent multiple properties.

```js

{
    firstProperty1:'value',
    secondProperty2:'value
}

```

- Union Type

```js
let myvar: string | number = "my value";

let names: (string | number)[] = [];
```

---

- Void - represent constant value that may be undefined or null

  void is used when function does not have return statement.

- never : represent value that will never occur,
  used when function never return value

- unknown

  - not kown
  - type safe counterpart of any

---

- Tuple

  - number of elements are fixed
  - type of elements are known and same.

```js
let skill: [string, number] = ["programming", 400];
console.log(skill);
```

---

- Enum

  Group of named constant values.

```js
enum OrderStatus {
  PENDING,
  DELIVERED,
  DISPATCH,
}



let order: { title: string; price: number; status: OrderStatus; date: Date };

order = {
  title: "Samsung TV1234",
  price: 33000.56,
  status: OrderStatus.PENDING,
  date: new Date(),
};

console.log(order);
order.status = OrderStatus.DISPATCH;
console.log(order);

console.log(OrderStatus);

```

- Type Alias

  creating Temp name of type

  ```js
  //exmaple
  type xyz = string;

  type aphaNum = string | number;

  type Order = {
    title: string,
    price: number,
    status: string,
  };
  ```

- String Literal Types

```js
let userName: "shubham" | "himanshu" | "harsh";
```
