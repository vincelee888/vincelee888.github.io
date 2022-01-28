This document serves as a guide to bear in mind as new code and components are created. It is a regurgitation of various other people’s ideas summarised here. Some items can come into conflict with each other, so try and be pragmatic; everything has to be weighed up and lead to an adequate compromise.

TL;DR

Pretty much everything described here boils down to getting fast feedback on every change you make, and making sure you are always on the right path forward.

Setup processes to alert you when things are not working as they should be; your lines of code, your system and your delivery.

Test all the things

Unit/Developer Tests - as prescribed by the backend template, I advocate getting 100% unit test coverage on your code. These should be fast, and form the bulk of your test suite. Avoid testing each and every function. Instead, determine appropriate boundaries around a “unit of behaviour”, mock out its dependencies. Use your tests to document behaviour, not just that x calls, this with y.

Integration Tests - test your configuration with happy path integration tests that fire requests/events into your component, and check to see what comes out the other end, be it database updates or new events. Aim for just enough tests to cover each pa 

Contract Tests - avoid slow and flaky end-to-end tests, and use contract tests to ensure dependencies work in the way you expect them.

Mutation Tests - ensure you really have covered each line of code by using tooling to change your implementation code and check if your tests still hold up.

Tell, don’t ask; event-driven by default

Avoid your functions and components knowing too much about what the other does.Don’t work on all the things

Automate all things

Don’t build all the things

Don’t work on all the things

Refactor most of the things

Recommended Reading

Pragmatic Programmer

Extreme Programming Explained

Domain Modelling Made Functional

Refactoring Guru 

