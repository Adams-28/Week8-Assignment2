# Week 8 Assignment 2: Managing Entities and Relationships

## Entity Relationship Diagram

```text
Customer (1) -------- (1) Address
    |
    | (1)
    |
    | (Many)
   Order (Many) ----- (Many) Product
```

## Fetch Type Configuration

-I selected `FetchType.LAZY` for almost all the entity relationships so that when I query for a customer's information it only reads the relevant data from the database when it needs it.

-I did use `FetchType.EAGER` for the customer to address relationship as they will need to retrieved together, but this could have also been set to LAZY.

-I could have primarily used `FetchType.EAGER` for my entity relationships since the code is realatively short, but it is not optimal/efficient as it reads all relevant data, even if it is not needed yet and can cause issues in much larger databases.

