
# Errors

Errors are returned when validation or authorization  
failed as well as when an API limit is reached.

<br>

```json
{
    "STATE" : "ERROR" ,

    "ERROR" : {
        "MESSAGE" : "" ,
        "ERROR" : ""
    }
}
```

<br>
<br>

## Responses

```ts
interface TooManyRequests {
    MESSAGE : ''
    CODE : 'ERR_API_TOO_MANY_REQUESTS'
}
```

```ts
interface RequestTooLarge {
    MESSAGE : `${ number }kb max`
    CODE : 'ERR_API_REQUEST_TOO_BIG'
}
```

```ts
interface TooManyEntities {
    MESSAGE : ''
    CODE : 'ERR_API_TOO_MANY_DATA_ENTITIES'
}
```

```ts
interface DuplicateRequest {
    MESSAGE : 'CALL_ID must be unique for each request'
    CODE : 'ERR_API_DUPLICATED_REQUEST'
}
```

```ts
interface InvalidChecksum {
    MESSAGE : ''
    CODE : 'ERR_API_CHECKSUM_INCORRECT'
}
```

```ts
interface UnsupportedAction {
    MESSAGE : 'Supported ACTION values are: import'
    CODE : 'ERR_API_ACTION_NOT_SUPPORTED'
}
```

<br>
