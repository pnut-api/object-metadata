<!-- give your raw a title -->
# Crosspost

<!-- specify the "type" for your raw -->
> ### io.pnut.core.crosspost

<!-- provide a description of what your raw represents -->
The crosspost raw is meant to specify the original or canonical source of a post on pnut.io from somewhere else on the web.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ js
{
    "type": "io.pnut.core.crosspost",
    "value": {
        "canonical_url": "https://twitter.com/pnutio/status/875679848903192576",
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field         | Required? | Type   | Description                                                 |
| -----         | --------- | ----   | -----------                                                 |
| canonical_url | Required  | string | A valid URL pointing to the source of the original content. |

<!-- provide a way to contact you -->
## Maintainers
* @33MHz

<!-- provide references to compatible apps / service -->
## Used by
* [Patter](https://patter.chat)