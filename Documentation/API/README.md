
# API Concept

>   [!NOTE]
>   Only very little of the functionality found on the  
>   website can be done through the public API endpoint.

<br>

## Notes

-   There currently is only one version / revision of the API ( `1.0` )

-   There is only one endpoint `https://www.pambill.com/api`

-   All requests are sent as `POST` requests with `JSON` payload

-   You require both the token & secret to use the API

<br>

```ts
async function example (){
    
    const payload = {
        DATA_FORMAT : 'pambill' ,
        CHECKSUM : '18fb1a7619e9420b9fea96f19c588f4a5083165d' ,
        CALL_ID : 'a7f2a7bec9754f2bab9f833adc1b40ac' ,
        VERSION : '1.0' ,
        ORIGIN : 'My_App' ,
        ACTION : 'import' ,
        TOKEN : 'c8d07a88a6994f949c9142d792b479f9' ,
        DATA : [{}]
    }

    const response = await fetch(`https://pambill.com/api`,{

        headers : { 'Content-Type' : 'application/json' } ,
        method : 'POST' ,
        body : JSON.stringify(payload)

    })
}
```

<br>
