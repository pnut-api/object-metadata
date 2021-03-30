# Poll

<!-- specify the "key" for the replacement value -->
> ### +io.pnut.core.poll

<!-- provide a description of the replacement value -->
This dynamically inserts information about a Pnut.io [Poll](http://pnut.io/docs/resources/poll/) into `raw`. The poll information is merged with any other values to form a single object.
Easily attach a poll to a post or message, using a "replacement value". By including the following example as a `raw` item, the API will replace the values given with relevant details from a poll stored in the API.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

#### Provided to Pnut.io
~~~ js
{
    "io.pnut.core.poll-notice": [
        {
            "+io.pnut.core.poll": {
                "poll_token": "12345abcde",
                "poll_id": "1",
            },
            "other_values": "are preserved"
        }
    ]
}
~~~

#### Returned by API
~~~ js
{
    "io.pnut.core.poll-notice": [
        {
            "poll_token": "12345abcde",
            "id": "1",
            "prompt": "This is a poll?",
            "closed_at": "2018-03-24T01:00:00Z",
            "options": [
                {
                    "text": "Looks like it",
                    "position": "1"
                },
                {
                    "text": "Fake news",
                    "position": "2"
                }
            ].
            "other_values": "are preserved"
        }
    ]
}
~~~


<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field | Required? | Type | Description |
| ----- | --------- | ---- | ----------- |
| `poll_token` | Required | string | A valid poll token that Pnut.io returned when you created a poll.|
| `poll_id` | Required | string | The id of the poll. |

<!-- provide a way to contact you -->
## Maintainers
* [@33MHz](https://beta.pnut.io/@33mhz)

<!-- provide references to compatible apps / service -->
## Used by
* 

<!-- provide references to related raws -->
## Related raws
* 
