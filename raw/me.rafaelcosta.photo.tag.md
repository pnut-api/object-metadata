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
        "ref" : "https://i.imgur.com/abcdef.jpg",
        "tags" : [{
            "username" : "rafaelcosta",
            "position" : "x,y,w,h",
          }, {
            "username" : "33MHz",
            "position" : "x,y,w,h",
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
| ref           | Required  | string | A reference URL. This spec only provides the tagging, so clients should check if the post has an oembed with this URL      |
| tags          | Required  | object | The object that provides the tags                              |

### Tag Object

| Field         | Required? | Type   | Description                                                    |
| -----         | --------- | ----   | -----------                                                    |
| username      | Required  | string | The username in the tagged picture                             |
| position      | Required  | string | The position of the tagged face. This assumes that the picture's top-left is the point (0,0). Therefore, the x and y refer to it (x being the horizontal distance in pixels from x=0; and y being the vertical distance in pixels from y=0). Width (w) and height (h) are the width and height of the face.                           |

## Visual example

<img src="/images/olympia_tagged.png" alt="alt text" width="350">
<!-- ![Olympia Tagged](/images/olympia_tagged.png) -->

<!-- provide a way to contact you -->
## Maintainers
* Rafael ([@rafaelcosta](https://pnut.io/@rafaelcosta))

<!-- provide references to compatible apps / service -->
## Used by
* None so far

<!-- provide references to related annotations -->
## Related annotations
* It is *require* to include the photo part as oembed image, this spec only intends to add tagging support, not to change how oembeds work :)
