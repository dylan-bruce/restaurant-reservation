# Periodic Tables | Restaurant Reservation System
The restaurant reservation system is inteded for the use of a restaurant to track the tables, and to track the reservations and details for any given night.  
### Live Deployment
* Click to view the deployed [**Periodic Tables**](https://restres-frontend.herokuapp.com/dashboard) client.
* Click to view the deployed [**Periodic Tables**](https://restres-backend.herokuapp.com/) backend.
>Note: Will need to add a GET route to view any data.

---
## API

|Method  |Route                                   |Description                                    |
|--------|----------------------------------------|-----------------------------------------------|
|`GET`   |`/reservations`                         |Lists all reservations for the current date.    |
|`GET`   |`/reservations?date=YYYY-MM-DD`         |Lists all reservations for the searched date.   |
|`POST`  |`/reservations`                         |Creates a new reservation.  All fields are <br> required except for `reservation_id` and `status` <br> as these are automatically filled in.|
|`GET`   |`/reservations/:reservation_id`         |List a specific reservation by it's `reservation_id`.|
|`PUT`   |`/reservations/:reservation_id`         |Update a reservation by it's `reservation_id`.|
|`PUT`   |`/reservations/:reservation_id/status`  |Update the `status` of a reservation.|
|`GET`   |`/tables`                               |List all tables. |
|`POST`  |`/tables`                               |Create a new table.  Only writable fields are <br> `table_name` and `capacity`.|
|`PUT`   |`/tables/:table_id/seat`                |Assigns a reservation to a table and changes the <br> reservation's `status` to seated.|
|`DELETE`|`/tables/:table_id/seat`                |Removes a reservation from a table and changes <br> the reservation's `status` to finished.|

---
## Screenshots
### Dashboard
![This is an image of the dashboard.](/photos/dashboard.PNG)
### Create A Table
![This is an image of creating a table.](/photos/createATable.PNG)
### Create A Reservation
![This is an image of creating a reservation.](/photos/createAReservation.PNG)
### Cancel A Reservation
![This is an image of canceling a reservation.](/photos/cancelAReservation.PNG)
### Seat A Reservation
![This is an image of seating a reservation.](/photos/seatAReservation.PNG)
### Finish A Reservation
![This is an image of finishing a reservation.](/photos/finishAReservation.PNG)

---
## Summary
This application is intended for the use of restaurant staff to keep track of tables and record reservations.  It will allow you to do the following.
* Create a table with a custom name and a custom quantity of seats.
* Record reservations with the customers Name, Phone Number, Reservation Date, Reservation Time, and the Party Size.
* Edit reservations as needed.
* Cancel reservations as needed.
* Assign a reservation to a table.
* Clear a a reservation from a table once they are done eating.

---
## Technology Used
|Frontend|Backend|
|-|-|
|React|Node.js|
|JavaScript|Express|
|HTML|Knex|
|JSX|CORS|
|CSS|PostgreSQL|
|React Router/Hooks||

---
## Installation Instructions
1. Fork and clone this repository.
2. Run commands
  1. `cp ./back-end/.env.sample ./back-end/.env`
  2. `cp ./front-end/.env.sample ./front-end/.env`
3. Update the `./back-end/.env` file with the connection URL to your ElephantSQL database.
4. You should not need to make changes to the `./front-end/.env` file unless you want to connect to a backend at a location other than `http://localhost:5000`.
5. Run `npm install` to install project dependencies.
6. Run `npm run start:dev` to start the server in development mode.

> Note: Run any knex commands from within the back-end folder.  This is where the `knexfile.js` file is located.
