<!-- give your raw a title -->
# Crosspost

<!-- specify the "type" for your raw -->
> ### io.pnut.core.crosspost

<!-- provide a description of what your raw represents -->
The crosspost raw is meant to specify the original or canonical source of a post on pnut.io from somewhere else on the web.

Optional fields can clarify the originating service, if there is a relevant external service to link to, and the originating user from the external service. If referenced, clients can handle the crosspost raw similar to if the post or message were a "repost", where the client would display the user and service, and note the actual Pnut user that is crossposting it.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ json
{
    "type": "io.pnut.core.crosspost",
    "value": {
        "canonical_url": "https://twitter.com/pnutio/status/875679848903192576",
        "source": {
            "name": "Twitter",
            "url": "https://twitter.com"
        },
        "user": {
            "avatar_image": "https://pbs.twimg.com/profile_images/862301868910813184/H4iLmfZ4_bigger.jpg",
            "username": "pnutio"
        }
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field         | Required? | Type   | Description                                                 |
| -----         | --------- | ----   | -----------                                                 |
| canonical_url | Required  | string | A valid URL pointing to the source of the original content. |
| source.name   | Optional  | string | Name of the external service. |
| source.url    | Optional  | string | URL linking to the external service. |
| user.username | Optional  | string | Username of the originating username from external service. |
| user.avatar_image | Optional | string | A URL to an image of the originating user from external service. |

If including `source`, `name` and `url` are required.

<!-- provide a way to contact you -->
## Maintainers
* @33MHz

<!-- provide references to compatible apps / service -->
## Used by
* [Patter](https://patter.chat)
* [HTML](https://html.is)