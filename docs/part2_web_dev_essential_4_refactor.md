### Refactoring

##### Review Unitest

-   Unit test, Small or large steps

    TDD is like having a ratchet that lets you save your progress, take a break, and make sure you never slip backwards. That way you donâ€™t have to be smart all the time.

-   Don't test constants
    In general, one of the rules of unit testing is Don’t test constants, and testing HTML as text is a lot like testing a constant.

-   The more atomic your commits, the better

-   Unit tests are really about testing logic, flow control, and configuration.

##### Refactoring to Use a Template

###### Concept

Improvement the code without changing its functionality.

Refactoring is behaviour preserving.

##### Important class & functions

-   Selenium
    -   **find_element_by_tag_name, find_element_by_id, find_eleements_by_tag_name**
        (notice the extra s, which means it will return several elements rather than just one)
    -   **send_keys**
        This is Selenium’s way of typing into input elements.
    -   **Keys**
        The Keys class (don’t forget to import it) lets us send special keys like Enter
    -   **time.sleep**
        The time.sleep is there to make sure the browser has finished loading before we make any assertions about the new page.
    -   **any** :star:
        any is a generator expression, which is like a list comprehension but awesomer. You need to read up on this. If you Google it, you’ll find [Guido himself explaining it nicely](http://python-history.blogspot.com/2010/06/from-list-comprehensions-to-generator.html).
