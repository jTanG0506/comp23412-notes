# Week 1: Web Frameworks

## Model-View-Controller (MVC)
MVC is a software architecture pattern for developing applications in three interconnected parts - the model, the view and the controller.

## What is the model, view and controller?
**Model** - this represents the application data domain, in other words, it is responsible for handling the business logic and maintaining data. The model layer may also consist of networking code, persistence code, parsing code, etc.

**View** - this represents the user interface, with which the end user interacts with, via touch or click events, for example. These classes are typically reusable, since there isn't any domain-specific logic in them, for example, labels.

**Controller** - the role of the controller is to respond to user's interactions with the view. All of the user input logic is contained within the controller. This is the least reusable part, because it involves your domain-specific rules. It should be no surprise that what makes sense in your app probably wouldn’t make sense in someone else’s.

{% center %} ![MVC Diagram](assets/mvc-diagram.png) {% endcenter %}

## Advantages of MVC
- **Faster development process** as different programmers can work on different parts of the MVC simultaneously.

- The ability to have **multiple views for a single model** without much code duplication, as MVC separates the data and business logic from the display.

## Disadvantages of MVC
- **Increased complexity** - as developers new to this pattern may find it difficult. MVC increases the event-driven nature of the UI code, which may lead to more complex debugging.

- **Alot of similar derivations exists**, such as Model-View-ViewModel (MVVM) - where the main difference is the communication between layers, where the controller is replaced by a view model.