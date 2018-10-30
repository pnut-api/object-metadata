<!-- give your raw a title -->
# Homepage

<!-- specify the "type" for your raw -->
> ### io.pnut.user.homepage

<!-- provide a description of what your raw represents -->
The homepage raw is meant to specify the homepage of the user on the world wide web.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ js
{
    "type": "io.pnut.user.homepage",
    "value": {
        "url": "http://pnut.io",
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field         | Required? | Type   | Description                                    |
| -----         | --------- | ----   | -----------                                    |
| url           | Required  | string | A valid URL pointing to the users' homepage    |

<!-- provide a way to contact you -->
## Maintainers
* @rafaelcosta

<!-- provide references to compatible apps / service -->
## Used by
* [ChimPnut](https://itunes.apple.com/us/app/chimpnut-microblog-pm-chat/id1198300163?mt=8)
* [Arachis](https://itunes.apple.com/br/app/arachis/id1200781062?mt=8)