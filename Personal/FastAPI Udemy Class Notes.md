# Complete Backend (API) Development with Python A-Z (Udemy FastAPI class)

General REST API and FAST API notes. Not all are from class, and not everything in class is in here.


> The 5 HTTP Status code levels - first number and topic
>> - 1XX - Informative
>> - 2XX - Success
>> - 3XX - Redirection
>> - 4XX - Client Error
>> - 5XX - Server Error

> HTTP Status code 200
>> - 200 - OK

> HTTP Status code 201
>> - 201 - Created

> HTTP Status code 204
>> - 204 - No Content (like when you are deleting something)

> HTTP Status code 400
>> - 400 - Bad request

> HTTP Status code 401
>> - 401 - Unauthorized

> HTTP Status code 403
>> - 403 - Forbidden 

> HTTP Status code 404
>> - 404 - Not found

> HTTP Status code 405
>> - 405 - Invalid input

> HTTP Status code 409
>> - 409 - Conflict

> 401 (unauthorized) vs 403 (forbidden) HTTPS response
>> 401 Unauthorized: If the request already included Authorization credentials, then the 401 response indicates that authorization has been refused for those credentials. 403 Forbidden: The server understood the request, but is refusing to fulfill it

> Map 5 HTTP methods to CRUD
>> - POST - Create
>> - GET - Read
>> - PUT and PATCH - Update
>> - DELETE - Delete

> Difference betewwn PUT and PATCH HTTP methods
>> - PUT - updates ALL of the target resource
>> - PATCH - PARTIAL modification of target resource


> Two main parts of REST API in action
>> - Request
>> - Response

> In rest API what does the URL represent
>> The request

> For parts of the REST API request
>> - Endpoint (the "path" or "resource", everything before the `?` in the URL)
>> - Method - HTTP method (`GET`, `POST`, `PUT`, `DELETE`)
>> - Headers
>> - Data, aka Body (might not be needed on `DELETE`?)

> Should REST API endpoints be verbs or nouns?
>> Nouns

> 5 types of parameters in REST API
>> - Query - `myapi.com/user?name=chuck`
>> - Path - `myapi.com/user/chuck`
>> - Body (not for GET since GET doesn't have a request body)
>> - Header 
>> - Cookie 

> In Fast API what should the default value of a parameter be to indicate that it is optional?
>> `None` or `fastapi.Query(None)`

> In Fast API how do you make a querry parameter required?
>> Don't give it a default value or use `Query` with `...` (Python Ellipsis) as first argument, ex `fastapi.Query(..., min_length=3)`

> Fast API optional string parameter `name` in get function `get_user`
>> ```py
>> from fastapi import FastAPI
>> from typing import Optional
>> app = FastAPI()
>> @app.get("/user/")
>> async def get_user(name: Optional[str] = None):
>>   return {"name": name}
>> ```
>> Note: Fast API doesn't care about `Optional`, that is just for editor

> Fast API - validate query parameter string for min/max length and regex with default of `None`
>> `Query(None, min_length=3, max_length=50, regex="^fixedquery$")` Note: this combination of validation parameters doesn't make much sense, it's just an example


