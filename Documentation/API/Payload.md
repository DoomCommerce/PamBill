
# Payload

<br>

```ts
interface Payload {

    DATA_FORMAT : Format
    VERSION : Version
    ACTION : Action
    DATA : Data

    CHECKSUM : string
    CALL_ID : string
    ORIGIN : string
    TOKEN : string
}
```

<br>
<br>

## Version

Possible values : `1.0`

<br>

## Action

Possible values : `import`

<br>

## Token

The 32 character long public token of the credentials.

<br>

## Format

Determines the format of the `DATA` property.

| Format | Description
|:------:|:------------
| `pambill` | [Custom PamBill specific import format][Format PamBill].
| `shopify` | Takes all the data it can get from **[Shopify Orders][Format Shopify]**.

<br>

## Call Id

Unique 32 character long nonce to prevent replay attacks.

Characters : `/^[0-9A-Z_]{32}$/i`

<br>

## Checksum

Hash calculated from the payload , secret and a nonce.

1.  Stringify the `DATA` as json

2.  Strip the following characters from it:

    -   Square & Curly Brackets

    -   Single & Double Quotes

    -   Backslashes

    -   Spaces

3.  Hash the stripped Json with SHA1

4.  Concatenate the hash , secret & call-id

5.  Finally hash the combined string

<br>

## Origin

Identifier of the system using the API.

Characters : `/^[0-9A-Z_]{3,32}$/i`

Example : `My_Invoice_App`

<br>

## Action

What action to take on PamBill.

| Action | Description
|:------:|:------------
| `import` | Import one or more orders to PamBill.

<br>


<!----------------------------------------------------------------------------->

[Format Shopify]: https://shopify.dev/docs/api/admin-rest/2023-07/resources/order
[Format PamBill]: https://www.pambill.com/pambill-api
