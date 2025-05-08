# Interface and Type Alias

### Both interface and type are powerful tools in TypeScript. In most cases, they can be used interchangeably for defining object shapes. type alias can define unions, intersections, tuples, and primitives. and interface can not do this. It is only for object shapes.
---

```javascript
// Using interface
interface Person {
  name: string;
  age: number;
}

// Using type alias
type PersonType = {
  name: string;
  age: number;
};

// Using tuples
type ActiveMan = 'work' | 'rest' | 'success';

type ID = string | number;

```

# Union and intersection

### Union type allows multiple variable types and Intersection type combines multiple types into one.

## Union Types

```javascript
type Status = 'success' | 'error' | 'loading';

function showStatus(status: Status) {
  if (status === 'success') {
    console.log('Operation was successful!');
  } else if (status === 'error') {
    console.log('Something went wrong.');
  } else {
    console.log('Loading...');
  }
}

showStatus('success');
```

## Intersection Types

```javascript
type Man = {
  name: string;
  age: number;
};

type Employee = {
  company: string;
  position: string;
};

type EmployeeProfile = Man & Employee;

const profile: EmployeeProfile = {
  name: 'Alice',
  age: 28,
  company: 'Tech Corp',
  position: 'Frontend Developer',
};

console.log(profile);
```
