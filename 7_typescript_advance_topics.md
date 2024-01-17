# TypeScript Generics

Generics concept help us to write generalized form of functions, Classes and Interfaces.

```ts
// Generic Functions
function getInfo<T>(numbers: T[]) {
  console.log(numbers[1]);
}

function merge<U, V>(ob1: U, ob2: V) {
  console.log({
    ...ob1,
    ...ob2,
  });
}

getInfo<string>(["one", "two"]);
getInfo<number>([1, 2]);
getInfo<boolean>([true, false]);
getInfo<MyType>([{ name: "test" }, { name: "test" }]);
merge<MyType, MyType1>({ name: "test" }, { email: "test@gmail.com" });
```

## Generatic Classes:

```ts
class Stack<T> {
  items: T[] = [];
  size: number;

  constructor(size: number) {
    this.size = size;
  }

  isEmpty() {
    if (this.items.length === 0) return true;

    return false;
  }

  isFull() {
    if (this.items.length === this.size) return true;
    return false;
  }

  insert(element: T) {
    if (!this.isFull()) {
      this.items.push(element);
    } else {
      console.log("Stack is full");
    }
  }

  remove(): T | undefined {
    if (!this.isEmpty()) {
      return this.items.pop();
    } else {
      throw new Error("Stack is empty");
    }
  }

  display() {
    this.items.forEach((element) => {
      console.log(element);
    });
  }
}

// let stack: Stack<number> = new Stack<number>(4);
// stack.insert(23);
// stack.insert(12);
// stack.insert(324);
// stack.display();
// console.log("removing");
// console.log(stack.remove());
// stack.display();
let stack: Stack<string> = new Stack(2);
stack.insert("harsh");
stack.insert("shubham");
stack.display();
```

## Ts Generic constraints

```ts
class Test<T extends Type> {}
```

---

# TS Modules

TypeScript module allows it to contain both the declaration and its code.

With the help of module we can make local scope of variables, functions , classes etc.

we can create module by exporting thing.

file.ts

```ts
export class Test {}
```

file1.ts

```ts
import { Test } from "file.ts";

//use test
```
