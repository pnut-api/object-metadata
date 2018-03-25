# File

<!-- specify the "key" for the replacement value -->
> ### +io.pnut.core.file

<!-- provide a description of the replacement value -->
This dynamically inserts information about a Pnut.io [File](http://pnut.io/docs/resources/file/) into `raw`. The File information is merged with any other values to form a single object.
Easily attach a file to a post or message, using a "replacement value". By including the following example as a `raw` item, the API will replace the values given with relevant details from a file stored in the API.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

### `url` format

#### Provided to Pnut.io
~~~ js
{
    "type": "com.example.test",
    "value": {
        "+io.pnut.core.file": {
            "file_token": "12345abcde",
            "format": "url",
            "file_id": "1",
        },
        "other_values": "are preserved"
    }
}
~~~

#### Returned by API
~~~ js
{
    "type": "com.example.test",
    "value": {
        "file_token_read": "new_file_token",
        "file_id": "4",
        "url": "http://example.com/file_url.png",
        "url_expires": "2018-03-24T01:00:00Z",
        "other_values": "are preserved"
    }
}
~~~


### `metadata` format

#### Provided to Pnut.io

~~~ js
{
    "type": "com.example.test",
    "value": {
        "+io.pnut.core.file": {
            "file_token": "12345abcde",
            "format": "metadata",
            "file_id": "4",
        },
        "other_values": "are preserved"
    }
}
~~~

#### Returned by API

~~~ js
{
    "type": "com.example.test",
    "value": {
        "file_token_read": "new_file_token",
        "file_id": "1",
        "complete": true,
        "mime_type": "image/png",
        ...other File object values...
        "other_values": "are preserved"
    }
}
~~~


### `oembed` format

This format can only be used with the `io.pnut.core.oembed` raw, not with 3rd party raws.

#### Provided to Pnut.io

~~~ js
{
    "type": "io.pnut.core.oembed",
    "value": {
        "+io.pnut.core.file": {
            "file_token": "12345abcde",
            "format": "oembed",
            "file_id": "4",
        },
        "other_values": "are preserved"
    }
}
~~~

#### Returned by API

~~~ js
{
    "type": "io.pnut.core.oembed",
    "value": {
        "file_token_read": "new_file_token",
        "file_id": "4",
        "url_immediate": "https://...",
        "url_immediate_expires": "2019-04-01T01:00:00Z",
        "version": "1.0",
        "type": "photo",
        ...other oembed values...
        "other_values": "are preserved"
    }
}
~~~

In addition to the standard oembed fields, Pnut.io will also add fields for `file_token_read` and `file_id` to the oembed data. If the oembed data is not public, the oembed `url` field will expire at the time indicated in `url_expires`.

If the oembed data is public, `url` will be a permanent url which always redirects to the image. In this case, an additional field `url_immediate` will provide the current value for the file so you can avoid the redirect. (This expires at `url_immediate_expires`). `thumbnail_url` and `thumbnail_large_url` (described below) also use this same url patterns.

We generate `thumbnail_url` from the [`image_thumb_200s` derived file](http://developers.app.net/docs/resources/file/#derived-files). If the image is smaller than 200x200, then we use the image as its own thumbnail. If we have a larger derived file (`image_thumb_960r`), then we will also include `thumbnail_large_url`, `thumbnail_large_width`, `thumbnail_large_height`, etc that correspond to the larger thumbnail.

If the file has a [`io.pnut.core.oembed.metadata` raw](../raws/io.pnut.core.oembed.metadata.md), it will be used to generate the oembed output. We replace `poster_key`, `thumbnail_key`, and `url_key` fields with `poster_url`, `thumbnail_url`, and `url` fields containing links to the corresponding derived files. If a `_key` field is provided but left empty, we do the replacement with a link to the root file.

If you provide `provider_name`, `provider_url`, or `embeddable_url` along with the replacement value, your value will override the Pnut.io provided key. No other oembed keys can be overridden. For example:

~~~ js
{
    "type": "io.pnut.core.oembed",
    "value": {
        "+io.pnut.core.file": {
            "file_token": "12345abcde",
            "format": "oembed",
            "file_id": "1",
        },
        "provider_name": "My Cool App"
    }
}
~~~

gets translated to:

~~~ js
{
    "type": "io.pnut.core.oembed",
    "value": {
        "file_token_read": "new_file_token",
        "file_id": "1",
        "url_immediate": "https://...",
        "url_immediate_expires": "2012-01-01T01:00:00Z",
        "version": "1.0",
        "type": "photo",
        ...other oembed values...
        "provider_name": "My Cool App" # overridden by user
    }
}
~~~

#### URL Lifetimes

*To be added*

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field | Required? | Type | Description |
| ----- | --------- | ---- | ----------- |
| `file_token` | Required | string | A valid file token that Pnut.io returned when you uploaded a file.|
| `format` | Required | string | Either `metadata`, `oembed`, or `url` depending on what data you want provided for this file. |
| `file_id` | Required | string | The id of the file. |

<!-- provide a way to contact you -->
## Maintainers
* [@33MHz](https://beta.pnut.io/@33mhz)

<!-- provide references to compatible apps / service -->
## Used by
* [Beta](https://beta.pnut.io/)

<!-- provide references to related raws -->
## Related raws
* [io.pnut.core.oembed](../raw/io.pnut.core.oembed.md)
* [io.pnut.core.oembed.metadata](../raw/io.pnut.core.oembed.metadata.md)