<!-- give your raw item a title -->
# Photo Tags

<!-- specify the "type" for your raw item -->
> ### io.pnut.core.phototag

<!-- provide a description of what your raw item represents -->
This is meant to add support for user tagging inside files (photos) uploaded to Pnut.io, and can be used on any platform.
One should be added per user.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ js
{
    "type":"io.pnut.core.phototag",
    "value": {
        "version"             : "1.0",
        "+io.pnut.core.user"  : "47",
        "x"                   : "10",
        "y"                   : "40",
        "w"                   : "100",
        "h"                   : "120",
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw item -->
## Fields

| Field         | Required? | Type   | Description                                                    |
| -----         | --------- | ----   | -----------                                                    |
| version       | Required  | string | Version Number. Currently, only 1.0 exists                     |
| +io.pnut.core.user   | Required  | string | Specifies the user ID that tag refers to. Special replacement value |
| x             | Required  | number | A number that has the x coordinates of the tagged user         |
| y             | Required  | number | A number that has the y coordinates of the tagged user         |
| w             | Required  | number | A number that has the width coordinates of the tagged user     |
| h             | Required  | number | A number that has the height coordinates of the tagged user    |

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
* This is meant to be attached to files, not posts
