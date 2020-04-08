# Webpack vs Create-React-App

## Webpack

**webpack** is a _static module bundler_ for modern JavaScript applications.

Webpack goes through your package and creates what it calls a dependency graph which consists of modules which your webapp would require to function as expected.

Then, depending on this graph, it creates a new package which consists of the very bare minimum number of files required, often just a single bundle.js file which can be plugged in to the html file easily and used for the application.

## Create React App

**Create React App** is the best way to start building **a new single-page application** in React.

To create a project, run:

```
npx create-react-app app-name
cd app-name
npm start
```


## Sources

[An intro to Webpack: what it is and how to use it](https://www.freecodecamp.org/news/an-intro-to-webpack-what-it-is-and-how-to-use-it-8304ecdc3c60/)

[Create React App](https://create-react-app.dev/)

[Create React App github](https://github.com/facebook/create-react-app#create-react-app--)
