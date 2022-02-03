# TL;DR

Pretty much everything described here boils down to getting fast feedback on every change you make, and making sure you are always on the right path forward.

Aim to setup processes to alert you when things are not working as they should be; your lines of code, your system and your delivery.

# Test all the things

* Unit/Developer Tests - as prescribed by the backend template, I advocate getting 100% unit test coverage on your code. These should be fast, and form the bulk of your test suite. Avoid testing each and every function. Instead, determine appropriate boundaries around a “unit of behaviour”, mock out its dependencies and use your tests to document behaviour, not just “x calls y with z”.

* Integration Tests - test your configuration with happy path integration tests that fire requests/events into your component, and check to see what comes out the other end, be it database updates or new events. Aim for just enough tests to cover each resource in a particular journey.

* Contract Tests - avoid slow and flaky end-to-end tests, and use contract tests to ensure dependencies work in the way you expect them, and you don’t break things for your consumers.

* Mutation Tests - ensure you really have covered each line of code by using tooling to change your implementation code and check if your tests still hold up.

# Tell, don’t ask; event-driven by default

* Avoid your functions and components knowing too much about what the other does. 

* A common code smell is when function A asks function B for some information, updates something in that data, and then gives function B the updated data back to save. Instead, function A should tell function B, and act on the result of that operation.

* On a micro-service level, aim to use messages over http requests. This will help encapsulate operations within their domain, de-couple workstreams, and allow for independent scaling of operations.

# Don’t work on all the things

* Limit work in progress by reducing the number of tickets allowed to be in flight. This promotes knowledge share by requiring the remaining person to pair with another, and reduces context switching for bottleneck roles

* Focus on items on the right of the board and get them to the customer sooner.

* Push small changes often to avoid merge conflicts and iterate through a task.

# Automate all things

* Identify bottlenecks in your process, and see if they can be automated, to reduce lead time and risk of human error.

* Learn your IDE and use the shortcuts to make safe refactorings.

* Put checks into your CI/CD pipeline 

# Don’t build all the things

It’s easy to rush ahead and try to plan out/code for every eventuality. In most situations it’ll end up as wasted effort as “You aren’t going to need it” (YAGNI).

* TDD as if you mean it, and write only enough code to pass your tests.

* Only add enough of a feature to test your hypothesis.

* Add enough observability to measure your experiment, and also to tell you when things go wrong.

# Refactor most of the things

* Tidy up your code to make it readable and easy to change for the next developer (it could be you in six months time!). 

* Equally, don’t refactor too early, as the wrong abstraction may be used, making it difficult add a change in the future. As a rule of thumb, it may be best to repeat a code block once for the time being, then refactor it on the third repetition, when the pattern is more apparent.

* However, it might be that this part of the code never changes ever again, so don’t waste your time refactoring things too much.

# Recommended Reading

* Pragmatic Programmer
* Extreme Programming Explained
* Domain Modelling Made Functional
* The Goal
* Mythical Man Month
* Refactoring Guru 
