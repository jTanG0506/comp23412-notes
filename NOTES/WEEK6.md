# Week 6: Testing functionality in isolation

A **test double** is a generic term for any case where production objects are replaced for testing purposes. In general, when you create any sort of test double, it's going to replicate an object of a specific class.

### Types of test doubles
- A **dummy** is an object which is passed around but never actually used, usually these are used to fill parameter lists.

- A **fake** is an object with a fully working implementation and behaves like a real object of its type, but usually takes some shortcut which makes them not suitable for production, but easier to test. For example, a data persistence object that uses an in-memory database instead of hitting a real production database.

- A **stub** can be told to return a specified fake value when a given method is called, usually not responding at all to anything outside what's programmed in for the test. For example, if your test subject requires a companion object to provide some sort of data, you can use a stub to *stub out* that data source and return consistent fake data in your test setup.

- A **spy** keeps track of what methods are called and what arguments they are called with. These can be used for test assertions, like checking whether a specific method was called or that it was called with the correct argument. Spies are useful when you want to test the relationship between two objects. For example, an email service may record how many times it fetched and received messages.

- A **mock** is similar to a spy, but instead, you typically set up expectations beforehand. You tell it what you expect to happen, executing the code you're testing, and then verify that the correct behaviour happened.

## Unit Testing

### FIRST: Best practices for unit tests
- **Fast** - tests should run quickly
- **Isolated** - tests should not do setup or teardown for one another
- **Repeatable** - tests should obtain the same result every time you run them (external data providers and concurrency issues could cause intermittent failures)
- **Self-validating** - tests should be fully automated - i.e. the output should either be *pass* or *fail*, rather than a developer having to interpret a log file
- **Timely** - ideally, tests should be written just before you write the production code they test

### Structure of a unit test
It is good practice to format the test into **given**, **when** and **then** sections:
- In the **given** section, setup any values needed
- In the **when** section, execute the code being test
- In the **then** section, assert the result you expect

```
Feature: User buys bananas
  Scenario: User purchases bananas during store opening times

  Given I have £10 GBP AND the time is before store closing time

  When I ask to buy 4 bananas

  Then I should have £8 AND a purchase of 4 bananas should have been executed
```

## Integration Testing
Integration tests, as the name suggests, is to test whether individually developed units work together as expected. It is achieved by combining multiple modules and running higher level tests against all of them to ensure they operate well together. It focuses mainly on the interfaces and flow of data between the modules.

For example, suppose our application has 3 modules, say Login Page, Mailbox and Deleted and each of them are integrated logically. Say we wish to check the integration between the login page and the mailbox, we would expect the application to direct us to the mailbox when login credentials are entered and the login button is pressed, for example. To test the integration between the mailbox itself and the Deleted folder, we would select a mail from mailbox and click the delete button and expect that this email appears in the Deleted folder.

### Big Bang Approach
In a big bang approach, all components are integrated together at **once**, and then tested. Clearly, this approach would be convenient for smaller systems. However, this approach means that fault localization is difficult, some interface links that need to be tested by accidentally missed out (as there may be alot of them), this type of integration testing can only happen once all the modules are designed.

### Incremental Approach
In a incremental approach, testing is done by joining two or more modules that are logically related. Then the other modules are added and tested for the proper functioning. This process continues until all of the modules are joined and tested successfully.

This process is carried out using dummy programs called **stubs** and **drivers**, which are used to simulate data communication with the calling module. A **stub** is called by the module under testing and a **driver** calls the module to be tested.

Incremental approach in turn is called out by two different methods: **bottom-up** and **top-down**.