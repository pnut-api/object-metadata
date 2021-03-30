<!-- give your raw a title -->
# Broadcast Notice

<!-- specify the "type" for your raw -->
> ### net.patter-app.broadcast

<!-- provide a description of what your raw represents -->

The broadcast notice should be attached to messages after creating a post with the same text. The post normally will have a `io.pnut.core.channel.invite` raw item on it, referencing the channel that it is being "broadcast" from.

This way, the post on Global will invite users into the channel, and the message in the channel will reference the broadcasted post, for clarity to channel members and reference for people directed there from outside.

<!-- provide at least one example of what your raw might look like in the wild -->
## Examples

~~~ js
{
    "net.patter-app.broadcast": [
        {
            "id": "348684",
            "url": "https://posts.pnut.io/348684"
        }
    ]
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field | Required? | Type | Description |
| ----- | --------- | ---- | ----------- |
| `id` | Required  | string | The ID of the post created on Global. |
| `url` | Optional | string | A valid link to the post. `https://posts.pnut.io/{id}` or `https://beta.pnut.io/{id}` are common options. |

<!-- provide a way to contact you -->
## Maintainers
* ([@33MHz](https://pnut.io/@33mhz), [support@pnut.io](mailto:support@pnut.io))

<!-- provide references to compatible apps / service -->
## Used by
* https://patter.chat

<!-- provide references to related raws -->
## Related raw
* 