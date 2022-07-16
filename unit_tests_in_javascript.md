# Unit tests in JavaScript

## Learning objectives
- Write units tests for a JavaScript app.
- Explain why manual QA is often necessary alongside unit tests.

### Estimated time: 1h

## Description
In this lesson you will learn why automated testing is important in the application development process and you will familiarise yourself with various types of automated tests. Finally, you will learn how to use one of the most popular testing libraries and write tests for the smallest parts (units) of your application.

### Why is testing important?
Testing can give you confidence that any changes or new features you introduce into your code will not break other parts of the application. It's particularly important when working on large applications in bigger teams and shipping new features to live systems. It also helps you debug the code you're developing and improve its quality.

### Unit testing
In this lesson we will focus on unit testing; however, there are many types of tests we use in software development. Read [this short guide](https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing) to learn more about them and their use cases.

There are quite a few good libraries that promise to make unit testing in JavaScript applications easier. The most popular ones are Mocha, Jasmine, Tape, and Jest. We will focus on [Jest](https://jestjs.io/) as it became an industry standard in recent years.
- Read this guide to [getting started with Jest](https://jestjs.io/docs/getting-started).
- Read this article about [using matchers](https://jestjs.io/docs/using-matchers), which will help you set the most common tests you might need for your applications.
- Watch these three fun videos on unit testing:
    - [Unit testing in JavaScript Part 1 - Why unit testing?](https://youtu.be/Eu35xM76kKY).
    - [Unit testing in JavaScript Part 2 - Your first tests](https://youtu.be/XsFQEUP1MxI).
    - [Unit testing in JavaScript Part 3 - Test runners](https://youtu.be/pdx2HjFRaJY).

### Spoiler alert - TDD

Testing became such an integral part of building software that the whole new methodology called Test Driven Development (TDD) arose and strongly re-shaped how teams work and build software. You will learn about TDD in the next module. However, as it is quite an important concept, please read this [short article](https://medium.com/@gondy/the-importance-of-test-driven-development-f80b0d02edd8) just to understand the term.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
