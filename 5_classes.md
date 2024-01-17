# Class

Typescript offer full support of class and object introduced in ES6.

- Template for object.
- Define fields
- Define constructor
- Define methods

```ts
class Car {
  //code
  //properties- data-- variables
  // constructor-- help object initialize
  //methods--> task --> functinality
}
```

## Creating object

we can create multiple object from single class and use that class.

```ts
let ob: Car = new Car();
```

## Constructor

Special function that is called when we create object to initialize fields.

```ts
class Car {
  constructor() {
    //initilize fields
  }
}
```

### Constrcutor loading

when we defined more than one constructor having different argument then it is constructor overloading.

```ts
class Car {
  constructor() {
    //initilize fields
  }

  constructor(x: number) {
    //initilize fields
  }
  constructor(x: number, y: number) {
    //initilize fields
  }
}
```

## Method

Functions inside class is Methods.
Methods are the behaviour associated with object.

```ts
class Car {
  //method
  start() {
    console.log("Car is starting");
  }
}
```

## Getter and Setters

When we don't want our class fields can be changed from outside or some validation happen while changing fields then we make our fields **private** and need setters and getters to set and get the values.

```ts
class Car {
  private _color;
  constructor(color: string) {
    this._color = color;
  }

  //getter
  get color() {
    //some logic
    return this._color;
  }

  //setter
  set color(color: string) {
    //some logic
    this._color = color;
  }
}
```

1. if get exists but not set then property is autmatically is **readonly**

2. getter and setter must have same member visiblity.

3. if setter parameter type is not specified then it is refered from return type of getter.

## Access Modifier

Modifiers are the keywords which can change the accessbility of properties and methods of class.

- Private
- Protected
- Public

## private

Limits the visiblity to same class.

Private memebers are limited to same class.

## public

No Limits

Can be access from all locations.

## protected

Limited to same class and its subclass.

protected memeber are accessible within same class and its sub-class.

# Readonly modifier

It marks properties to be immutable.

once value assigned can **not** be changes.

we can use readonly at two places

- with class fields
- inside constructor parameters.

---

# Inheritance

when class takes properties and methods of another class then its called **Inheritance**.

class that takes properties and methods is called **child class**.

class that provide the properties and methods is called **parent class**.

> > Inheritance allow reuse of the code.

Example

```ts
// here A is taking properties and method of B
class A extends B {}
```

## super

when is need to call parent class constructor from child class constructor then we use super

```ts
class A {
  constructor() {}
}

class B extends A {
  constructor() {
    // call to parent class constructor
    super();
  }
}
```

## Method overriding

When child class redfined method body of parent class then it is method overriding.

```ts
class A {
  describe() {
    //body
  }
}

class A extends B {
  describe() {
    //new body of describe
  }
}
```

# Static Properties

when be declare any field in class then it is intance field and objects get the copy of that field .

but when be declare static field then that field is shared amongs all the objects of the class .

## Static methods

Similar to static properties methods are share amongs objects.

# Abstract Class

Abstract is basically incomplete class.

If we want to define common behaviour of classes then be use abstract class.

Object of abstract class can not be created.

Abstract method must be implemented by derived class.

> > abstract class has atleast one abstract methods

```ts
abstract class Car {
  //common functionality
  //abstract
}
```

To use abstract class you need to inherit and provide the implementation of class.

# Interfaces

- Interface is a structure that defines the contract in your application

- Classes that defined from interface must follow the structure provided by Interface.

- Typescript uses interface for type checking- **Duck** typing

Example1

```ts
interface Employee {
  empId: string;
  empNaem: string;
  getSalary: (number) => string;
}
```

Example2

```ts
interface Coordinate {
  x: number;
  y: number;
  difference: () => number;
}
```

UseCase:

Find the distance between two point.

Point has two coordinate x and y

```
d = sqrt((x2-x1)^2+(y2-y1)^2)

```
