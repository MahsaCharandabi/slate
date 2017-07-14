# Customers
The Echonio API allows you to create, delete, and update your customers. You can retrieve individual customers as well as a list of all your customers. Importing customers by file is available in CSV or JSON formats.


## The customer object

Attributes | Type | Description
--------- | ------- | -------
id | UUID | Unique identifier for the object
organizationId | UUID | Unique identifier for the organization
creatorOperatorId | UUID | Unique identifier for the operator who has creted the customer
avatarUploadedFileId | UUID | Unique identifier for the uploaded avatar
type | String | Type of the customer. (corporate/personal)
identity | Object | Customer's identity information
tagsIds | Array | List of customer's tags' ids
contacts | Array | List of customer's contacts


## Create a customer
> Definition:

```curl
POST http://api.echon.io/v1/customers
```
> Example Request:

```curl
curl -X POST \
  http://api.echon.io/v1/customers \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 2ad518c2-e721-31b1-7b64-1154943fff57' \
  -d 'identity=%7B%22title%22%3A%22%DA%A9%D8%A7%D9%81%DB%8C%20%D8%B4%D8%A7%D9%BE%22%2C%22name%22%3A%22%D8%B1%D8%A7%D8%AF%DB%8C%D9%88%22%2C%22manager%22%3A%22%D9%86%D8%AF%D8%A7%20%DB%8C%D8%A7%D8%B1%DB%8C%22%7D&contacts=%5B%7B%22type%22%3A%22tel%22%2C%22value%22%3A%22%2B982123422342%22%7D%2C%7B%22type%22%3A%22mobile%22%2C%22value%22%3A%22%2B982123422342%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%7D%5D&type=corporate'
```
> Example Response:

```json
{
  "id": "61d9ebbf-084f-4221-ad71-d45d4b1a6ff1",
  "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
  "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
  "avatarUploadedFileId": null,
  "type": "corporate",
  "identity": {
    "name": "Art",
    "title": "Restaurant",
    "manager": "Helen Cron"
  },
  "tagsIds": [
    "9639b18c-13eb-4ccb-a3f1-9ee75c6a4a77"
  ],
  "contacts": [
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
  ]
}
```

Creates a new customer object.

###Returns
Returns a customer object if the call succeeded. The returned object will have information about identity, contact type, and contacts, if that information has been provided. If a non-existent operator is provided, or the operator doesn't have write access to customer the call will return an error. 



## Import customers by file
> Definition:

```curl
POST http://api.echon.io/v1/customers/import
```
> Example Request:

```curl
curl -X POST \
  http://api.echon.io/v1/customers/import \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 53cab9e5-0472-ee91-6fc2-d5dbb4df6157' \
  -d id=9d0ba832-eef8-4fcf-bd8f-90be717805f7
```

For Importing customers you should first upload your customers' file in CSV or JSON format as described in (#Files) section, Then you get a UUID and you can Import the customers in that file by calling api's import route with that UUID as id property in request.

### Returns

Returns the number of created customers.


## Retrieve a customer
> Definition:

```curl
GET http://api.echon.io/v1/customers/{CUSTOMER_ID}

```
> Example Request:

```curl
curl -X GET \
  http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1 \
  -H 'authorization: bearer   2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 6b17519e-cc57-36d5-7249-d54a01ded361' \
  -d 'identity=%7Bname%3A%22%D9%87%D9%86%D8%B1%22%2Ctitle%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2Cmanager%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&contacts=%5B%7B%22id%22%3A%226dffa198-05b9-407f-b56f-187ccc17a33d%22%2C%22role%22%3Anull%2C%22type%22%3A%22tel%22%2C%22title%22%3Anull%2C%22value%22%3A%22%2B982155556666%22%2C%22fullname%22%3A%22%D8%A7%D8%B5%D8%BA%D8%B1%20%D8%AA%D8%B1%D9%82%D9%87%22%7D%2C%7B%22id%22%3A%22ce60ac6d-f63a-4a3e-9d87-a7c5e53321bf%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22type%22%3A%22mobile%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%2C%22value%22%3A%22%2B982123422342%22%2C%22fullname%22%3Anull%7D%5D&type=corporate'
```
> Example Response:

```json
{
  "id": "61d9ebbf-084f-4221-ad71-d45d4b1a6ff1",
  "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
  "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
  "avatarUploadedFileId": null,
  "type": "corporate",
  "identity": {
    "name": "Art",
    "title": "Restaurant",
    "manager": "Helen Cron"
  },
  "tagsIds": [
    "9639b18c-13eb-4ccb-a3f1-9ee75c6a4a77"
  ],
  "contacts": [
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
  ]
}
```
Retrieves the details of an existing customer. You need only supply the unique customer identifier that was returned upon customer creation.

###Returns
Returns a customer object if a valid identifier was provided.


## Update a customer
> Definition:

```curl
PUT http://api.echon.io/v1/customers/{CUSTOMER_ID}

```
> Example Request:

```curl
curl -X PUT \
  http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 297e947b-eb23-9b5b-5a8d-e0447598ec26' \
  -d 'identity=%7B%22name%22%3A%22%D9%87%D9%86%D8%B1%22%2C%22title%22%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2C%22manager%22%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&type=corporate'
```
> Example Response:

```json
{
  "id": "61d9ebbf-084f-4221-ad71-d45d4b1a6ff1",
  "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
  "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
  "avatarUploadedFileId": null,
  "type": "corporate",
  "identity": {
    "name": "Art",
    "title": "Restaurant",
    "manager": "Helen Cron"
  },
  "tagsIds": [
    "9639b18c-13eb-4ccb-a3f1-9ee75c6a4a77"
  ],
  "contacts": [
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
  ]
}
```
Updates the specified customer by setting the values of the parameters passed. Any parameters not provided will be left unchanged.
This request accepts mostly the same arguments as the customer creation call.

### Returns
Returns a customer object with updated values in case of success.


## Delete a customer
> Definition:

```curl
DELETE http://api.echon.io/v1/customers/{CUSTOMER_ID}
```
> Example Request:

```curl
curl -X DELETE \
  http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 4628af72-775d-80ed-ea76-4eec3b92b20a'
```
> Example Response:

```json
{ 
  "result": "true", 
  "id": "61d9ebbf-084f-4221-ad71-d45d4b1a6ff1"
}
```
Permanently deletes a customer and events for that customer.

### Returns
Returns an object with a true parameter and the ID of deleted customer on success. If the customer ID does not exist, this call returns an error.

## List all customers
> Definition:

```curl
GET http://api.echon.io/v1/customers?search={KEYWORD}&offset={OFFSET_NUMBER}&limit={LIMIT_NUMBER}
```
> Example Request:

```curl
curl -X GET \
  'http://api.echon.io/v1/customers?search=Bob&offset=1&limit=200' \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 9fd3ea04-7f8f-ef9f-c68d-f0f08cdf0b5b' \
  -d 'identity=%7B%22name%22%3A%22%D9%87%D9%86%D8%B1%22%2C%22title%22%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2C%22manager%22%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&contacts=%5B%7B%22id%22%3A%226dffa198-05b9-407f-b56f-187ccc17a33d%22%2C%22role%22%3Anull%2C%22type%22%3A%22tel%22%2C%22title%22%3Anull%2C%22value%22%3A%22%2B982155556666%22%2C%22fullname%22%3A%22%D8%A7%D8%B5%D8%BA%D8%B1%20%D8%AA%D8%B1%D9%82%D9%87%22%7D%2C%7B%22id%22%3A%22ce60ac6d-f63a-4a3e-9d87-a7c5e53321bf%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22type%22%3A%22mobile%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%2C%22value%22%3A%22%2B982123422342%22%2C%22fullname%22%3Anull%7D%5D&type=corporate'
```
> Example Response:

```json
{
  "items": [
    {
      "id": "af70a42c-9188-4c8d-b2bb-6a9b0d02093a",
      "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
      "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
      "avatarUploadedFileId": null,
      "type": "personal",
      "identity": {
        "lastName": "Shook",
        "firstName": "Gary",
        "fatherName": "Bob"
      },
      "tagsIds": [
        "a37e0e36-5f38-4d41-a676-396450ebaf4b"
      ],
      "contacts": [
        {
          "id": "3355abc5-5aa3-47a3-b2e2-1c0dd3172bf1",
          "data": {
            "note": null,
            "role": null,
            "type": "email",
            "value": "GaryCShook@dayrep.com",
            "responder": null
          }
        },
        {
          "id": "2e0b585f-6d5c-4a00-897f-6bb5672438e2",
          "data": {
            "note": null,
            "role": null,
            "type": "tel",
            "value": "001661-330-3341",
            "responder": null
          }
        },
      ]
    },
    {
      "id": "61d9ebbf-084f-4221-ad71-d45d4b1a6ff1",
      "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
      "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
      "avatarUploadedFileId": null,
      "type": "corporate",
      "identity": {
        "name": "Art",
        "title": "Restaurant",
        "manager": "Helen Cron"
      },
      "tagsIds": [
        "9639b18c-13eb-4ccb-a3f1-9ee75c6a4a77"
      ],
      "contacts": [
        {
          "id": "3081b132-c98f-4c45-a2b8-19650d20af14",
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
    },
  ],
  "count": 2
}
```

Returns list of your customers. The customers are returned sorted by update date, with the most recent modified customers appearing first. It also has three optional parameters:
* search: accepts a keyword to search among customers' identities and their contacts, You may leave it blank to show all customers.
* offset: refers to the offset of the first item to retrive, blank offset will be replaced by default 0.
* limit: refers to the number of customers that you want to retrieve, It would get replace with the number of 100 in case of blank limit or larger than 100.



## Add tag to customer
> Definition:

```curl
POST http://api.echon.io/v1/customers/{CUSTOMER_ID}/tags
```
> Example Request:

```curl
curl -X POST \
  http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/tags \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 7c9fe335-a56d-4115-ad46-636c5cfcc612' \
  -d tagId=726af1c1-a089-4371-bf26-1b3608683800
```
> Example Response:

```json
{
  "result": true,
  "customerId": "61d9ebbf-084f-4221-ad71-d45d4b1a6ff1",
  "tagId": "9639b18c-13eb-4ccb-a3f1-9ee75c6a4a77",
  "timelineEvent": {
    "id": "6273b4f2-59b8-413c-8dad-0f939ab071c6",
    "customerId": "61d9ebbf-084f-4221-ad71-d45d4b1a6ff1",
    "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
    "type": "add-tag",
    "description": "Premium customer tag added",
    "data": {
        "tagId": "9639b18c-13eb-4ccb-a3f1-9ee75c6a4a77"
    },
    "updatedAt": "2017-07-06T07:34:19.961Z",
    "createdAt": "2017-07-06T07:34:19.961Z",
    "deletedAt": null
  }
}
```
Adds a tag you have defined before in #settings to the specific customer by passing tag's ID as 'tagId' parameter in request.

### Returns
Returns an object with result property of true, customer's ID, tag's ID and the created 'add-tag' timeline event in case of success.

## Remove tag from customer
> Definition:

```curl
DELETE http://api.echon.io/v1/customers/{CUSTOMER_ID}/tags/{TAG_ID}
```
> Example Request:

```curl
curl -X DELETE \
  http://api.echon.io/v1/customers/61d9ebbf-084f-4221-ad71-d45d4b1a6ff1/tags/9639b18c-13eb-4ccb-a3f1-9ee75c6a4a77 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: ecfd2610-874d-def3-2e99-39a02de794af'
```
> Example Response:

```json
{
  "result": true,
  "customerId": "61d9ebbf-084f-4221-ad71-d45d4b1a6ff1",
  "tagId": "9639b18c-13eb-4ccb-a3f1-9ee75c6a4a77",
  "timelineEvent": {
    "id": "025ff77f-d00e-484c-a14a-4e2217316370",
    "customerId": "61d9ebbf-084f-4221-ad71-d45d4b1a6ff1",
    "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
    "type": "remove-tag",
    "description": "Premium customer tag removed",
    "data": {
      "tagId": "9639b18c-13eb-4ccb-a3f1-9ee75c6a4a77"
    },
    "updatedAt": "2017-07-06T07:40:17.498Z",
    "createdAt": "2017-07-06T07:40:17.498Z",
    "deletedAt": null
  }
}
```
Removes a tag of an specific customer by passing tag's id in url.

### Returns
Returns an object with result property of true, customer's id, tag's id and the created 'remove-tag' timeline event in case of success.
