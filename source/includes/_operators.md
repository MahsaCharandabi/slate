# Operators

## The operator object

```curl

```
> The above command returns JSON structured like this:

```json

```

## Create an operator

```curl
curl -X POST \
  http://echon.io/v1/operators \
  -H 'authorization: bearer 88fe8d1a6cfd408eba29b4c000427a7cH0NbzXX20ViFrGjfbPaiN57W4C8o73dzHKPrc561EDlqDJbLmTVmSJem86ueEMzcThuj89n4Ld1HHB8dGU72ojvwJakuFNKI3VBhFkhAHfi8pgl2icCyTkklcmwQ266tq4lHLsjanv9raufhP4gxWbvT6StWth8DGfDEJEC9AWLk5fbHNu2xFFLKE64sXgKGkm3MGVOtrTfDj1XTadcpG5uPbulDxoFz' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: b9359e7c-b727-7c7b-827e-19caeab78411' \
  -d 'firstName=%D9%81%D8%B1%D8%B2%D8%A7%D9%85&lastName=%D8%AE%D8%AC%D8%B3%D8%AA%D9%87&email=hi%40far077za3m.me&password=123&actions=%7B%22test%22%3Atrue%2C%22editCustomer%22%3Atrue%2C%22createCustomer%22%3Atrue%2C%22deleteCustomer%22%3Atrue%2C%22manageOperators%22%3Afalse%2C%22accessToTimeline%22%3Atrue%2C%22configOrganization%22%3Atrue%2C%22manageApplications%22%3Atrue%2C%22allowedEventTypesSlugsForAddToTimeline%22%3A%7B%22contracts%22%3Atrue%2C%22email%22%3Atrue%2C%22sms%22%3Afalse%2C%22telegram%22%3Afalse%2C%22note%22%3Atrue%7D%2C%22allowedEventTypesSlugForViewInTimeline%22%3A%7B%22contracts%22%3Atrue%2C%22email%22%3Atrue%2C%22sms%22%3Afalse%2C%22telegram%22%3Afalse%2C%22hasat%22%3A%22reza%22%7D%7D&='
```
> The above command returns JSON structured like this:

```json

```


## Retrieve an operator

```curl
curl -X GET \
  http://echon.io/v1/operators/c7e94231-e6a7-4826-adf0-e9e626d0c486 \
  -H 'authorization: bearer 88fe8d1a6cfd408eba29b4c000427a7cH0NbzXX20ViFrGjfbPaiN57W4C8o73dzHKPrc561EDlqDJbLmTVmSJem86ueEMzcThuj89n4Ld1HHB8dGU72ojvwJakuFNKI3VBhFkhAHfi8pgl2icCyTkklcmwQ266tq4lHLsjanv9raufhP4gxWbvT6StWth8DGfDEJEC9AWLk5fbHNu2xFFLKE64sXgKGkm3MGVOtrTfDj1XTadcpG5uPbulDxoFz' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 147ddb11-cf59-75db-8ca4-c1f609d1a1ae' \
  -d metaTags=%5B%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22firstName%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22test%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D8%AA%D8%B3%D8%AA%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22lastName%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%20%D8%AE%D8%A7%D9%86%D9%88%D8%A7%D8%AF%DA%AF%DB%8C%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22title%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D8%B9%D9%86%D9%88%D8%A7%D9%86%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22name%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22test%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%20%D9%BE%D8%AF%D8%B1%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Atrue%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22manager%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Atrue%2C%22defaultValue%22%3A%22%22%7D%5D
```
> The above command returns JSON structured like this:

```json

```

## Update an operator

```curl
curl -X PUT \
  http://echon.io/v1/operators/c7e94231-e6a7-4826-adf0-e9e626d0c486 \
  -H 'authorization: bearer 88fe8d1a6cfd408eba29b4c000427a7cH0NbzXX20ViFrGjfbPaiN57W4C8o73dzHKPrc561EDlqDJbLmTVmSJem86ueEMzcThuj89n4Ld1HHB8dGU72ojvwJakuFNKI3VBhFkhAHfi8pgl2icCyTkklcmwQ266tq4lHLsjanv9raufhP4gxWbvT6StWth8DGfDEJEC9AWLk5fbHNu2xFFLKE64sXgKGkm3MGVOtrTfDj1XTadcpG5uPbulDxoFz' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 5f8a1f32-e710-678f-faea-0f3447ebbcfd' \
  -d actions=%7B%22test%22%3Atrue%2C%22editCustomer%22%3Atrue%2C%22createCustomer%22%3Atrue%2C%22deleteCustomer%22%3Atrue%2C%22manageOperators%22%3Afalse%2C%22accessToTimeline%22%3Atrue%2C%22configOrganization%22%3Atrue%2C%22manageApplications%22%3Atrue%2C%22allowedEventTypesSlugsForAddToTimeline%22%3A%7B%22contracts%22%3Atrue%2C%22email%22%3Atrue%2C%22sms%22%3Afalse%2C%22telegram%22%3Afalse%2C%22note%22%3Atrue%7D%2C%22allowedEventTypesSlugForViewInTimeline%22%3A%7B%22contracts%22%3Atrue%2C%22email%22%3Atrue%2C%22sms%22%3Afalse%2C%22telegram%22%3Afalse%2C%22hasat%22%3A%22reza%22%7D%7D
```
> The above command returns JSON structured like this:

```json

```

## Delete an operator

```curl
curl -X DELETE \
  http://echon.io/v1/operators/1a2a9733-c4d7-4f8c-81c4-b8b7628232b1 \
  -H 'authorization: bearer 85791972e14b4461b1cf736b646766c5O0jvDDwQEDx1xqFGoZo3MZHQhUnk0HSNLWym0WwIfUStsMUCpLvmwCGRLOXomEECodQbDMdP4dkxu2FI3CMIhsA0fD2OWYQXiuBGpausWsJm6NfwRx1GAAJbOTJFkImqmG2IBGZrE9uKbx4pdmg7VQU8r5Notfk5I2IrOLraPPPN4AxCWpXDvAe8aGDewMqDx0Ll9PNdJbzM6Aoj18P5bVz9V7mmwjUP' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 697e4f8d-180b-42dd-9eb9-c9e21ed7c08b' \
  -d 'firstName=%D9%81%D8%B1%D8%B2%D8%A7%D9%85&lastName=%D8%AE%D8%AC%D8%B3%D8%AA%D9%87&email=hi%40farzam.me&password=123&actions=%7B%22editCustomer%22%3Atrue%2C%22createCustomer%22%3Atrue%2C%22deleteCustomer%22%3Atrue%2C%22manageOperators%22%3Afalse%2C%22accessToTimeline%22%3Atrue%2C%22configOrganization%22%3Atrue%2C%22manageApplications%22%3Atrue%2C%22allowedEventTypesSlugsForAddToTimeline%22%3A%7B%22contracts%22%3Atrue%2C%22email%22%3Atrue%2C%22sms%22%3Afalse%2C%22telegram%22%3Afalse%7D%2C%22allowedEventTypesSlugForViewInTimeline%22%3A%7B%22contracts%22%3Atrue%2C%22email%22%3Atrue%2C%22sms%22%3Afalse%2C%22telegram%22%3Afalse%7D%7D'
```
> The above command returns JSON structured like this:

```json

```

## List all operators

```curl
curl -X GET \
  http://echon.io/v1/operators \
  -H 'authorization: bearer 41d7404c0c3e4f7abe39591559250c67j07Pm1ij05b9TPNGTxXmB8bsXVriHBxCuYjyiFvEsDq6PRx6oLmX1f73ZAEDuDnkqhRBwAVIuR0dbVrNybnTV27tQRADMsy05mm9oW2BpVYnxp6RFRtN130BegjhSaxb6hLHf72AJQksALxgHM2nDky1BcXVy2SGciQshEIncmXtfELNKHgbEZn5vdcTb2kGShyHI8TMYX5oIBb0ycL0hvStSjaIiV69' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 2a176854-7f0d-38d0-d100-549987949fb2' \
  -d metaTags=%5B%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22firstName%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22test%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D8%AA%D8%B3%D8%AA%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22lastName%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%20%D8%AE%D8%A7%D9%86%D9%88%D8%A7%D8%AF%DA%AF%DB%8C%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22title%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D8%B9%D9%86%D9%88%D8%A7%D9%86%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22name%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%22%2C%22readonly%22%3Atrue%2C%22allowNull%22%3Afalse%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22personal%22%2C%22slug%22%3A%22test%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%86%D8%A7%D9%85%20%D9%BE%D8%AF%D8%B1%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Atrue%2C%22defaultValue%22%3A%22%22%7D%2C%7B%22for%22%3A%22corporate%22%2C%22slug%22%3A%22manager%22%2C%22type%22%3A%22string%22%2C%22title%22%3A%22%D9%85%D8%AF%DB%8C%D8%B1%22%2C%22readonly%22%3Afalse%2C%22allowNull%22%3Atrue%2C%22defaultValue%22%3A%22%22%7D%5D
```
> The above command returns JSON structured like this:

```json

```

