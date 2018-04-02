<!-- give your raw item a title -->
# Quote

<!-- specify the "type" for your raw item -->
> ### com.hutattedonmyarm.quote

<!-- provide a description of what your raw item represents -->
This is for embedding quotes into posts. Clients can use this info to highlight embedded quotes.
This leans onto the [Entities](https://pnut.io/docs/api/implementation/entities) field of posts. 
The quote and itself is part of the posttext, and the raw contains additional info. 

It is required to set a display text of the source of the quote in `source_text`. If the name of the source is already present in the post text its position may be set with `source_pos` and `source_len`, so clients can visually highlight it if theey want.
The same applies to the quote text itself. Its position within the post text can be specified with `pos` and `len` to allow clients to visually distinguish it. To accomodate to the fact, that a quote may be split into two parts `pos` and `len` are arrays.

Optionally the creation date of the quote can be specified in `source_created_at`.

`source_url` optionally contains a link with further info (e.g. a pnut post, a wiki page, etc)

Position and lengths are all multibyte (UTF-32) code points (just like entities).
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
        "pos": [0],
        "len": [45],
        "source_pos": 48,
        "source_len": 15,
        "source_url": "https://en.wikipedia.org/wiki/Walter_Ulbricht",
        "source_text": "Walter Ulbricht",
        "source_created_at": "1961-08-13"
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
        "source_text": "@bazbt3"
    }
}
~~~
Raw (source only):
~~~ js
{
    "type":"com.hutattedonmyarm.quote",
    "value": {
        "source_pos": 0,
        "source_len": 3,
        "source_text": "@bazbt3"
    }
}
~~~
Post:
~~~
"What are you gonna do?", he asked, "stab me?"
~~~
Raw (split quote):
~~~ js
{
    "type":"com.hutattedonmyarm.quote",
    "value": {
        "pos": [0, 36],
        "len": [24, 10],
        "source_text": "Stabbed man"
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw item -->
## Fields

| Field             | Required? | Type   | Description                                                      |
| ----------------- | --------- | ----   | -----------                                                      |
| pos               |           | int[]  | Zero-indexed starting position of the quote within the post text |
| len               |           | int[]  | Length of the quote                                              |
| source_text       | Required  | String | The source (e.g. author name) of the quote                       |
| source_pos        |           | int    | Position of the source name if it is part of the post text       |
| source_len        |           | int    | Length of the source name if it is part of the post text         |
| source_url        |           | String | URL of the quote or additional details                           |
| source_created_at |           | Strin  | ISO 8601 time the quoted material was created                    |

<!-- provide a way to contact you -->
## Maintainers
* Max ([@hutattedonmyarm](https://pnut.io/@hutattedonmyarm))

<!-- provide references to compatible apps / service -->
## Used by
* None so far
