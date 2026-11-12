In TypeScript, both type aliases and interface are used to define the structure of data. They look similar, but they have some important differences.

Let's understand them with simple examples.
1. Interface in TypeScript
An interface defines the structure of an object. It describes what properties and types an object should have.

Example:
interface Student {
    name: string;
    age: number;
    isActive: boolean;
}

const student: Student = {
    name: "Saidur",
    age: 20,
    isActive: true
};


Here:
- Student is an interface.
- name must be a string.
- age must be a number.
- isActive must be a boolean.
2. Type Alias in TypeScript
A type alias gives a name to any type. It can define objects, primitive types, unions, tuples, and more.

Example 1: Object type
type Student = {
    name: string;
    age: number;
    isActive: boolean;
};

const student: Student = {
    name: "Saidur",
    age: 20,
    isActive: true
};


Example 2: Primitive type
type UserName = string;

let name: UserName = "Saidur";