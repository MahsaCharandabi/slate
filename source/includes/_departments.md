# Departments

## The department object

## Create a department

```curl
curl -X POST \
  http://echon.io/v1/departments \
  -H 'authorization: bearer 41d7404c0c3e4f7abe39591559250c67j07Pm1ij05b9TPNGTxXmB8bsXVriHBxCuYjyiFvEsDq6PRx6oLmX1f73ZAEDuDnkqhRBwAVIuR0dbVrNybnTV27tQRADMsy05mm9oW2BpVYnxp6RFRtN130BegjhSaxb6hLHf72AJQksALxgHM2nDky1BcXVy2SGciQshEIncmXtfELNKHgbEZn5vdcTb2kGShyHI8TMYX5oIBb0ycL0hvStSjaIiV69' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 9520003e-bb53-8faf-6913-1a16cdb38b22' \
  -d 'title=%D8%AA%D9%88%D8%B3%D8%B9%D9%87&slug=develop'
```
> The above command returns JSON structured like this:

```json

```

## Retrieve a department
> Definition:

```curl

```
> Example Request:

```curl
curl -X GET \
  http://echon.io/v1/departments/1dd01217-1061-482e-b00b-84de0bb11dc4 \
  -H 'authorization: bearer 115ced0cdb4244e5a2273bcd02bd46dbefHEcwT03SAsFT6EwxLwCFsFMJsVu11r9e5DOYE4YBp7NK5kY4thWSLGaUkKrb9HL2zHkt6A0Lyn6oSz63hwoYONx0Lz5VxV2HglRJfTmEPX575l1tkZ2P6GWZXXA3A7k0ZA1qUTxZ2y9hXrdyyTAeCXyMNAwhN3JxDV5SCHQfb5jGvnEIfmbJ2wuxDL4OaIEVdVTApiKw3asAGKOCyL1xOJL9axRKjf' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: cee3d411-0739-0271-cd02-38221cc4e21d' \
  -d 'identity=%7B%22name%22%3A%22%D9%87%D9%86%D8%B1%22%2C%22title%22%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2C%22manager%22%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&contacts=%5B%7B%22id%22%3A%226dffa198-05b9-407f-b56f-187ccc17a33d%22%2C%22role%22%3Anull%2C%22type%22%3A%22tel%22%2C%22title%22%3Anull%2C%22value%22%3A%22%2B982155556666%22%2C%22fullname%22%3A%22%D8%A7%D8%B5%D8%BA%D8%B1%20%D8%AA%D8%B1%D9%82%D9%87%22%7D%2C%7B%22id%22%3A%22ce60ac6d-f63a-4a3e-9d87-a7c5e53321bf%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22type%22%3A%22mobile%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%2C%22value%22%3A%22%2B982123422342%22%2C%22fullname%22%3Anull%7D%5D&type=corporate'
```
> Example Response:

```json

```


## Update a department
> Definition:

```curl

```
> Example Request:

```curl
curl -X PUT \
  http://echon.io/v1/departments/1dd01217-1061-482e-b00b-84de0bb11dc4 \
  -H 'authorization: bearer f9cacb7e20a943719eb3fdfb6f51a101uzfNCsb93Vrs3sHy1Hd2G8Iys81i6pFxcl3AUw58yDloQvVajxcrVSepI83RisoK5R9n3aYQqD8YTE1yn9GmZWroMLqOH3vxLGAUwXeNjONa3owWQotsnDrlf9FGbIfnOptdrvuoBcBThsdUJJZRKUGqlfMT0ilzntmVWILwSzVF8JKKYEBmP1laPmVOAySO3gpuKJZDhyXWdPuBkDADnS0BzGKJE1Ma' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: b57d2bdf-414c-aa01-ad31-c4dcd575bc22' \
  -d 'title=%D8%AF%D9%BE%D8%A7%D8%B1%D8%AA%D9%85%D8%A7%D9%86%20%D8%A2%D9%BE%D8%AF%DB%8C%D8%AA%20%D8%B4%D8%AF%D9%87&slug=support'
```
> Example Response:

```json

```


## Delete a department
> Definition:

```curl

```
> Example Request:

```curl
curl -X DELETE \
  http://echon.io/v1/departments/1dd01217-1061-482e-b00b-84de0bb11dc4 \
  -H 'authorization: bearer 3220dc682996472b8fb1d16ad4506cdbeRoDRZJb3N5zQPde8wwH2liXOQpnH5ZQf5aYxiZn055cgfcUhLOTriQ0SfJsIXWamiGwDldhzNPGUoQwB9vBfgWo9GdpP7UCyBGYWbHPsgPZtns0TnkmsVJKe9EH6L1ESiLYNdMnaJQJncAgwWhQPBnK1xq71lZzTrOTTQXYTVofbYA6A2EAoNw8DdzPNB20rjveodM32jg4xTtg5K1Fjl78E50nVEgt' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: d4bde47c-0f92-3988-addc-35c98d0c5540' \
  -d 'identity=%7B%22name%22%3A%22%D9%87%D9%86%D8%B1%22%2C%22title%22%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2C%22manager%22%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&contacts=%5B%7B%22id%22%3A%226dffa198-05b9-407f-b56f-187ccc17a33d%22%2C%22role%22%3Anull%2C%22type%22%3A%22tel%22%2C%22title%22%3Anull%2C%22value%22%3A%22%2B982155556666%22%2C%22fullname%22%3A%22%D8%A7%D8%B5%D8%BA%D8%B1%20%D8%AA%D8%B1%D9%82%D9%87%22%7D%2C%7B%22id%22%3A%22ce60ac6d-f63a-4a3e-9d87-a7c5e53321bf%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22type%22%3A%22mobile%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%2C%22value%22%3A%22%2B982123422342%22%2C%22fullname%22%3Anull%7D%5D&type=corporate'
```
> Example Response:

```json

```


## List all departments
> Definition:

```curl

```
> Example Request:

```curl
curl -X GET \
  http://echon.io/v1/departments \
  -H 'authorization: bearer 41d7404c0c3e4f7abe39591559250c67j07Pm1ij05b9TPNGTxXmB8bsXVriHBxCuYjyiFvEsDq6PRx6oLmX1f73ZAEDuDnkqhRBwAVIuR0dbVrNybnTV27tQRADMsy05mm9oW2BpVYnxp6RFRtN130BegjhSaxb6hLHf72AJQksALxgHM2nDky1BcXVy2SGciQshEIncmXtfELNKHgbEZn5vdcTb2kGShyHI8TMYX5oIBb0ycL0hvStSjaIiV69' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 63affb74-62a7-77c7-fa2a-ae82d1eb6695' \
  -d 'identity=%7B%22name%22%3A%22%D9%87%D9%86%D8%B1%22%2C%22title%22%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2C%22manager%22%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&contacts=%5B%7B%22id%22%3A%226dffa198-05b9-407f-b56f-187ccc17a33d%22%2C%22role%22%3Anull%2C%22type%22%3A%22tel%22%2C%22title%22%3Anull%2C%22value%22%3A%22%2B982155556666%22%2C%22fullname%22%3A%22%D8%A7%D8%B5%D8%BA%D8%B1%20%D8%AA%D8%B1%D9%82%D9%87%22%7D%2C%7B%22id%22%3A%22ce60ac6d-f63a-4a3e-9d87-a7c5e53321bf%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22type%22%3A%22mobile%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%2C%22value%22%3A%22%2B982123422342%22%2C%22fullname%22%3Anull%7D%5D&type=corporate'
```
> Example Response:

```json

```


## Add operator to a department
> Definition:

```curl

```
> Example Request:

```curl
curl -X POST \
  http://echon.io/v1/departments/3e7aba04-629a-43d6-beba-e4022bb90461/operators/10441c40-8f6f-4350-9d16-52c4f0f06a33 \
  -H 'authorization: bearer 41d7404c0c3e4f7abe39591559250c67j07Pm1ij05b9TPNGTxXmB8bsXVriHBxCuYjyiFvEsDq6PRx6oLmX1f73ZAEDuDnkqhRBwAVIuR0dbVrNybnTV27tQRADMsy05mm9oW2BpVYnxp6RFRtN130BegjhSaxb6hLHf72AJQksALxgHM2nDky1BcXVy2SGciQshEIncmXtfELNKHgbEZn5vdcTb2kGShyHI8TMYX5oIBb0ycL0hvStSjaIiV69' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 2ab77433-041d-271d-5456-591e14011a15'
```
> Example Response:

```json

```


## Remove operator from a department
> Definition:

```curl

```
> Example Request:

```curl
curl -X DELETE \
  http://echon.io/v1/departments/1dd01217-1061-482e-b00b-84de0bb11dc4/operators/1a2a9733-c4d7-4f8c-81c4-b8b7628232b1 \
  -H 'authorization: bearer 88fe8d1a6cfd408eba29b4c000427a7cH0NbzXX20ViFrGjfbPaiN57W4C8o73dzHKPrc561EDlqDJbLmTVmSJem86ueEMzcThuj89n4Ld1HHB8dGU72ojvwJakuFNKI3VBhFkhAHfi8pgl2icCyTkklcmwQ266tq4lHLsjanv9raufhP4gxWbvT6StWth8DGfDEJEC9AWLk5fbHNu2xFFLKE64sXgKGkm3MGVOtrTfDj1XTadcpG5uPbulDxoFz' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 55a3d022-2f7a-0765-44d7-22ecd132bae0'
```
> Example Response:

```json

```


## List all operators of a department
> Definition:

```curl

```
> Example Request:

```curl
curl -X GET \
  http://echon.io/v1/departments/3e7aba04-629a-43d6-beba-e4022bb90461/operators \
  -H 'authorization: bearer 41d7404c0c3e4f7abe39591559250c67j07Pm1ij05b9TPNGTxXmB8bsXVriHBxCuYjyiFvEsDq6PRx6oLmX1f73ZAEDuDnkqhRBwAVIuR0dbVrNybnTV27tQRADMsy05mm9oW2BpVYnxp6RFRtN130BegjhSaxb6hLHf72AJQksALxgHM2nDky1BcXVy2SGciQshEIncmXtfELNKHgbEZn5vdcTb2kGShyHI8TMYX5oIBb0ycL0hvStSjaIiV69' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 8c6f864d-ab74-68ca-e109-674c0f38cd2b' \
  -d 'identity=%7B%22name%22%3A%22%D9%87%D9%86%D8%B1%22%2C%22title%22%3A%22%D9%BE%DB%8C%D8%AA%D8%B2%D8%A7%22%2C%22manager%22%3A%22%D9%81%D8%B1%D8%B2%D8%A7%D9%85%22%7D&contacts=%5B%7B%22id%22%3A%226dffa198-05b9-407f-b56f-187ccc17a33d%22%2C%22role%22%3Anull%2C%22type%22%3A%22tel%22%2C%22title%22%3Anull%2C%22value%22%3A%22%2B982155556666%22%2C%22fullname%22%3A%22%D8%A7%D8%B5%D8%BA%D8%B1%20%D8%AA%D8%B1%D9%82%D9%87%22%7D%2C%7B%22id%22%3A%22ce60ac6d-f63a-4a3e-9d87-a7c5e53321bf%22%2C%22role%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%D8%B9%D8%A7%D9%85%D9%84%22%2C%22type%22%3A%22mobile%22%2C%22title%22%3A%22%D8%A7%D8%B5%D9%84%DB%8C%22%2C%22value%22%3A%22%2B982123422342%22%2C%22fullname%22%3Anull%7D%5D&type=corporate'
```
> Example Response:

```json

```
