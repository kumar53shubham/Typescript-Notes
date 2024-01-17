# Functions in Typescript

Set of statement writtern for doing a specific task is called functions.

1- Functions has name

2- Functions has block of code(statements)

3- Functions can take parameters

4- Functions can return values

> > In typescript type of parameters and return type is most important thing.

**Syntax**

```js
function nameOfFunction(a:type,b:type...) : returnType
{

//statements

}

```

example

```js
//function creation

function ramu(rs: number, name: string): number {
  console.log("hello sir g , what can i do for you?");
  return 4;
}

// function calling

let ng = ramu(12, "left");
console.log(ng);

ramu(15, "center");
ramu(450, "right");
```

## Type of Function

(parameters) => return type

(a: number, b: number) => number

## Optional Parameters

- Required Parameters- must
- Optional Parameters- optional

```js
function myFun(a: string, b: string, c?: string) {}

function sumOfThree(a: number, b: number, c?: number, d?: number): number {
  console.log("Adding three numbers");
  if (c !== undefined) {
    return a + b + c;
  }
  return a + b;
}
```

## Default Parameters

we can use default values of paramertes in functions

```js
function sumOfThree(a: number = 1, b: number, c: number = 1): number {
  console.log("Adding three numbers");
  return a + b + c;
}
```

## Rest Parameters

This parameter accept multiple value as array.

> > It must be last parameter

```js
function sumAtLeastTwo(a: number, b: number, ...rest: number[]): number {
  let sum = a + b;

  rest.forEach((n) => {
    sum = sum + n;
  });
  console.log("sum is ", sum);

  return sum;
}

sumAtLeastTwo(12, 12);
sumAtLeastTwo(12, 12, 23, 12, 35, 34, 46, 57);
sumAtLeastTwo(1, 2, 3);
```
