# Week 9: Meeting customer requirements

### Acceptance testing
An acceptance test is a formal description of the behaviour of an application, generally expressed as an example or usage scenario. Agile methods tend to use acceptance tests as the main form of functional specification and the only formal expression of business requirements. Other teams may use acceptance tests as a complement to specification documents containing use cases.

Advantages of acceptance testing:
- encourages closer collaboration between developers and customers, users or domain experts, as they entail that business requirements should be expressed

- providing a clear and unambigious *contract* between customers and developers - a product which passes acceptance tests will be considered adequate

- decreasing the chance of severity both of new defects and regressions

### Test Driven Development (TDD)
Test-driven development is an approach to software development where you write tests first, then use those tests to drive the design and development of your software application.

#### Red Green Refactor
The red phase is the starting point of this cycle. At this stage, we write a simple test that informs the implementation of a feature, but when you run this test as is, it should fail as this feature is not yet implemented.

The green phase is where you implement code to make your test pass, where the goal is to find a solution without worrying about optimising your implementation. This is usually the bare minimum to make the test pass.

In the refactor phase, we look at how we can implement our code better or more efficiently. We can look at this in two ways, by consdering the characteristics of a good test (see [Week 6](WEEK6.md)). We can refactor our implementation code by looking at how to accomplish the same output with more descriptive or efficient code.

#### Implications of TDD
- Design must be organic - running code provides feedback between decisions
- Developers must write the unit tests - rather than waiting for someone else to do so
- Development environment must provide rapid feedback after small changes
- System must consist of many loosely coupled components, to make testing easy

#### TDD Motivation - Projects
- Quality assurance becomes proactive rather than reactive
- Estimations can be accurate enough to involve real customers in daily development
- Engineers can engage in minute-by-minute collaboration
- Short iterations deliver real business value as each iteration produces a working product

#### TDD Motivation - People
- Gives you the protection of tests from the start
- Provides clear feedback as progress continues

#### TDD Motivation - Code
- Encourages good object oriented design practice as we must think like the user of the class when we design (interface first, then internals)
- Encourages design for testability as it avoids the hidden dependencies that can make test-last so difficult
- We get an unambiguous progress meter
- We build up a comprehensive set of regression tests as we go along