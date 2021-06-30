# Create an API for a Booking site - PART II

In this project we will continue building our API for booking a hotel. We will integrate a data la

## What you will be doing

This project will allow you to practise using:

> - HTTP methods
> - Database MongoDB CRUD operations
> - MVC Pattern
> - Layered Pattern

This project assumes you've already had experience with:

> - Routing Express
> - CRUD Operations
> - MongoDB Schemas
> - Using Schema references

## Tasks

Before starting copy all the files from the previous assignment in this folder and commit.  


## Task 1 - Creating and Configuring a Data Layer 

  1. Create a new folder `data`, we will use this folder to store all our data layer files.

### 1. customerData
   1. Create a new `customerData.js` file inside the data folder. 
   

### 2. hotelData
  1. Create a new `hotelData.js` file inside the data folder. 
 

### 3. reservationData
  1. Create a new `reservationData.js` file inside the data folder. 
 


## Task 2 - Creating and configuring the Service Layer

  1. Create a new folder `services`, we will use this folder to store all our service layer files.

### 1. customerService
   1. Create a new `customerService.js` file inside the service folder. 


### 2. hotelService
  1. Create a new `hotelService.js` file inside the service folder. 
 

### 3. reservationService
  1. Create a new `reservationService.js` file inside the service folder. 
  


## Task 3 - Transferring logic to the data layer and service layer

### 1. createCustomer()
  1. Bring the  `Customer.create()` logic (data related logic) to the `customerData.js`, you can create a method there `createCustomer` which will create the new customer. 
 
  2. Open `customerService.js` and import the `customerData` file. 

  3. Create a method `createCustomer` in `customerService.js` which uses the `customerData.createCustomer()` to create a new customer.
 
  3. Adapt the controller method `createCustomer()` so it uses `customerService` to create a new customer. 

  ### 2. getCustomers()
  1. Bring the  `Customer.find()` logic (data related logic) to the `customerData.js` file, you can create a method there `getCustomers` which will return a list of customers. 

  2. Create a method `getCustomers` in `customerService.js` which uses the `customerData.getCustomers()` to get a list of customers.

  3. Adapt the controller method `getCustomers()` so it uses `customerService` to query for a list of customers. 

### 2. getCustomers()
  1. Bring the data related logic to the `customerData.js`, get list of customers there
 
  2. import the `customerController` inside the customerRoutes. 

### 3. Reservation controller
  1. Create a new `reservationController.js` file inside the controllers folder. 
 
  2. import the `reservationController` inside the reservationRoutes. 



## Task 4 - Customer Controller
  1. Create a new controller method `createCustomer()` and add the logic to create a new customer.
  2. Create a new controller method `getCustomers()` and add the logic to list all customers from the database.


## Task 5 - Wire the controller methods to the Customer routes
 1. Wire the createCustomer method to a `POST` endpoint `/create` inside the customerRoutes. 
 2. Wire the getCustomers method to a `GET` endpoint `/list` inside the customerRoutes. 
 
 Example of wiring a controller method: 
 ```javascript
  const controller = require('../controllers/orderController'); 

  router.get('/', controller.getOrders);
   ```

## Task 6 - Hotel Controller
  1. Create a new controller method `createHotel()` and add the logic to create a new hotel.
  2. Create a new controller method `getHotels()` and add the logic to list all hotels from the database.

## Task 7 - Wire the controller methods to the Hotel routes
 1. Wire the createHotel method to a `POST` endpoint `/create` inside the hotelRoutes. 
 2. Wire the getHotels method to a `GET` endpoint `/list` inside the hotelRoutes. 
 
 Example of wiring a controller method: 
 ```javascript
  const controller = require('../controllers/orderController'); 

  router.get('/', controller.getOrders);
   ```

## Task 8 - Reservation Controller
  1. Create a new controller method `createReservation()` and add the logic to create a new reservation. 
   - Make sure to validate whether the `hotelId` and `customerId` exists in the database.


  2. Create a new controller method `getReservations()` and add the logic to list all reservations from the database.


## Task 9 - Wire the controller methods to the Reservation routes
 1. Wire the createReservation method to a `POST` endpoint `/create` inside the reservationRoutes. 
 2. Wire the getReservations method to a `GET` endpoint `/list` inside the reservationRoutes. 
 
 Example of wiring a controller method: 
 ```javascript
  const c# Create an API for a Booking site

In this project we will create our own API for booking a hotel. We will be able to add customers
to our backend and customers will be able to book a hotel. 

## What you will be doing

This project will allow you to practise using:

> - HTTP methods
> - Database MongoDB CRUD operations
> - MVC Pattern

This project assumes you've already had experience with:

> - Routing Express
> - CRUD Operations
> - MongoDB Schemas
> - Using Schema references

## Tasks

Before starting run `npm install` to install all the required packages. 


## Task 1 - Complete the .env file

1. Create a new `.env` file to store the database environment variables.
   
2. Configure your database env variables. 


## Task 2 - Creating our schemas

### 1. Create a new `CustomerSchema` with the following fields: 

- `firstname` - String
- `lastname` - String 
- `username` - String
- `createdDate` - Date

### 2. Create a new `HotelSchema` with the following fields: 

- `name` - String
- `Address` - String 
- `City` - String
- `Country` - String
- `Price` - Number
- `hasParking` - Boolean

### 3. Create a new `ReservationSchema` with the following fields: 

- `customerId` - ObjectID
- `hotelId` - ObjectID
- `bookedForm` - Date 
- `bookedUntil` - Date


## Task 3 - Creating and configuring controllers

### 1. Customer controller
  1. Create a new `customerController.js` file inside the controllers folder. 
 
  2. import the `customerController` inside the customerRoutes. 

### 2. Hotel controller
  1. Create a new `hotelController.js` file inside the controllers folder. 
 
  2. import the `hotelController` inside the hotelRoutes. 

### 3. Reservation controller
  1. Create a new `reservationController.js` file inside the controllers folder. 
 
  2. import the `reservationController` inside the reservationRoutes. 



## Task 4 - Customer Controller
  1. Create a new controller method `createCustomer()` and add the logic to create a new customer.
  2. Create a new controller method `getCustomers()` and add the logic to list all customers from the database.


## Task 5 - Wire the controller methods to the Customer routes
 1. Wire the createCustomer method to a `POST` endpoint `/create` inside the customerRoutes. 
 2. Wire the getCustomers method to a `GET` endpoint `/list` inside the customerRoutes. 
 
 Example of wiring a controller method: 
 ```javascript
  const controller = require('../controllers/orderController'); 

  router.get('/', controller.getOrders);
   ```

## Task 6 - Hotel Controller
  1. Create a new controller method `createHotel()` and add the logic to create a new hotel.
  2. Create a new controller method `getHotels()` and add the logic to list all hotels from the database.

## Task 7 - Wire the controller methods to the Hotel routes
 1. Wire the createHotel method to a `POST` endpoint `/create` inside the hotelRoutes. 
 2. Wire the getHotels method to a `GET` endpoint `/list` inside the hotelRoutes. 
 
 Example of wiring a controller method: 
 ```javascript
  const controller = require('../controllers/orderController'); 

  router.get('/', controller.getOrders);
   ```

## Task 8 - Reservation Controller
  1. Create a new controller method `createReservation()` and add the logic to create a new reservation. 
   - Make sure to validate whether the `hotelId` and `customerId` exists in the database.


  2. Create a new controller method `getReservations()` and add the logic to list all reservations from the database.


## Task 9 - Wire the controller methods to the Reservation routes
 1. Wire the createReservation method to a `POST` endpoint `/create` inside the reservationRoutes. 
 2. Wire the getReservations method to a `GET` endpoint `/list` inside the reservationRoutes. 
 
 Example of wiring a controller method: 
 ```javascript
  const controller = require('../controllers/orderController'); 

  router.get('/', controller.getOrders);
   ```



# Bonus: 
Add a roomSchema, one hotel can have multiple rooms. Upon making a reservation the user has to select a room. 
Make sure to check whether the room is still available during this period. 

# Part 2 : 



ontroller = require('../controllers/orderController'); 

  router.get('/', controller.getOrders);
   ```



# Bonus: 
Add a roomSchema, one hotel can have multiple rooms. Upon making a reservation the user has to select a room. 
Make sure to check whether the room is still available during this period. 

# Part 2 : 



