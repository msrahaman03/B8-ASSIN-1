what is type-narrowing
Type Narrowing in TypeScript means reducing a variable's broad type into a more specific type after checking its actual value.

In simple words, TypeScript first knows a variable might have multiple types. After checking the type, TypeScript understands exactly which type you are working with.

Let's understand with examples.

1. Basic Example: typeof
function printValue(value: string | number) {
    if (typeof value === "string") {
        console.log(value.toUpperCase());
    } else {
        console.log(value.toFixed(2));
    }
}

printValue("saidur"); // SAIDUR
printValue(100);      // 100.00

Explanation:

Initially, value can be string or number.

Inside the if block, TypeScript knows value is a string.

Inside the else block, TypeScript knows value is a number.

This process is called Type Narrowing.

2. Common Type Narrowing Techniques
A. typeof Operator
Used for checking primitive types.

function checkValue(value: string | number) {
    if (typeof value === "string") {
        return value.toUpperCase();
    }

    return value * 2;
}

B. instanceof Operator
Used to check whether an object belongs to a particular class.

function printDate(value: Date | string) {
    if (value instanceof Date) {
        console.log(value.getFullYear());
    } else {
        console.log(value.toUpperCase());
    }
}

C. in Operator
Used to check whether an object contains a particular property.

type Student = {
    name: string;
    grade: number;
};

type Teacher = {
    name: string;
    subject: string;
};

function printInfo(person: Student | Teacher) {
    if ("grade" in person) {
        console.log(person.grade);
    } else {
        console.log(person.subject);
    }
