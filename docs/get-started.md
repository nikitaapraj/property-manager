# Get started

Learn how to start the Real Estate Real Data API, and create users and properties.

## System requirements

* [GitHub Desktop](https://desktop.github.com/)
* The [Postman](https://www.postman.com/downloads/) app. The Real Estate Real Data API service runs on your development system with an `http://localhost` hostname. Therefore, the service doesn't work with the web-version of Postman.
* The current LTS version of [node.js](https://nodejs.org/en/)
* The current version of [json-server](https://www.npmjs.com/package/json-server)
* A fork of this repo. Ensure it includes the [database file](/api/property-manager.json).

## Start the service

1. Open the fork in **Command Prompt**. In **GitHub Desktop**, switch to the fork. Go to **Repositories** > **Open in Command Prompt**.

2. In **Command Prompt**, change directory to API.
    
    ```
    cd api
    ```

3. In the API directory, open the database file.

    ```
    json-server -w property-manager.json
    ```

    The json server starts on a local port. Note the index. This is your base URL.

    **Example response**

    ```
    Index:
    http://localhost:3000/

    Endpoints:
    http://localhost:3000/properties
    http://localhost:3000/users
    ```

The service is now started.

## Create users

Create an `owner` or `manager` user and assign them `read-only` or `CRUD` permissions.

1. Open the **Postman** app and create a `POST` request.
    ```
    {base_url}/users/
    ```

2. In the **Headers** section, ensure **content-type** is `application/json`.

3. In the **Body** section, select **raw**.

4. In the **Body text** field, enter the properties and values for the `manager` user. See [Users](/users.md).

    *Note*: All properties are required.

5. Click **Send**. The `manager` user is created, and it appears in the **Response Body** section.

6. Repeat the above steps to create an `owner` user.

### Example

#### Request

```
http://localhost:3000/users
```

```json
{
    "id": "4",
    "username": "patrick.johnson",
    "role": "manager",
    "permissions": "crud"
}
```

#### Response

```json
{
    "id": "4",
    "username": "patrick.johnson",
    "role": "manager",
    "permissions": "crud"
}
```

## Create properties

Add a property to your portfolio.

1. In the **Postman** app, create a `POST` request.
    ```
    {base_url}/properties/
    ```

2. In the **Headers** section, ensure **content-type** is `application/json`.

3. In the **Body** section, select **raw**.

4. In the **Body text** field, enter the property details. See [Properties](/properties.md).

5. Click **Send**. A property is created and it appears in the **Response Body** section.

6. Repeat the above steps to create more properties.

### Example

#### Request

```
http://localhost:3000/properties
```

```json
{
    "building_name": "Ocean View Condos",
    "address_line_1": "789 Ocean View Dr",
    "address_line_2": "Suite 305",
    "address_line_3": "Atlanta, GA 35034",
    "id": 9,
    "owner_id": 7,
    "manager_id": 8
}
```

#### Response

```json
{
    "building_name": "Ocean View Condos",
    "address_line_1": "789 Ocean View Dr",
    "address_line_2": "Suite 305",
    "address_line_3": "Atlanta, GA 35034",
    "id": 9,
    "owner_id": 7,
    "manager_id": 8
}
```

## Next steps

* [Update a property](update-property.md)
* [Delete a property](delete-property.md)
* [Find a property](/get-property-by-owner.md)
* [Update a user](/update-user.md)
* [Delete a user](/delete-user.md)
* [Find a user](/get-user.md)

