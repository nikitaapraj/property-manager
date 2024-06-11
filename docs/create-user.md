# Create a user

Create an `owner` or `manager` user and assign them `read-only` or `CRUD` permissions.

## Create a user

1. Open the Postman app on your desktop.

2. Create a `POST` request.

    ```
    {base_url}/users/
    ```

3. In the **Headers** section, ensure **content-type** is `application/json`.

4. In the **Body** section, select `raw` and then enter the properties and values in the text field. See the [Users properties](/users.md). All properties are required.


