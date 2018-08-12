### Overview

#### Concepts

-   **TDD means that long periods of anticipation are only defused very gradually, and by tiny increments.**

-   TDD cycle / workflow
    The TDD cycle involves starting with a test that fails, then writing code to get it to pass.

    Cycle / Workflow will look a bit like this:

    1. We start by writing a functional test, describing the new functionality from the user’s point of view.

    2. Once we have a functional test that fails, we start to think about how to write code that can get it to pass (or at least to get past its current failure). We now use one or more unit tests to define how we want our code to behave—​the idea is that each line of production code we write should be tested by (at least) one of our unit tests.

    3. Once we have a failing unit test, we write the smallest amount of application code we can, just enough to get the unit test to pass. We may iterate between steps 2 and 3 a few times, until we think the functional test will get a little further.

    4. Now we can rerun our functional tests and see if they pass, or get a little further. That may prompt us to write some new unit tests, and some new code, and so on.

#### Extending Our Functional Test Using the unittest Module

#### Testing a Simple Home page with Unit Tests

-   Functional tests test the application from the outside, from the point of view of the user. Unit tests test the application from the inside, from the point of view of the programmer.

-   Functional tests should help you build an application with the right functionality, and guarantee you never accidentally break it. Unit tests should help you to write code that’s clean and bug free.

#### Django’s MVC, URLs, and View Functions

Django’s workflow goes something like this:

    1. An HTTP request comes in for a particular URL.

    2. Django uses some rules to decide which view function should deal with the request (this is referred to as resolving the URL).

    3. The view function processes the request and returns an HTTP response.

So we want to test two things:

    1. Can we resolve the URL for the root of the site (“/”) to a particular view function we’ve made?

    2. Can we make this view function return some HTML which will get the functional test to pass?

#### Important classes & methods

-   **TestCase**
    Provided by Django. It’s an augmented version of the standard unittest.TestCase, , with some additional Django-specific features,

-   **resolve**
    ```
    from django.urls import resolve
    ```
    resolve is the function Django uses internally to resolve URLs and find what view function they should map to.

#### How to investigate a failure

1.  The first place you look is usually the error itself.
2.  The next thing to double-check is: which test is failing?
3.  Then we look for the place in our test code that kicked off the failure.
4.  Look further down for any of our own application code which was involved with the problem.

#### VSC settings

[DJANGO PROJECTS IN VISUAL STUDIO CODE](https://automationpanda.com/2018/02/08/django-projects-in-visual-studio-code/)
