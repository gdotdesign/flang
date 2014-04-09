# XMLHTTPRequests
Requests are core parts of the langagues.

## Syntax
Requests are using the `@` token followed by one of: **get**, **post**, **put**, **delete**, **patch** followed by an **url** [(expression)](expressions.md) then a **request-block**.

```
@get '/users' {
  @withCredentials;

  @headers {
    ContentType: aapplication/json;
  }

  parameter1: value;
  parameter2: value2;

  ~ success { ... }
  ~ error { ... }
}
```

## Request Block
The request block is a special block that can contain:
  * **directives** - Such as *@headers* and *@withCredentials*
  * **key-value pairs** - The data to be sent represented as key-value pairs
  * **events** - Such as success and error
