# Console.log vs Debugger

**Debugging** is the act of looking over codes understanding what it is doing and figuring out why it is not executing as expected or not executing at all or maybe a user interaction with the application or website is triggering a weird behavior.

The Console method **log()** outputs a message to the web console. The message may be a single string, or it may be any or more JavaScript objects.

```JavaScript
console.log(msg)
```

**msg** The message to display.

console.log() out values to discover where bugs were.

```javascript
console.log('Total Price:', total); // Check if total value was stored

console.log('Here'); // If execution reached a certain function
```

Using console.log is inefficient, there is  a better way. Use **browser's debugging tools**. The **Debugger** allows you to literally go into the function and see what happens step by step

## Chrome Developers Tools

To open Chrome Developers Tools **Ctrl + Shift + I**

### Three Panels for Debugging using Sources Panel

1. File Navigator
2. Source Code Editor
3. Debugging Pane

#### Setup Breakpoint

**Breakpoint** is something your browser looks for in order to know when to pause execution of your code and allow your the opportunity to debug it.

* **Resume Button** allows the entire piece of code to executes

* **Step into Button** allows each line of code to execute one by one inside of each function

* **Step over Button** allows skipping over entire functions that are known to be working.

* Set a **Line-of-Code** Breakpoint by clicking on the line number that you would like to see more information about. Then run your code as usual and execution will stop on your set line-of-code breakpoint as opposed to needing to step through or over every function.

&nbsp;&nbsp;

#### Sources

[Console API Reference](https://developers.google.com/web/tools/chrome-devtools/console/api) by Google

[How to stop using console.log() and start using your browser’s debugger](https://medium.com/datadriveninvestor/stopping-using-console-log-and-start-using-your-browsers-debugger-62bc893d93ff) by Parag Zaveri

[Debugging your JavaScript code: console.log Vs debugger](https://codesource.io/debugging-your-javascript-code-console-log-vs-debugger/) by Emmanuel John
