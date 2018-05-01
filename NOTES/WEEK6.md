# Week 6: Testing functionality in isolation

A **test double** is a generic term for any case where production objects are replaced for testing purposes. In general, when you create any sort of test double, it's going to replicate an object of a specific class.

#### Types of test doubles
- A **dummy** is an object which is passed around but never actually used, usually these are used to fill parameter lists.

- A **fake** is an object with a fully working implementation and behaves like a real object of its type, but usually takes some shortcut which makes them not suitable for production, but easier to test. For example, a data persistence object that uses an in-memory database instead of hitting a real production database.

- A **stub** can be told to return a specified fake value when a given method is called, usually not responding at all to anything outside what's programmed in for the test. For example, if your test subject requires a companion object to provide some sort of data, you can use a stub to *stub out* that data source and return consistent fake data in your test setup.

- A **spy** keeps track of what methods are called and what arguments they are called with. These can be used for test assertions, like checking whether a specific method was called or that it was called with the correct argument. Spies are useful when you want to test the relationship between two objects. For example, an email service may record how many times it fetched and received messages.

- A **mock** is similar to a spy, but instead, you typically set up expectations beforehand. You tell it what you expect to happen, executing the code you're testing, and then verify that the correct behaviour happened.
