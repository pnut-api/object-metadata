<!-- give your raw a title -->
# Embedded Poll

<!-- specify the "type" for your raw -->
> ### io.pnut.core.poll-notice

<!-- provide a description of what your raw represents -->
The embedded poll raw specifies a poll object that should be displayed with this post.

The embed will not include up-to-date results for the poll. The client would have to fetch the poll separately. This only gives an overview and the `poll_token` and `poll_id` combo that may be necessary to retrieve the full poll.

<!-- provide at least one example of what your raw might look like in the wild -->
## Examples

### Photo

~~~ js
{
    "type": "io.pnut.core.poll-notice",
    "value": {
        "prompt": "What is your main \"computer\"?",
        "poll_token": "7m_SG07ZbfhG1kNbfnMJl4ZDO15ioqt9",
        "closed_at": "2018-05-19T14:52:46Z",
        "poll_id": "132",
        "options": [
            {
                "text": "Desktop Mac",
                "position": 1
            },
            {
                "text": "Desktop PC",
                "position": 2
            },
            {
                "text": "Laptop Mac",
                "position": 3
            },
            {
                "text": "Laptop PC",
                "position": 4
            },
            {
                "text": "Tablet",
                "position": 5
            },
            {
                "text": "Other",
                "position": 6
            }
        ]
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields 
**To correspond with the oEmbed spec, this raw accepts keys that are not specified below.**

| Field | Required? | Type | Description |
| ----- | --------- | ---- | ----------- |
| `prompt` | Required  | string | The time at which the poll was created in ISO 8601 format. |
| `poll_token` | Required | string | A token to access and respond to the poll. |
| `closed_at` | Required | string | The time at which the poll closes in ISO 8601 format. |
| `poll_id` | Required | string | Primary identifier for a poll. |
| `options` | Required | list | A list of 2 to 10 responses for the poll. `text` and `position` will be set for each. |

<!-- provide a way to contact you -->
## Maintainers
* ([@33MHz](https://pnut.io/@33mhz), [support@pnut.io](mailto:support@pnut.io))

<!-- provide references to compatible apps / service -->
## Used by
* 

<!-- provide references to related raws -->
## Related raw
* 