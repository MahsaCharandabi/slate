# Operators
The Echonio API allows you to create, delete, and update your operators. You can retrieve individual operators as well as a list of all your operators.


## The operator object
Attributes | Type | Description
--------- | ------- | -------
id | UUID | Unique identifier for the object
firstName | String | Operator's first name
lastName | String | Operator's last name
email |String | Operator's email address
actions | Object | List of actions with true/false value
avatarUploadedFileId | UUID | Unique identifier for operator's avatar file


## Create an operator
> Definition:

```curl
  POST http://api.echon.io/v1/operators
```
> Example Request:

```curl
curl -X POST \
  http://localhost:7337/v1/operators \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 7dbb15a2-b3a7-c82a-f29c-ab65d6468cc1' \
  -d 'firstName=%D9%81%D8%B1%D8%B2%D8%A7%D9%85&lastName=%D8%AE%D8%AC%D8%B3%D8%AA%D9%87&email=hi%40far077za3m.me&password=11111111&actions=%7B%22configDepartments%22%3A%20true%2C%20%22removeCustomerTag%22%3A%20true%2C%20%22addCustomerTag%22%3A%20true%2C%20%22importCustomers%22%3A%20true%2C%20%22editCustomer%22%3A%20true%2C%20%22createCustomer%22%3A%20true%2C%20%22deleteCustomer%22%3A%20true%2C%20%22manageOperators%22%3A%20false%2C%20%22accessToTimeline%22%3A%20true%2C%20%22configOrganization%22%3A%20true%2C%20%22manageApplications%22%3A%20true%2C%20%22allowedEventTypesSlugForViewInTimeline%22%3A%20%7B%22sms%22%3A%20false%2C%20%22email%22%3A%20true%2C%20%22telegram%22%3A%20false%2C%20%22contracts%22%3A%20true%7D%2C%20%22allowedEventTypesSlugsForAddToTimeline%22%3A%20%7B%22sms%22%3A%20false%2C%20%22email%22%3A%20true%2C%20%22telegram%22%3A%20false%2C%20%22contracts%22%3A%20true%7D%7D&='
```
> Example Response:

```json
{
    "id": "5c06f079-59a0-4f07-af9f-4a932116038f",
    "firstName": "Arron",
    "lastName": "Dreher",
    "email": "Arron@dayrep.com",
    "actions": {
        "editCustomer": true,
        "importCustomers": true,
        "createCustomer": true,
        "deleteCustomer": true,
        "addCustomerTag": true,
        "removeCustomerTag": true,
        "accessToTimeline": true,
        "manageOperators": false,
        "configOrganization": true,
        "configDepartments": true,
        "manageApplications": true,
        "allowedEventTypesSlugsForAddToTimeline": {
            "contracts": true,
            "email": true,
            "sms": false,
            "telegram": false
        },
        "allowedEventTypesSlugForViewInTimeline": {
            "contracts": true,
            "email": true,
            "sms": false,
            "telegram": false
        }
    },
    "avatarUploadedFileId": null
}
```
Creates a new operator object.

###Returns
Returns an operator object if the call succeeded. The returned object contains operator's ID, first name, last name, avatar's file ID and the actions of operator in an object. 



## Retrieve an operator
> Definition:

```curl
  GET http://api.echon.io/v1/operators/{OPERATOR_ID}
```
> Example Request:

```curl
curl -X GET \
  http://api.echon.io/v1/operators/c7e94231-e6a7-4826-adf0-e9e626d0c486 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 147ddb11-cf59-75db-8ca4-c1f609d1a1ae' \
  -d metaTags=%5B%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22firstName%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22test%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D8%AA%D8%B3%D8%AA%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22lastName%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%20%D8%AE%D8%A7%D9%86%D9%88%D8%A7%D8%AF%DA%AF%DB%8C%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22title%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D8%B9%D9%86%D9%88%D8%A7%D9%86%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22name%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22test%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%20%D9%BE%D8%AF%D8%B1%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Atrue%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22manager%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Atrue%2C%22defaultValue%22%3A%22%22%7D%5D
```
> Example Response:

```json
{
    "id": "5c06f079-59a0-4f07-af9f-4a932116038f",
    "firstName": "Arron",
    "lastName": "Dreher",
    "email": "Arron@dayrep.com",
    "actions": {
        "superuser": true,
        "editCustomer": true,
        "addCustomerTag": true,
        "createCustomer": true,
        "deleteCustomer": true,
        "importCustomers": true,
        "manageOperators": false,
        "accessToTimeline": true,
        "configDepartments": true,
        "removeCustomerTag": true,
        "configOrganization": true,
        "manageApplications": true,
        "allowedEventTypesSlugForViewInTimeline": {
            "sms": false,
            "email": true,
            "telegram": false,
            "contracts": true
        },
        "allowedEventTypesSlugsForAddToTimeline": {
            "sms": false,
            "email": true,
            "telegram": false,
            "contracts": true
        }
    },
    "avatarUploadedFileId": null
}
```
Retrieves an existing operator. You need only supply the unique operator identifier that was returned upon operator creation.

###Returns
Returns an operator object if a valid identifier was provided.


## Update an operator
> Definition:

```curl
  PUT http://api.echon.io/v1/operators/{OPERATOR_ID}
```
> Example Request:

```curl
curl -X PUT \
  http://api.echon.io/v1/operators/c7e94231-e6a7-4826-adf0-e9e626d0c486 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 5f8a1f32-e710-678f-faea-0f3447ebbcfd' \
  -d actions=%7B%22test%22%3Atrue%2C%22editCustomer%22%3Atrue%2C%22createCustomer%22%3Atrue%2C%22deleteCustomer%22%3Atrue%2C%22manageOperators%22%3Afalse%2C%22accessToTimeline%22%3Atrue%2C%22configOrganization%22%3Atrue%2C%22manageApplications%22%3Atrue%2C%22allowedEventTypesSlugsForAddToTimeline%22%3A%7B%22contracts%22%3Atrue%2C%22email%22%3Atrue%2C%22sms%22%3Afalse%2C%22telegram%22%3Afalse%2C%22note%22%3Atrue%7D%2C%22allowedEventTypesSlugForViewInTimeline%22%3A%7B%22contracts%22%3Atrue%2C%22email%22%3Atrue%2C%22sms%22%3Afalse%2C%22telegram%22%3Afalse%2C%22hasat%22%3A%22reza%22%7D%7D
```
> Example Response:

```json
{
    "id": "5c06f079-59a0-4f07-af9f-4a932116038f",
    "firstName": "Arron",
    "lastName": "Dreher",
    "email": "Arron@dayrep.com",
    "actions": {
        "editCustomer": true,
        "importCustomers": true,
        "createCustomer": true,
        "deleteCustomer": true,
        "addCustomerTag": true,
        "removeCustomerTag": true,
        "accessToTimeline": true,
        "manageOperators": false,
        "superuser": true,
        "configOrganization": true,
        "configDepartments": true,
        "manageApplications": true,
        "allowedEventTypesSlugsForAddToTimeline": {
            "contracts": true,
            "email": true,
            "sms": false,
            "telegram": false
        },
        "allowedEventTypesSlugForViewInTimeline": {
            "contracts": true,
            "email": true,
            "sms": false,
            "telegram": false
        }
    },
    "avatarUploadedFileId": null
}
```
Updates the specified operator by setting the values of the parameters passed. Any parameters not provided will be left unchanged.
This request accepts mostly the same arguments as the operator creation call.

### Returns
Returns an operator object with updated values in case of success.


## Delete an operator
> Definition:

```curl
  DELETE http://api.echon.io/v1/operators/{OPERATOR_ID}
```
> Example Request:

```curl
curl -X DELETE \
  http://api.echon.io/v1/operators/1a2a9733-c4d7-4f8c-81c4-b8b7628232b1 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 697e4f8d-180b-42dd-9eb9-c9e21ed7c08b' \
  -d 'firstName=%D9%81%D8%B1%D8%B2%D8%A7%D9%85&lastName=%D8%AE%D8%AC%D8%B3%D8%AA%D9%87&email=hi%40farzam.me&password=123&actions=%7B%22editCustomer%22%3Atrue%2C%22createCustomer%22%3Atrue%2C%22deleteCustomer%22%3Atrue%2C%22manageOperators%22%3Afalse%2C%22accessToTimeline%22%3Atrue%2C%22configOrganization%22%3Atrue%2C%22manageApplications%22%3Atrue%2C%22allowedEventTypesSlugsForAddToTimeline%22%3A%7B%22contracts%22%3Atrue%2C%22email%22%3Atrue%2C%22sms%22%3Afalse%2C%22telegram%22%3Afalse%7D%2C%22allowedEventTypesSlugForViewInTimeline%22%3A%7B%22contracts%22%3Atrue%2C%22email%22%3Atrue%2C%22sms%22%3Afalse%2C%22telegram%22%3Afalse%7D%7D'
```
> Example Response:

```json
{
    "result": true,
    "id": "5c06f079-59a0-4f07-af9f-4a932116038f"
}
```
Permanently deletes an operator.

### Returns
Returns an object with a true parameter and the ID of deleted operator on success. If the operator ID does not exist, this call returns an error.



## List all operators
> Definition:

```curl
  GET http://api.echon.io/v1/operators
```
> Example Request:

```curl
curl -X GET \
  http://api.echon.io/v1/operators \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 2a176854-7f0d-38d0-d100-549987949fb2' \
  -d metaTags=%5B%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22firstName%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22test%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D8%AA%D8%B3%D8%AA%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22lastName%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%20%D8%AE%D8%A7%D9%86%D9%88%D8%A7%D8%AF%DA%AF%DB%8C%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22title%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D8%B9%D9%86%D9%88%D8%A7%D9%86%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22name%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22test%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%20%D9%BE%D8%AF%D8%B1%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Atrue%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22manager%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Atrue%2C%22defaultValue%22%3A%22%22%7D%5D
```
> Example Response:

```json
[
    {
        "id": "10a271ff-4e38-4e3f-80da-0fe2c941540d",
        "departments": [
            {
                "id": "4b7c98de-98af-432f-bbf2-8a046bd8a3a6",
                "organizationId": "7660bf50-6d93-45ed-be85-7a254ecde565",
                "slug": "support",
                "title": "support",
                "createdAt": "2017-07-12T14:37:41.042Z",
                "updatedAt": "2017-07-12T14:37:41.042Z",
                "deletedAt": null,
                "departmentsOperators": {
                    "operatorId": "10a271ff-4e38-4e3f-80da-0fe2c941540d"
                }
            }
        ],
        "firstName": "Jerry",
        "lastName": "McCord",
        "email": "Jerry@dayrep.com",
        "actions": {
            "superuser": true
        },
        "avatarUploadedFileId": null
    },
    {
        "id": "5c06f079-59a0-4f07-af9f-4a932116038f",
        "departments": [],
        "firstName": "Arron",
        "lastName": "Dreher",
        "email": "Arron@dayrep.com",
        "actions": {
            "editCustomer": true,
            "addCustomerTag": true,
            "createCustomer": true,
            "deleteCustomer": true,
            "importCustomers": true,
            "manageOperators": false,
            "accessToTimeline": true,
            "configDepartments": true,
            "removeCustomerTag": true,
            "configOrganization": true,
            "manageApplications": true,
            "allowedEventTypesSlugForViewInTimeline": {
                "sms": false,
                "email": true,
                "telegram": false,
                "contracts": true
            },
            "allowedEventTypesSlugsForAddToTimeline": {
                "sms": false,
                "email": true,
                "telegram": false,
                "contracts": true
            }
        },
        "avatarUploadedFileId": null
    }
]
```

Returns list of your organization's departments. 
