<!-- give your raw a title -->
# External User Profiles

<!-- specify the "type" for your raw -->
> ### me.rafaelcosta.user.profiles

<!-- provide a description of what your raw represents -->
This raw lists a user's external profiles.

By convention, these are common options, but users or clients can specify their own also:

```
pnut
homepage
blog
twitter
whatsapp
telegram
facebook
mastodon
micro.blog
```

_Signal was removed from a previous attempt at this specification because they do not support URL schemes ATM._

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ js
{
    "type": "me.rafaelcosta.user.profiles",
    "value": {
        "profiles": [
            {
                "service": "signal",
                "id": "+12223334444"
            },
            {
                "service": "telegram",
                "id": "rafaelcosta"
            },
            {
                "service": "facebook",
                "id": "thisthat444"
            },
            {
                "service": "facebook",
                "id": "thatthis444",
                "text": "Work"
            },
            {
                "service": "blog",
                "url": "https://example.com"
            },
            {
                "service": "homepage",
                "url": "https://example.com"
            }
        ]
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

| Field         | Required? | Type   | Description                                                 |
| -----         | --------- | ----   | -----------                                                 |
| service       | Required  | string | The service hosting the profile |
| id            | Optional  | string | ID of the user. If not provided, clients can assume there is nothing to parse but the `url` to a website |
| url           | Optional  | string | If no `id` is provided, this is required. Otherwise optional. |
| text          | Optional  | string | Should supplement any profile handle or service name, not replace it |

<!-- provide a way to contact you -->
## Maintainers
* @rafaelcosta
* @33MHz
* @ludolphus

<!-- provide references to compatible apps / service -->
## Used by
* [ChimPnut](https://itunes.apple.com/us/app/chimpnut-microblog-pm-chat/id1198300163?mt=8)
* [Arachis](https://itunes.apple.com/br/app/arachis/id1200781062?mt=8)