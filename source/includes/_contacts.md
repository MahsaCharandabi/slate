# Customer's contacts
The Echonio API allows you to create, delete, and update contacts of your customers. You can retrieve individual customers as well as a list of all your customers. Importing customers by file is available in CSV or JSON formats

## The contact object

Attributes | Type | Description
---------- | ---- | -------
id | UUID | Unique identifier for the object
data | Object | Contains note, role, type, value and responder of contact

### the data Object:

Properties | required | Description
---------- | -------- | ----------
note | No | Any note you may want to add to contact
role | No | Role of the responder
type | Yes | Type of contact like tel or email
value | Yes | The value of contact
responder | No | Name of who may respond


## Create a contact for customer
>Definition:

```curl
  POST http://api.api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/contacts
```
> Example Request:

```curl
curl -X POST \
  http://api.api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/contacts \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: c16cb6f8-55a1-92ee-2c9e-36ea24f95d87' \
  -d 'type=tel&value=001760-615-7972'
```
> Example Response:

```json
{
  "id": "bae0fe10-d4f7-4b1a-a2f6-2d97e4f5b5f3",
  "data": {
    "note": null,
    "role": "manager",
    "type": "tel",
    "value": "001760-615-7972",
    "responder": "Helen Cron"
  }
}
```
Creates a new contact object.

###Returns
Returns a contact object if the call succeeded. The returned object will have an id and a data containing note, role, type, value and responder of the contact.


## Retrieve a contact of a customer
> Definition:

```curl
  GET http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/contacts/bae0fe10-d4f7-4b1a-a2f6-2d97e4f5b5f3
```
> Example Request:

```curl
curl -X GET \
  http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/contacts/bae0fe10-d4f7-4b1a-a2f6-2d97e4f5b5f3 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 8f99d02c-1017-bca9-2ec3-87de857f0731' \
  -d 'type=tel&value=001760-615-79727'
```
> Example Response:

```json
{
  "id": "bae0fe10-d4f7-4b1a-a2f6-2d97e4f5b5f3",
  "data": {
    "note": null,
    "role": "manager",
    "type": "tel",
    "value": "001760-615-7972",
    "responder": "Helen Cron"
  }
}
```
Retrieves an existing contact. You need only supply the unique contact identifier that was returned upon contact creation.

###Returns
Returns a contact object if a valid identifier was provided.


## Update a contact of a customer
> Definition:

```curl
  PUT http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/contacts/bae0fe10-d4f7-4b1a-a2f6-2d97e4f5b5f3
```
> Example Request:

```curl
curl -X PUT \
  http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/contacts/bae0fe10-d4f7-4b1a-a2f6-2d97e4f5b5f3 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 13bd0bc8-527b-9400-d01b-34ee90607ec0' \
  -d 'type=tel&value=%2B9365484087&title=default&role=%D9%85%D8%AF%DB%8C%D8%B1&fullName=%D8%AD%D8%B3%D9%86%20%D8%B5%D8%A8%D8%A7%D8%AD'
```
> Example Response:

```json
{
  "id": "bae0fe10-d4f7-4b1a-a2f6-2d97e4f5b5f3",
  "data": {
    "note": null,
    "role": "manager",
    "type": "tel",
    "value": "001760-615-7972",
    "responder": "Helen Cron"
  }
}
```
Updates the specified contact of a customer by setting the values of the parameters passed. Any parameter not provided will be left unchanged.
This request accepts mostly the same arguments as the contact creation call.

### Returns
Returns a contact object with updated values in case of success.


## Delete a contact of a customer
> Definition:

```curl
  DELETE http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/contacts/bae0fe10-d4f7-4b1a-a2f6-2d97e4f5b5f3
```
> Example Request:

```curl
curl -X DELETE \
  http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/contacts/bae0fe10-d4f7-4b1a-a2f6-2d97e4f5b5f3 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: ee3b19c5-d51c-0c11-cde7-0ff2bb7dbf5e'
```
> Example Response:

```json
{
  "result": true,
  "contactId": "bae0fe10-d4f7-4b1a-a2f6-2d97e4f5b5f3"
}
```
Permanently deletes a customer's specific contact.

### Returns
Returns an object with a true parameter and the ID of deleted contact on success. If the customer ID or contact ID does not exist, this call returns an error.

## Get list of contacts for a customer
> Definition:

```curl
  GET http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/contacts
```
> Example Request:

```curl
curl -X GET \
  http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/contacts \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 7de28963-93ce-9616-5ccc-8985e9bb5739' \
  -d 'identity=%7Bname%3A%22%D9%87%D9%86%D8%B1%22%2Ctitle%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2Cmanager%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&contacts=%5B%7B%22id%22%3A%226dffa198-05b9-407f-b56f-187ccc17a33d%22%2C%22role%22%3Anull%2C%22type%22%3A%22tel%22%2C%22title%22%3Anull%2C%22value%22%3A%22%2B982155556666%22%2C%22fullname%22%3A%22%D8%A7%D8%B5%D8%BA%D8%B1%20%D8%AA%D8%B1%D9%82%D9%87%22%7D%2C%7B%22id%22%3A%22ce60ac6d-f63a-4a3e-9d87-a7c5e53321bf%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22type%22%3A%22mobile%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%2C%22value%22%3A%22%2B982123422342%22%2C%22fullname%22%3Anull%7D%5D&type=corporate'
```
> Example Response:

```json
[
  {
    "id": "bae0fe10-d4f7-4b1a-a2f6-2d97e4f5b5f3",
    "data": {
      "note": null,
      "role": "manager",
      "type": "tel",
      "value": "001760-615-7972",
      "responder": "Helen Cron"
    }
  },
  {
    "id": "3081b132-c98f-4c45-a2b8-19650d20af14",
    "data": {
      "note": null,
      "role": "manager",
      "type": "email",
      "value": "Helen@art.com",
      "responder": "Helen Cron"
    }
  }
]
```

