
## Differences between interfaces and types in TypeScript.

### Type in TypeScript

The Type System in TypeScript describes the various data types supported by the language. It is divided into three major sections: Any Type, Built-In Type, and User-Defined Type. The Type System in TypeScript is responsible for ensuring the correctness of the data types before they are used in a program.

**Example:** In this example we defines two TypeScript types, User and UserEmail, and combines them using the intersection & operator. The gfg constant implements both types, storing and logging the combined object.

  ```bash
type User = {
  name: string;
  age: number;
};

type UserEmail = {
  email: string;
};

type combineUser = User & UserEmail;

const user: combineUser = {
  name: "Najmul",
  age: 25,
  email: "najmul.nh.shaon@gmail.com"
};

console.log(user);
  ```

### Interface in TypeScript
An Interface in TypeScript is a syntactical contract that entities must adhere to. It can only contain the declaration of properties, methods, and events, without any implementation. Interfaces define a standard structure that implementing classes must follow.

**Example:** In this example we demonstrates interface merging in TypeScript. Two User interfaces are combined automatically, allowing the user object to implement all properties (name, age, email) and log the merged result.

  ```bash
  // Creating a interface
interface User {
  name: string;
  age: number
}

interface User {
  email: string;
}

// Using the merged interface
const user: User = {
  name: "Najmul",
  age: 25,
  email: "najmul.nh.shaon@gmail.com"
};

console.log(user);
  ```


## The use of the keyof keyword in TypeScript.
The TypeScript keyof operator is used to get a union of all keys in an object type. It’s useful when you want to work with the property names of an object in a type-safe way, ensuring only valid keys are used.

We can use it to define generic functions that work with any object type, without knowing the specific keys of that type. It can also be used to create read-only versions of an interface or to extract specific keys from an interface.


### Syntax

``` bash
type KeysOfType = keyof ObjectType;
```

### Example

``` bash
interface Person {
      name: string;
      age: number;
      gender: string;
}
type PersonKeys = keyof Person;
```
---
