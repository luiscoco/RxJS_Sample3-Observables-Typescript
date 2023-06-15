# RxJS_Sample3-Observables-Typescript

To run this code in VSCode, you'll need to set up a TypeScript project and install the necessary dependencies. Here's a step-by-step guide:

1.Install Node.js: Make sure you have Node.js installed on your system. You can download it from the official website: https://nodejs.org/

2.Install TypeScript: Open a terminal and run the following command to install TypeScript globally:
```
npm install -g typescript
```
3.Set up a project folder. Create a new folder for your TypeScript project.

4.Initialize a TypeScript project: Open a terminal in the project folder and run the following command:
```
tsc --init
````
This will generate a tsconfig.json file that contains TypeScript compiler options.

5.Install RxJS: In the terminal, navigate to your project folder and run the following command to install the required rxjs package:
```
npm install rxjs
```
6.Create a new file: In your project folder, create a new file called example1.ts and copy the TypeScript code into it.
```typescript
import { Observable } from 'rxjs';

const observable = new Observable((subscriber) => {
  subscriber.next(1);
  subscriber.next(2);
  subscriber.next(3);
  setTimeout(() => {
    subscriber.next(4);
    subscriber.complete();
  }, 1000);
});

observable.subscribe({
  next: (value) => {
    console.log(value); // Print the value to the console
  },
  complete: () => {
    console.log('Observable complete'); // Print a completion message
  },
});
```
7.Build the TypeScript code: In the terminal, navigate to your project folder and run the following command to compile the TypeScript code:
```
tsc
```
This will generate a JavaScript file (example.js) based on the TypeScript code.
8.To run the application:
```
node example1.js
```
