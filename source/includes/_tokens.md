# Tokens

## Get token 
> Definition:

```curl
GET ttp://echon.io/v1/token
```
> Example Request:

```curl
curl -X POST \
  http://echon.io/v1/token \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: c1d78ff1-8c9d-1294-9ebe-de8ba895e00a' \
  -d 'grantType=password&clientId=57f986e1-4588-4512-90ea-d264904df7b2&username=crm%40fidilio.com&password=12312312'
```
> Example Response:

```json
{
    "token": "2faafd13b0f64a388c57de929a8b6a54X5WC3JRlQrwgi36N2QsTyKBLiOJwcfiJNvfnUlUHMaHDUvcP6211ls2BFqj35UnCQ2kxltWBTul0dK2MNC5rBRWoJ9GGhIXfq4YLB57rloXwRci5QmSJK7EtZMjuFDC9nmQnwaoSGtL9r9A5P85vma508eaiYcJunNTJw0m0QkLJWEKOmiTUbm0I4vUbUro2GqsiX2d5vm58IRg6VO8LVZgC27UbYNcA",
    "refreshToken": "d2261e5419784567b67b5f3bc4f3960aFlBu7lDlskBweSERxqD1U8rjHKEqkfZGYzY33HJ5jeANF1PQlF3eDLMOB76XOwEK3t9943GKD1VGKHUf9X4rH1mWZjJIUfs6LTTIbkP3qBz3m7Udm7InqNArvs2F9eXbeYiSAcF2AEapxqK35SBgqB6ZmIbHcUWkRKBJftoDEOUjR08CgDK7RUFoSn5k4qZOD6wxBBXOkpZKFUOAXX3Jahl5I7Yk50nP",
    "expiresIn": 3600
}
```


## Refresh token
> Definition:

```curl
POST ttp://echon.io/v1/refresh/token
```
> Example Request:

```curl
curl -X POST \
  http://echon.io/v1/refresh/token \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: fc7e8ba1-7c0c-750d-5dfb-2c8437be645d' \
  -d 'refreshToken=d2261e5419784567b67b5f3bc4f3960aFlBu7lDlskBweSERxqD1U8rjHKEqkfZGYzY33HJ5jeANF1PQlF3eDLMOB76XOwEK3t9943GKD1VGKHUf9X4rH1mWZjJIUfs6LTTIbkP3qBz3m7Udm7InqNArvs2F9eXbeYiSAcF2AEapxqK35SBgqB6ZmIbHcUWkRKBJftoDEOUjR08CgDK7RUFoSn5k4qZOD6wxBBXOkpZKFUOAXX3Jahl5I7Yk50nP&='
```
> Example Response:

```json
{
    "token": "856cf6fd223041c79ad22b11f26b2cb9OaP12ciaOL9JHEiS549gyqHfqbrWFB2w98jMbUKvGAW528ArixNaSi2q6H9K2SUZdgsJazSOEIw7qvcBXGUCkS3k1L8w6kWMlMclJt8Xk9Dnx5ZYeysCr1XNYqUbchGG1Oe3pySl1muemvnlYyATwDWNvn8S2uuIvzzfZKV5Ku9yPaygD20ccW2bUzvOakBwXZZB10TFTiJ9q4Ax8XKguLpvmOoqXNGa",
    "refreshToken": "a5435b1e056947c2853a23adfffdfdb4x5tBaWG4n0n3xUlPqzeI0aHrr0xzmhd3YFrkgIBLjHXmNisUWB0vQryVnFHOE21LZPenwcWKumY1R9Iy4OY7CEJf6RYWECDQkOUciD1l2SLYx8D3TODXZ15LwXFhTbQKoSQFKs6MFg204x05gq93LyRztyFbE4tmwpVn0DP0nGt1bNqK0sHM6Iz3DkSfPxUnl9znOOLq3BFtA1HmmnCauDhaDFmYad4x",
    "expiresIn": 3600
}
```

