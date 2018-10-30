<!-- give your raw a title -->
# Signal User

<!-- specify the "type" for your raw -->
> ### io.pnut.user.signal

<!-- provide a description of what your raw represents -->
The Signal raw is meant to specify the username of the user on the messaging service Signal.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ js
{
    "type": "io.pnut.user.signal",
    "value": {
        "phone": "+5511987654321",
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field         | Required? | Type   | Description                                                                      |
| -----         | --------- | ----   | -----------                                                                      |
| phone         | Required  | string | A valid phone number, with country codes pointing to the Signal users' account   |

<!-- provide a way to contact you -->
## Maintainers
* @rafaelcosta

<!-- provide references to compatible apps / service -->
## Used by
* [Arachis](https://itunes.apple.com/br/app/arachis/id1200781062?mt=8)