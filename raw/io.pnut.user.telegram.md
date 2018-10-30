<!-- give your raw a title -->
# Telegram User

<!-- specify the "type" for your raw -->
> ### io.pnut.user.telegram

<!-- provide a description of what your raw represents -->
The Telegram raw is meant to specify the username of the user on the messaging service Telegram.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ js
{
    "type": "io.pnut.user.telegram",
    "value": {
        "username": "pnutio",
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field         | Required? | Type   | Description                                                 |
| -----         | --------- | ----   | -----------                                                 |
| username      | Required  | string | A valid username pointing to the Telegram users' username   |

<!-- provide a way to contact you -->
## Maintainers
* @rafaelcosta

<!-- provide references to compatible apps / service -->
## Used by
* [Arachis](https://itunes.apple.com/br/app/arachis/id1200781062?mt=8)