<!-- give your raw item a title -->
# ChimPnut etc Long Posts

<!-- specify the "type" for your raw item -->
> ### nl.chimpnut.blog.post

<!-- provide a description of what your raw item represents -->
The longpost "raw" is meant to provide extended text for a Pnut post.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ js
{
    "type":"nl.chimpnut.blog.post",
    "value": {
        "body": "Dass es eine Webapplikation ist, macht dann aber \u00fcberhaupt keinen
         Sinn ;-) im Gegenteil: \"woher wei\u00df ich dass das nicht ausgelesen wird?\"
        ",
        "title": "",
        "tstamp": 1487171761002
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw item -->
## Fields

| Field         | Required? | Type   | Description                                                    |
| -----         | --------- | ----   | -----------                                                    |
| body          | Required  | string | Words. Many words. More words than 256 characters anyway.      |
| title         |           | string | Blog post title (if any).                                      |
| tstamp        | Required  | string | Microseconds since the UNIX Epoch 1st Jan. 1970.               |

<!-- provide a way to contact you -->
## Maintainers
* [SΤΞVΞΠ](http://yellowdice.com/) ([@ludolphus](https://pnut.io/@ludolphus))

<!-- provide references to compatible apps / service -->
## Used by
* [ChimPnut](https://itunes.apple.com/us/app/chimpnut/id1198300163?ls=1&mt=8)

<!-- provide references to related annotations -->
## Related annotations
