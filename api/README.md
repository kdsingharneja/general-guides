APIs
====

A guide for designing APIs.

General
-------

* Prefer JSON based APIs as much as possible.
* Avoid XML payloads unless there is a technical need.
* Design APIs such that UI and consumers do not have to make multiple calls to make many calls.

JSON
----

* Use JSON for API request and response bodies.

REST
----

* Prefer RESTful "resources".
* Use the appropriate [HTTP verb].
* `GET`, `DELETE`, and `PUT` requests should be [idempotent].
* `GET` requests should have no side effects.

[HTTP verb]: http://www.restapitutorial.com/lessons/httpmethods.html
[idempotent]: http://www.restapitutorial.com/lessons/idempotency.html

Localization
------------

* Use the `Accept-Language` HTTP header.
* Localize data values on the client, not the server.
* Return date and times in [ISO-8601] format.

[ISO-8601]: https://en.wikipedia.org/wiki/ISO_8601

Errors
------

* Use the appropriate [HTTP status code] to indicate the error to the client.
* Include any applicable error messages in the response body:
```JavaScript
{
  errors: ["First name is required", "Date of birth is required"]
}
```
```JavaScript
{
  errors: ["This example just has one error, but we wrap it in 'errors' for consistency."]
}
```

[HTTP status code]: http://www.restapitutorial.com/httpstatuscodes.html