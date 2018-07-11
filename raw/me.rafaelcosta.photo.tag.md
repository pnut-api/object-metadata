<!-- give your raw item a title -->
# Photo Tags

<!-- specify the "type" for your raw item -->
> ### me.rafaelcosta.photo.tag

<!-- provide a description of what your raw item represents -->
This is meant to add support for user tagging inside photos, and can be used on any platform.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ js
{
    "type":"me.rafaelcosta.photo.tag",
    "value": {
        "version": "1.0",
        "attached_to_type" : "url",
        "ref" : "https://i.imgur.com/abcdef.jpg",
        "tags" : [{
            "user_id"  : "47",
            "location" : {
                "x" : "10",
                "y" : "40",
                "w" : "100",
                "h" : "120",
            },
          }, {
            "user_id" : "1",
            "location" : {
                "x" : "400",
                "y" : "40",
                "w" : "100",
                "h" : "120",
            },
          }, {...},
        ],
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw item -->
## Fields

| Field         | Required? | Type   | Description                                                    |
| -----         | --------- | ----   | -----------                                                    |
| version       | Required  | string | Version Number. Currently, only 1.0 exists                     |
| attached_to_type   | Required  | `file` or `url` | Specifies if this raw object refers to a file or an URL |
| ref           | Required  | string | A reference URL/File ID. This spec only provides the tagging, so clients should check if the post has an oembed with this URL/File ID      |
| tags          | Required  | object | The object that provides the tags                              |

### Tag Object

| Field         | Required? | Type   | Description                                                    |
| -----         | --------- | ----   | -----------                                                    |
| user_id       | Required  | string | The user_id in the tagged picture                              |
| username      | Required  | string | The username in the tagged picture                             |
| location      | Required  | object | The position of the tagged face. This assumes that the picture's top-left is the point (0,0). Therefore, the x and y refer to it (x being the horizontal distance in pixels from x=0; and y being the vertical distance in pixels from y=0). Width (w) and height (h) are the width and height of the face.                           |

## Visual example

<img src="/images/olympia_tagged.png" alt="alt text" width="350">

<!-- provide a way to contact you -->
## Maintainers
* Rafael ([@rafaelcosta](https://pnut.io/@rafaelcosta))

<!-- provide references to compatible apps / service -->
## Used by
* None so far

<!-- provide references to related annotations -->
## Related annotations
* It is *require* to include the photo part as oembed image, this spec only intends to add tagging support, not to change how oembeds work :)
