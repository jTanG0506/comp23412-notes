# Week 3: Data Modelling and Persistence

### Notice
The first section of this weeks lecture was an introduction to Spring annotations for persistence, which is not examinable hence ommited.

## CRUD - Create, Read, Update and Delete
When dealing with data persistent, we have four basic functions; **create**, **read**, **update** and **delete**. A model should have the ability to perform these four functions, if not, then maybe it could be broken down into models of its own.

Imagine we have a system that keeps track of events for a single venue. We would have a `events` resource, which would store `event` objects, which may look something like this:
```
"event": {
  "id": Int,
  "name": String,
  "desc": String,
  "capacity": Int,
  "datetime: Date
}
```

We will look at what each of the operations in the CRUD acronym do.

- **Create** - this would be called when we wished to create a new event and the values for `name`, `desc`, `capacity` and `datetime` would be passed when calling this function. Upon calling this function, there should be a new entry in the `events` resource, corresponding to this new event, which will also be automatically assigned a unique `id`, for access later on.

- **Read** - this would consist of functions which would be called to see all of the events currently booked. We could also have functions to retrieve a single book, for which we could supply the `name`, `description`, or `datetime`. Events are simply retrieved and displayed, not modified.

- **Update** - this would be called when the information about a event needs to be changed. For example, the program would supply new values for `name`, `desc`, `capacity` and `datetime`, which would update the corresponding entry in the `events` resource with the new fields supplied.

- **Delete** - this would be a function would be called to delete a event from the bookings. The program would pass one or more values (`id`, `name`, and / or `datetime`) to identify the event, and then this event would be removed from the `events` resource.