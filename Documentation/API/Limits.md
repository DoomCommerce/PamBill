
# Limitations

<br>

## Rate Limit

The number of requests per shop ( Token ) are limited to `100 / Minute`

Fails with [`ERR_API_TOO_MANY_REQUESTS`][Rate Limit]

<br>
<br>

## Size Limit

The size of the request body cannot exceed `64Mb`

Fails with [`ERR_API_REQUEST_TOO_BIG`][Size Limit]

<br>
<br>

## Entity Limit

The number of items in the `DATA` array cannot exceed `500`

Fails with [`ERR_API_TOO_MANY_DATA_ENTITIES`][Entity Limit]

<br>


<!----------------------------------------------------------------------------->

[Entity Limit]: ./Errors#Responses
[Size Limit]: ./Errors#Responses
[Rate Limit]: ./Errors#Responses
