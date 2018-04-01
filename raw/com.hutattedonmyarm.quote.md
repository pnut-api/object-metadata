<!-- give your raw item a title -->
# Quote

<!-- specify the "type" for your raw item -->
> ### com.hutattedonmyarm.quote

<!-- provide a description of what your raw item represents -->
This is for embedding quotes into posts. Clients can use this info to highlight embedded quotes.
This leans onto the [Entities](https://pnut.io/docs/api/implementation/entities) field of posts. 
The quote text (and optionally source text) itself is part of the posttext, and the RAW contains metadata. 
Position and lengths are all multibyte (UTF-32) code points (just like entities).
Optionally, the quote text itself can be added to the raw, but if doen so it must be identical to the quote text within the post.
Optionally a source can be added to the raw. This source can be part of the post text (if so, specify the position and length).
It can also be a link to the source or author of the quote, either in addition or instead of the source_pos/source_len field.

source_pos and source_len are also optional and should be added if the source of the quote is plain text part of the post text, e.g. "Oscar Wilde".
source_url is optional and can be set if the origin of the quote is not named in the post text or if it is named, but you want to provide more detail.

Optionally a filler position and length can be specified to tell a client to hide fillers between the quote and the source, e.g. " by ", or " - ".
If quotation marks are present, they should be counted as parts of the quote.


<!-- provide at least one example of what your raw might look like in the wild -->
## Examples
Post:
~~~
"Nobody has the intention of building a wall" - Walter Ulbricht
~~~
Raw (source with additional info):
~~~ js
{
    "type":"com.hutattedonmyarm.quote",
    "value": {
        "pos": 0,
        "len": 45,
        "source_pos": 48,
        "source_len": 15,
        "source_url": "https://en.wikipedia.org/wiki/Walter_Ulbricht",
        "filler_pos": 45,
        "filler_len": 3
    }
}
~~~
Post:
~~~
Baz: "Shut up, baz!"
~~~
Raw (minimum):
~~~ js
{
    "type":"com.hutattedonmyarm.quote",
    "value": {
        "pos": 5,
        "len": 15
    }
}
~~~
Raw (source text plus link):
~~~ js
{
    "type":"com.hutattedonmyarm.quote",
    "value": {
        "pos": 5,
        "len": 15,
        "source_pos": 0,
        "source_len": 3,
        "source_url": "https://beta.pnut.io/posts/207139"
    }
}
~~~
Raw (only link to source):
~~~ js
{
    "type":"com.hutattedonmyarm.quote",
    "value": {
        "pos": 5,
        "len": 15,
        "source_url": "https://beta.pnut.io/posts/207139"
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw item -->
## Fields

| Field         | Required? | Type   | Description                                                      |
| -----         | --------- | ----   | -----------                                                      |
| pos           | Required  | int    | Zero-indexed starting position of the quote within the post text |
| len           | Required  | int    | Length of the quote                                              |
| source_pos    |           | int    | The position of the origin string                                |
| source_len    |           | int    | The length of the origin string                                  |
| source_url    |           | String | URL of the quote                                                 |
| filler_pos    |           | int    | The position of the filler string                                |
| filler_len    |           | int    | The length of the filler string                                  |

<!-- provide a way to contact you -->
## Maintainers
* Max ([@hutattedonmyarm](https://pnut.io/@hutattedonmyarm))

<!-- provide references to compatible apps / service -->
## Used by
* None so far
