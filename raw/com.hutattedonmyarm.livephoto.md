<!-- give your raw item a title -->
# Live Photos

<!-- specify the "type" for your raw item -->
> ### com.hutattedonmyarm.livephoto

<!-- provide a description of what your raw item represents -->
This is meant to support Apple's 'Live Photos', and can be used on any platform.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ js
{
    "com.hutattedonmyarm.livephoto": [
        {
            "version": "1.0",
            "width": "1959",
            "height": "2048",
            "photo_url": "https://i.imgur.com/abcdef.jpg",
            "video_url": "https://somehost.com/abcdef.mov",
            "title": "A moving picture"
        }
    ]
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw item -->
## Fields

| Field         | Required? | Type   | Description                                                    |
| -----         | --------- | ----   | -----------                                                    |
| version       | Required  | string | Version Number. Currently, only 1.0 exists                     |
| width         |           | string | Width of the video and photo (needs to be identical)           |
| height        | Required  | string | Height of the video and photo (needs to be identical)          |
| photo_url     | Required  | string | URL of the still image. Must be a .jpg                         |
| video_url     | Required  | string | URL of the video. Must be a .mov                               |
| title         |           | string | Title of the live photo (if any)                               |

<!-- provide a way to contact you -->
## Maintainers
* Max ([@hutattedonmyarm](https://pnut.io/@hutattedonmyarm))

<!-- provide references to compatible apps / service -->
## Used by
* None so far

<!-- provide references to related annotations -->
## Related annotations
* It is recommended to include the photo part also as oembed image, so that clients without support for Live Photos can still display the still image.
