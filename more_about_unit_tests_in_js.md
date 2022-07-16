# More about unit tests in JavaScript

## Learning objectives
- Write units tests for a JavaScript app

### Estimated time: 2.5h
## Description 
As you already know, tests are a very important part of the modern application development process. In this lesson, you will learn about some of the best practices in writing tests. You will learn what kind of functions are best to test and how to "fake" external services. You will also learn how to configure your project to test ES6 modules.

### Why is it important?
As a developer, you are going to write many tests for various applications. You will then need to decide not only **how**, but also **what** exactly should or can be tested.  Knowing the answers to those questions will make your work easier and your code cleaner.

### Pure functions
It is important to understand that testing should be done in isolation. It means that your tests should focus only on the functionality of a given function - not other functions that are being called by the tested function. So naturally, the best candidates for tests are so-called *pure functions*. These are functions that don't have *side effects* and do not depend on external functions.

 - Read this article to learn more about [*pure functions*](https://medium.com/@jamesjefferyuk/javascript-what-are-pure-functions-4d4d5392d49c).

You can already see that bringing tests into the development process can determine some important architectural decisions. Usually, it's best to keep the core logical functions separate from DOM manipulating functions. Such an approach will make the code more testable and therefore robust and future proof.

### Mocks
But how can you test anything other than *pure* functions? How can you test functionality that depends on asynchronous calls to an external API? How can we isolate such cases and write a reliable test for code that depends on external payloads? 
The best way to do it is to *mock* the results of our API calls. 

- Watch [this video](https://youtu.be/4Fl5GH4eYZ8) to learn the basics of using mocks with Jest.

### Manipulating the DOM
When you test functions that manipulate the DOM, you need to mock parts of the DOM in your test too. That way you ensure the test is isolated and you control its environment. Imagine you need to test a  function called `addItem()`  that adds an `<li>` item with some content to an HTML list (`<ul id="list" />`). In your test you need to mock the part of the DOM that the function is looking for (`<ul id="list" />`). You can then assign its children to a variable with `querySelectorAll()`, execute the `addItem()` function and `expect` the list to have one new element:

```javascript
const addItem = require ('./addItem');

test('Add one new item to the list', () => {
    document.body.innerHTML =
    '<div>' +
    '  <ul id="list"></li>' +
    '</div>';
    addItem();
    const list = document.querySelectorAll('#list li');
    expect(list).toHaveLength(1);
});
```

- Read more about [DOM manipulation with Jest](https://jestjs.io/docs/tutorial-jquery).
- Check [all available *expect* methods](https://jestjs.io/docs/expect).

### Testing ES6 modues

By default, Jest uses CommonJS notation. You have already seen it in the examples provided above. CommonJS modules are exported with `module.exports`: 
```javascript  
module.exports = someModule;
```
and imported with `require()`:
```javascript  
const someModule = require('./someModule');
```
So to make Jest understand ES6 native modules and notation like:
```javascript  
export default someModule;
```
and
```javascript  
import someModule from './someModule';
```
we need to *transform* all ES6 modules into CommonJS notation. Luckily it is very easy to automate this job with the use of [**Babel** compiler](https://babeljs.io/). 
All we'd need to do is to install Babel plugin:

```npm install --save-dev @babel/plugin-transform-modules-commonjs```

and create a new file in the project root directory called: `.babelrc` with the following code in it:

```javascript
{
  "env": {
    "test": {
      "plugins": ["@babel/plugin-transform-modules-commonjs"]
    }
  }
}
```

That's it! With Babel compiler configured, it is now possible to use `import` instead of `require` and write tests for ES6 modules.

## Additional materials
**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

Mocking data is a broader topic and you will be coming back to it as you test more and more complex applications. Jest provides a good number of mock functions that you might find useful in your tests.
- Read about all available [Jest mock functions here](https://jestjs.io/docs/mock-functions).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
