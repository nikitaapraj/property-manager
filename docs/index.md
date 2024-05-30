# REAL ESTATE, REAL DATA

Real Estate, Real Data is a REST API for managing real estate portfolios. It's a simplistic yet empowering way of managing properties. The API eliminates the need for complex spreadsheets to track all properties and numbers for each of them. The API also allows you to visualize trends and patterns in your portfolio without having to manually create charts.

## Overview

This API consists of two resources: `properties` and `users`. 

The `properties` resource includes information such as property type, location, area, rental income, and occupancy. 

The `users` resource includes owners and managers managing the property. Depending on their type, they have full or read-only access to the properties. Users with full access can create, read, update, and delete a property. Users with read-only access can view their properties but they can't add, delete, or update them. 

## Use cases

The following are a few example use cases where this API can be used:

* **Rental app or website**: If you manage an app or website for renting houses or offices, you can integrate this API to allow your users to efficiently manage their rental portfolio. 

* **Real estate management companies**: If you're a real estate management company, you can incorporate this API into your system to allow your team to track the performance of their properties more effectively.

## Get started

Implementing the Real Estate Real Data API is fast and easy. Try it out: [Create a property](/docs/create-property.md).

## Learn more

### API reference docs

* [`properties`](/properties.md)
* [`users`](/users.md)

### Properties Tutorials

* [Create a property](/docs/create-property.md)
* [Find a property](/docs/get-property.md)
* [Update a property](/docs/update-property.md)
* [Delete a property](/docs/delete-property.md)

### Users Tutorials

* [Create a user](/docs/create-user.md)
* [Find a user](/docs/get-user.md)
* [Update a user information and access](/docs/update-user.md)
* [Delete a user](/docs/delete-user.md)