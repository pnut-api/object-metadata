<!-- give your raw a title -->
# Twitter User

<!-- specify the "type" for your raw -->
> ### io.pnut.user.twitter

<!-- provide a description of what your raw represents -->
The Twitter raw is meant to specify the username of the user on the website Twitter.com.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ js
{
    "type": "nl.chimpnut.user.facebook",
    "value": {
        "username": "pnutio",
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field         | Required? | Type   | Description                                                 |
| -----         | --------- | ----   | -----------                                                 |
| username      | Required  | string | A valid username pointing to the Facebook users' username    |

<!-- provide a way to contact you -->
## Maintainers
* @rafaelcosta (?)

<!-- provide references to compatible apps / service -->
## Used by
* [ChimPnut](https://itunes.apple.com/us/app/chimpnut-microblog-pm-chat/id1198300163?mt=8)
* [Arachis](https://itunes.apple.com/br/app/arachis/id1200781062?mt=8)