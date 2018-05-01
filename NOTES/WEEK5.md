# Week 5: Specification by Example

**Specification By Example** (SbE) is a user-driven contextual approach to defining software requirements. Its primary aim is to build the right product by focusing on shared understanding, thus establishing a single source of truth. We can also automate the acceptance criteria so that focus is on defect prevention rather than defect detection.

In **SbE**, we illustrate the expected behaviour using real life examples and example scenarios. These examples are then used to create requirements that are easier to understand and harder to misinterpret.

#### Example
For those that are interested, here is an example of SbE written in [Gherkin](https://github.com/cucumber/cucumber/wiki/Gherkin)
```
Feature: Feedback when entering invalid payment details

  We notice that alot of people who made mistakes at the payment stage
  simply closed the window. We need to be as helpful as possible here
  to avoid losing customers at this stage of the purchase.

  Background:
    Given I have chosen some items to buy
    And I am about to enter my credit card details

  Scenario: Credit card number too short
    When I enter a card number that's only 15 digits long
    And all the other details are correct
    And I submit the form
    Then the form should be redisplayed
    And I should see a message advising me of the correct number of digits
```