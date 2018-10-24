# Lab12: Design Hotel management system

## Overview

An attempt to RDBMS schema design with a given requirements set.


## Problem Domain
The owners of “Async Inn” have approached you with plans to renovate their hotel chain. Currently they are tracking all the different locations and rooms in spreadsheets and binders. They currently have about 10 binders full of paperwork that consists of the difference between each location and the pricing for each room. The amount of time and paperwork it takes to manage the rooms and locations is costing the company both time and money. They are currently looking for a “better way” to maintain their business model.

They are currently looking for a full stack web application that will allow them to better manage their assets in their hotels. They are anticipating the ability to modify and manage rooms, amenities, and new hotel locations as they are built. They have turned to you to assist them in persisting their data across a relational database and maintain its integrity as they make changes to the system.

After your meeting with the team, you have extracted some basic requirememts about the data and how it should be represented in a database. You are going to attempt a first draft at a database schema to share with the team later on today.

To the best of your ability, create a system design of a database schema that meets all of the requirements below. The schema should take all of the requirements into consideration and allow a baseline for starting the creation of the web application.

## Requirements

- The hotel can hold many guests at any given time, in fact guests can come and go as they please…..asynchronously :)
- The hotel is named “Async Inn” and has many nationwide locations. Each location will have a name, city, state, address, and phone number.
- Async Inn prides themselves on their unique layout designs of each hotel room. They advertise as it being your “apartment for the night”. This means they have invested a lot of resources into how each room looks and feels. Some have one bedroom, others have 2 bedrooms, while a few are more of a cozy studio. The team mentioned that they like to label each room with a nickname to better tell the difference between each of the layouts and amenities each room has to offer. (for example, the Seattle location has two 2-bedroom suites, but one is named “Seahawks Snooze” while the other is named “Restful Rainier”, each with their own amenities.)
- They also take pride in the amenities that each room has to offer. This can consist of features like “air conditioning”, “coffee maker”, “ocean view”, “mini bar”, the list goes on…They requested that they would like the amenities associated with each of the rooms as they do vary.
- The rooms vary in price, per location, as well as per room number. They also have a few rooms that they want to advertise as pet friendly.
- The number of rooms for each hotel varies. Some hotels have only a few rooms, while others may have dozens.

## Schema description

The DB should include following entities:

- Guest
  - PK Guest_id
- Manager
  - PK Manager_id
- Room
  - PK Room_id
  - FK Amenity_id
  - FK_Location_id
  - FK_Price_modifier_id
- Location
  - PK_Location_id
- Amenity
  - PK_Amenity_id
- Action
  - PK_Action_id
  - FK_Bill_id
  - FK_Payment_id
  - FK_Reservation_id
  - FK_Staying_id
  - FK_Manager_id
- Bill
  - PK_Bill_id
  - FK_Guest_id
- Payment
  - PK_Payment_id
  - FK_Guest_id
- Reservation
  - PK_Reservation_id
  - FK_Guest_id
  - FK_Room_id
- Staying
  - PK_Staying_id
  - FK_Guest_id
  - FK_Room_id

All relationships are shown in the diagram below.

## Screenshots

![image](https://raw.githubusercontent.com/al1s/Lab12-Relational-Databases/master/schema.png)

