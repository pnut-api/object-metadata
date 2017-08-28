<!-- give your raw item a title -->
# Chat Room Settings

<!-- specify the "type" for your raw item -->
> ### io.pnut.core.chat-settings

<!-- provide a description of what your raw item represents -->


<!-- provide at least one example of what your raw item might look like in the wild -->
## Example

~~~ js
{
    "type":"io.pnut.core.chat-settings",
    "value": {
        "name": "Frederick's Music Lounge",
        "description": "A musical interlude for music-lovers",
        "categories": ["community"]
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw item -->
## Fields

| Field         | Required? | Type   | Description                                                    |
| -----         | --------- | ----   | -----------                                                    |
| name          | Required  | string | Name of the chat room.  |
| description   | Optional  | string | Description of the chat room. Up to 256 bytes. |
| categories    | Optional  | list of strings | Up to three categories. Options are `fun, lifestyle, profession, language, community, tech, event, general`. |

<!-- provide a way to contact you -->
## Maintainers
* [@33MHz](https://pnut.io/@33mhz)

<!-- provide references to compatible apps / service -->
## Used by
* [Patter](https://patter.chat)
* [Patter for iOS](https://itunes.apple.com/us/app/patter/id600033550?ls=1&mt=8)
* [ChimPnut](https://itunes.apple.com/us/app/chimpnut/id1198300163?ls=1&mt=8)
* [Arachis](https://itunes.apple.com/br/app/arachis/id1200781062?mt=8)

<!-- provide references to related raw items -->
## Related raw items
