# npm

## npm (Node Package Manager)

`npm` installs the packages you want to use and provides a useful interface to work with them.

But before using npm, you have to first install [Node.js](https://nodejs.org/en/) in your system.

npm consists of three distinct components

1. Use the **website** to discover packages, set up profiles, and manage other aspects of your npm experience

2. The **Command Line Interface (CLI)** runs from terminal, and is how most developers interact with npm

3. The **registry** is a large public database of JavaScript software and the meta-information surrounding it

The npm registry contains packages, many of which are also Node modules, or contain Node modules.

A **package** is a file or directory that is described by a `package.json` file. A package must contain a `package.json` file in order to be published to the npm registry.

A **module** is any file or directory in the `node_modules` directory that can be loaded by the Node.js `require()` function

## Semantic Versioning

![Image of semantic versioning breakout](https://media.geeksforgeeks.org/wp-content/uploads/semver.png)

- Major releases: \* or x (incompatible API changes)
- Minor releases: 1 or 1.x or ^1.0.4 (add functionality in a backwards-compatible manner)
- Patch releases: 1.0 or 1.0.x or ~1.0.4 (backwards-compatible bug fixes)

### ~, ^, and \*

The `*` character fixes both the major and minor version numbers, while matching any patch number.

```
~2.3.1

npm would match all versions greater than or equal to 2.3.1 and less than 2.4.0 for that dependency
```

The `^` character locks down the major version number, but leaves the minor and patch versions to be more flexible.

```
^2.2.3

npm will match any version that is greater than or equal to 2.2.3 and less than < 3.0.0
```

The `*` acts as a stand in for either the major, minor, or patch number and catches any version number for the place that it represents.

```
*

npm would equate to any version that was greater than or equal to 0.0.0,

while 1.* would allow versions greater than or equal to 1.0.0 and less than 2.0.0
```

## Sources

[npm Documentation](https://docs.npmjs.com/)

[npm Semantic Versioning](https://docs.npmjs.com/about-semantic-versioning)

[What do the tilde, caret and asterisk mean in package.json](https://gunnariauvinen.com/what-do-the-tilde-carrot-and-asterick-mean-in-package-dot-json/)

## Other Video

[JavaScript for React Developers](https://www.youtube.com/watch?v=NCwa_xi0Uuc&list=PLz1o23UtsUF_wnaN_dPyT7tEGKRvXkZuR&index=3&t=0s)

[Dan Abramov - The Melting Pot of JavaScript](https://www.youtube.com/watch?v=G39lKaONAlA)
