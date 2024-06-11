# Get properties by owner

Get a list of all properties a person owns.

## URL

**GET** `{base_url}/properties?owner_id={id}`

## Parameters

`id`: Unique identifier of the owner of the property

## Example

### Request

```
http://localhost:3000//properties?owner_id=2
```

### Response

```json
[
    {
        "building_type": "High-rise Office",
        "building_name": "100 Park Place",
        "address_line_1": "100 Park Place Dr",
        "address_line_2": "Suite 400",
        "address_line_3": "Atlanta, GA 30303",
        "is_occupied": "Y",
        "tenant_name": "Morgan & Morgan",
        "sq_footage": "10000",
        "monthly_rent": "$20000",
        "id": "1",
        "owner_id": 2,
        "manager_id": 1
    }
]
```
