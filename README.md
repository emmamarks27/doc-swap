# doc-swap

## Overview
## Authentication
If we had authentication, there would be the ability to authenticate as a regular user or as a event host, with certain routes only available to the event host.
## Events
Users can view events, create new ones, update them through booking
### Public user routes
These routes would be available to anyone authenticated as a regular user
#### Example - view event with ID 
`GET http://localhost:PORT/events/:id`

Example response
```
{
  id: 1,
  eventName: 'title',
  eventType: 'gig',
  eventDate: 'date',
  numberOfTickets: 500,
  numberOfTicketsRemaining: 100,
  minimumAge: 18,
  location: 'address',
  description: 'a real fun time',
  host: 'fun company ltd.',
  price: 15.5,
}
```
#### Example - view events 
`GET http://localhost:PORT/events/`

Example response
```
[{
  id: 1,
  eventName: 'title',
  eventType: 'gig',
  eventDate: 'date',
  numberOfTickets: 500,
  numberOfTicketsRemaining: 100,
  minimumAge: 18,
  location: 'address',
  description: 'a real fun time',
  host: 'fun company ltd.',
  price: 15.5,
},
{
  id: 2,
  eventName: 'title',
  eventType: 'gig',
  eventDate: 'date',
  numberOfTickets: 500,
  numberOfTicketsRemaining: 100,
  minimumAge: 18,
  location: 'address',
  description: 'a real fun time',
  host: 'fun company ltd.',
  price: 15.5,
}
]
```


### Host routes
These routes would be available to anyone authenticated as an event host
#### Create event

```
Example POST Request
POST http://localhost:PORT/events
'Content-Type': 'application/json'
Accept: 'application/json'

{
  id: 1,
  eventName: 'title',
  eventType: 'gig',
  eventDate: 'date',
  numberOfTickets: 500,
  numberOfTicketsRemaining: 100,
  minimumAge: 18,
  location: 'address',
  description: 'a real fun time',
  host: 'fun company ltd.',
  price: 15.5,
};
```
~~Planned extensions~~
#### Update event details (access by id)
#### Delete event
## Bookings
Users can view their bookings and book more tickets to events
These routes would be available to anyone authenticated as a regular user
### View all bookings
`GET http://localhost:PORT/bookings/`
```
[{
  eventName: 'title',
  numberOfTickets: 3,
  userName: 'userName',
  id: 1,
  totalPrice: 46.5,
},
{
  eventName: 'title',
  numberOfTickets: 5,
  userName: 'user2',
  id: 2,
  totalPrice: 100,
}]
```
### View booking by id
`GET http://localhost:PORT/bookings/:id`
```
{
  eventName: 'title',
  numberOfTickets: 3,
  userName: 'userName',
  id: 1,
  totalPrice: 46.5,
}
```
### Create a new booking.
## Testing
We don't have any
