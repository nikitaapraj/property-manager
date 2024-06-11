# Get started

## System requirements

* [GitHub Desktop](https://desktop.github.com/)
* The [Postman](https://www.postman.com/downloads/) app. The Real Estate Real Data API service runs on your development system with an `http://localhost` hostname. Therefore, the service doesn't work with the web-version of Postman.
* The current LTS version of [node.js](https://nodejs.org/en/)
* The current version of [json-server](https://www.npmjs.com/package/json-server)
* A fork of this repo. Ensure it includes the [database file](/api/property-manager.json).

## Start the service

1. Open the fork in **Command Prompt**. In **GitHub Desktop**, switch to the fork. Go to **Repositories** > **Open in Command Prompt**.

2. In **Command Prompt**, change directory to API.
    
    ```cli
    cd api
    ```

3. In the API directory, open the database file.

    ```cli
    json-server -w property-manager.json
    ```

    The json server starts on a local port. Note the index. This is your base URL.

    **Example response**
    ```cli
    Index:
    http://localhost:3000/

    Endpoints:
    http://localhost:3000/properties
    http://localhost:3000/users
    ```
The service is now started.

## Create users

## Create properties

## Next steps

* Update a property
* Delete a property
* Find a property
* Update a user
* Delete a user
* Find a user