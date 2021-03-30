<!-- give your raw a title -->
# Fallback URL

<!-- specify the "type" for your raw -->
> ### net.patter-app.broadcast

<!-- provide a description of what your raw represents -->

If a client has an issue or does not know how to display a content type, this fallback URL can be used to point users to the best experience for it. E.g., if you add special raw material to a message or post, your app may be the only one to fully display that content properly.

<!-- provide at least one example of what your raw might look like in the wild -->
## Examples

~~~ js
{
    "io.pnut.core.fallback_url": [
        {
            "url": "https://beta.pnut.io/messages/18"
        }
    ]
}
~~~

The API will check for a valid URL.

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field | Required? | Type | Description |
| ----- | --------- | ---- | ----------- |
| `url` | Required | string | A valid link to a standard site for the content. |

<!-- provide a way to contact you -->
## Maintainers
* ([@33MHz](https://pnut.io/@33mhz), [support@pnut.io](mailto:support@pnut.io))

<!-- provide references to compatible apps / service -->
## Used by
* 

<!-- provide references to related raws -->
## Related raw
* 