<!-- give your raw item a title -->
# Channel Avatar Image

<!-- specify the "type" for your raw item -->
> ### io.pnut.core.channel.avatar

<!-- provide a description of what your raw represents -->
This raw item provides an avatar image for a channel, similar to an avatar image for a user. The dimensions of this image must be 200x200.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ js
{
    "io.pnut.core.channel.avatar": [
        {
            "+io.pnut.core.file": {
                "file_token": "abcdefg",
                "format": "metadata",
                "file_id": "8"
            }
        }
    ]
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field         | Required? | Type   | Description                                                 |
| -----         | --------- | ----   | -----------                                                 |
| +io.pnut.core.file | Required  | object | A file replacement object. Format must be `metadata`, and the image must be 200x200 pixels. |

<!-- provide a way to contact you -->
## Maintainers
* @33MHz

<!-- provide references to compatible apps / service -->
## Used by
* 