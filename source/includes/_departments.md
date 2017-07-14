# Departments
The Echonio API allows you to create, delete, and update your departments. You can retrieve individual departments as well as a list of all your departments.
You can also assign an operator to a department or unassign an operator from it, And retrieve list of operators of a department.

## The department object
Attributes | Type | Description
--------- | ------- | -------
id | UUID | Unique identifier for the object
organizationId | UUID | Unique identifier for the organization
slug | String | Unique slug for department
title | String | title of the department

## Create a department
> Definition:

```curl
  POST http://api.echon.io/v1/departments
```
> Example Request:

```curl
curl -X POST \
  http://api.echon.io/v1/departments \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 9520003e-bb53-8faf-6913-1a16cdb38b22' \
  -d 'title=%D8%AA%D9%88%D8%B3%D8%B9%D9%87&slug=develop'
```
> Example Response:

```json
{
  "id": "11814c45-d23e-49bc-89dc-aa91f6bd63c8",
  "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
  "slug": "support",
  "title": "support"
}
```
Creates a new department object.

###Returns
Returns a department object if the call succeeded. The returned object contains department's ID, organization's ID and the slug and title you defined when creating the department. 



## Retrieve a department
> Definition:

```curl
  GET http://api.echon.io/v1/departments/{DEPARTMENT_ID}
```
> Example Request:

```curl
curl -X GET \
  http://api.echon.io/v1/departments/11814c45-d23e-49bc-89dc-aa91f6bd63c8 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: cee3d411-0739-0271-cd02-38221cc4e21d' \
  -d 'identity=%7B%22name%22%3A%22%D9%87%D9%86%D8%B1%22%2C%22title%22%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2C%22manager%22%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&contacts=%5B%7B%22id%22%3A%226dffa198-05b9-407f-b56f-187ccc17a33d%22%2C%22role%22%3Anull%2C%22type%22%3A%22tel%22%2C%22title%22%3Anull%2C%22value%22%3A%22%2B982155556666%22%2C%22fullname%22%3A%22%D8%A7%D8%B5%D8%BA%D8%B1%20%D8%AA%D8%B1%D9%82%D9%87%22%7D%2C%7B%22id%22%3A%22ce60ac6d-f63a-4a3e-9d87-a7c5e53321bf%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22type%22%3A%22mobile%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%2C%22value%22%3A%22%2B982123422342%22%2C%22fullname%22%3Anull%7D%5D&type=corporate'
```
> Example Response:

```json
{
  "id": "11814c45-d23e-49bc-89dc-aa91f6bd63c8",
  "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
  "slug": "support",
  "title": "support"
}
```
Retrieves an existing department. You need only supply the unique department identifier that was returned upon department creation.

###Returns
Returns a department object if a valid identifier was provided.


## Update a department
> Definition:

```curl
  PUT http://api.echon.io/v1/departments/{DEPARTMENT_ID}
```
> Example Request:

```curl
curl -X PUT \
  http://api.echon.io/v1/departments/11814c45-d23e-49bc-89dc-aa91f6bd63c8 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: b57d2bdf-414c-aa01-ad31-c4dcd575bc22' \
  -d 'title=%D8%AF%D9%BE%D8%A7%D8%B1%D8%AA%D9%85%D8%A7%D9%86%20%D8%A2%D9%BE%D8%AF%DB%8C%D8%AA%20%D8%B4%D8%AF%D9%87&slug=support'
```
> Example Response:

```json
{
  "id": "11814c45-d23e-49bc-89dc-aa91f6bd63c8",
  "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
  "slug": "support",
  "title": "customer support"
}
```
Updates the specified department by setting the values of the parameters passed. Any parameters not provided will be left unchanged.
This request accepts mostly the same arguments as the department creation call.

### Returns
Returns a department object with updated values in case of success.



## Delete a department
> Definition:

```curl
  DELETE http://api.echon.io/v1/departments/{DEPARTMENT_ID}
```
> Example Request:

```curl
curl -X DELETE \
  http://api.echon.io/v1/departments/11814c45-d23e-49bc-89dc-aa91f6bd63c8 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: d4bde47c-0f92-3988-addc-35c98d0c5540' \
  -d 'identity=%7B%22name%22%3A%22%D9%87%D9%86%D8%B1%22%2C%22title%22%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2C%22manager%22%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&contacts=%5B%7B%22id%22%3A%226dffa198-05b9-407f-b56f-187ccc17a33d%22%2C%22role%22%3Anull%2C%22type%22%3A%22tel%22%2C%22title%22%3Anull%2C%22value%22%3A%22%2B982155556666%22%2C%22fullname%22%3A%22%D8%A7%D8%B5%D8%BA%D8%B1%20%D8%AA%D8%B1%D9%82%D9%87%22%7D%2C%7B%22id%22%3A%22ce60ac6d-f63a-4a3e-9d87-a7c5e53321bf%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22type%22%3A%22mobile%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%2C%22value%22%3A%22%2B982123422342%22%2C%22fullname%22%3Anull%7D%5D&type=corporate'
```
> Example Response:

```json
{
  "result": true,
  "id": "11814c45-d23e-49bc-89dc-aa91f6bd63c8"
}
```
Permanently deletes a department.

### Returns
Returns an object with a true parameter and the ID of deleted department on success. If the department ID does not exist, this call returns an error.


## List all departments
> Definition:

```curl
GET http://api.echon.io/v1/departments
```
> Example Request:

```curl
curl -X GET \
  http://api.echon.io/v1/departments \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 63affb74-62a7-77c7-fa2a-ae82d1eb6695' \
  -d 'identity=%7B%22name%22%3A%22%D9%87%D9%86%D8%B1%22%2C%22title%22%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2C%22manager%22%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&contacts=%5B%7B%22id%22%3A%226dffa198-05b9-407f-b56f-187ccc17a33d%22%2C%22role%22%3Anull%2C%22type%22%3A%22tel%22%2C%22title%22%3Anull%2C%22value%22%3A%22%2B982155556666%22%2C%22fullname%22%3A%22%D8%A7%D8%B5%D8%BA%D8%B1%20%D8%AA%D8%B1%D9%82%D9%87%22%7D%2C%7B%22id%22%3A%22ce60ac6d-f63a-4a3e-9d87-a7c5e53321bf%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22type%22%3A%22mobile%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%2C%22value%22%3A%22%2B982123422342%22%2C%22fullname%22%3Anull%7D%5D&type=corporate'
```
> Example Response:

```json
[
  {
    "id": "11814c45-d23e-49bc-89dc-aa91f6bd63c8",
    "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
    "slug": "support",
    "title": "support"
  },
  {
    "id": "2ad20706-aeb5-4ff8-a3b5-1196dc2d8428",
    "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
    "slug": "sales",
    "title": "sales"
  }
]
```
Returns list of your organization's departments. 


## Add operator to a department
> Definition:

```curl
  POST http://api.echon.io/v1/departments/{DEPARTMENT_ID}/operators/{OPERATOR_ID}
```
> Example Request:

```curl
curl -X POST \
  http://localhost:7337/v1/departments/11814c45-d23e-49bc-89dc-aa91f6bd63c8/operators \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 58020537-a01f-a91d-609a-88dce47c1e88' \
  -d operatorId=5fe9122c-2b6e-4b0f-b70f-2feb829cde69
```
> Example Response:

```json
{
  "result": true,
  "departmentId": "11814c45-d23e-49bc-89dc-aa91f6bd63c8",
  "operatorId": "5fe9122c-2b6e-4b0f-b70f-2feb829cde69"
}
```
Assigns an operator to a department. 

### Returns
Returns an object with result property of true, department's ID and operator's ID in case of success.


## Remove operator from a department
> Definition:

```curl
  DELETE  http://api.echon.io/v1/departments/{DEPARTMENT_ID}/operators/{OPERATOR_ID}
```
> Example Request:

```curl
curl -X DELETE \
  http://api.echon.io/v1/departments/11814c45-d23e-49bc-89dc-aa91f6bd63c8/operators/5fe9122c-2b6e-4b0f-b70f-2feb829cde69 \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 55a3d022-2f7a-0765-44d7-22ecd132bae0'
```
> Example Response:

```json
{
  "result": true,
  "departmentId": "11814c45-d23e-49bc-89dc-aa91f6bd63c8",
  "operatorId": "5fe9122c-2b6e-4b0f-b70f-2feb829cde69"
}
```
Unassigns an operator to a department. 

### Returns
Returns an object with result property of true, department's ID and operator's ID in case of success.


## List all operators of a department
> Definition:

```curl
  GET http://api.echon.io/v1/departments/{DEPARTMENT_ID}/operators
```
> Example Request:

```curl
curl -X GET \
  http://api.echon.io/v1/departments/11814c45-d23e-49bc-89dc-aa91f6bd63c8/operators \
  -H 'authorization: bearer 2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 8c6f864d-ab74-68ca-e109-674c0f38cd2b' \
  -d 'identity=%7B%22name%22%3A%22%D9%87%D9%86%D8%B1%22%2C%22title%22%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2C%22manager%22%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&contacts=%5B%7B%22id%22%3A%226dffa198-05b9-407f-b56f-187ccc17a33d%22%2C%22role%22%3Anull%2C%22type%22%3A%22tel%22%2C%22title%22%3Anull%2C%22value%22%3A%22%2B982155556666%22%2C%22fullname%22%3A%22%D8%A7%D8%B5%D8%BA%D8%B1%20%D8%AA%D8%B1%D9%82%D9%87%22%7D%2C%7B%22id%22%3A%22ce60ac6d-f63a-4a3e-9d87-a7c5e53321bf%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22type%22%3A%22mobile%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%2C%22value%22%3A%22%2B982123422342%22%2C%22fullname%22%3Anull%7D%5D&type=corporate'
```
> Example Response:

```json
{
  "id": "11814c45-d23e-49bc-89dc-aa91f6bd63c8",
  "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
  "slug": "support",
  "title": "support",
  "createdAt": "2017-07-12T14:37:41.042Z",
  "updatedAt": "2017-07-12T14:37:41.042Z",
  "deletedAt": null,
  "operators": [
    {
      "id": "5fe9122c-2b6e-4b0f-b70f-2feb829cde69",
      "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
      "userId": "538de4e9-8859-4edb-9cee-f52c17f4d57a",
      "avatarUploadedFileId": null,
      "actions": {
        "superuser": true
      },
      "createdAt": null,
      "updatedAt": null,
      "deletedAt": null,
      "departmentsOperators": {
        "departmentId": "4b7c98de-98af-432f-bbf2-8a046bd8a3a6"
      }
    }
  ]
}
```
Returns information about the specified department and list of operators assigned to it. 
