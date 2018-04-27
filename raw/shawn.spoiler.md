<!-- give your raw item a title -->
# Spoiler Alert / Block

<!-- specify the "type" for your raw item -->
> ### shawn.spoiler

<!-- provide a description of what your raw represents -->
Clients can tell that the post or message contains a [spoiler alert](https://www.wordnik.com/words/spoiler%20alert), and display the topic without displaying the post contents.

Optionally, an `expired_at` timestamp tells the client that after specified date, it is no longer considered a spoiler.

Clients could offer users "Do not hide this topic" for the rest of a session when dismissing a spoiler alert.

<!-- provide at least one example of what your raw might look like in the wild -->
## Example

~~~ json
{
    "type": "shawn.spoiler",
    "value": {
        "topic": "Star Trek: DS9",
        "expired_at": "2018-04-27T13:02:56Z"
    }
}
~~~

<!-- provide a complete description of the fields in the "value" object for your raw -->
## Fields

|Field|Required?|Type|Description|
|-----|---------|----|-----------|
|topic|Required|string|An un-escaped, one-line description of what is being talked about. Recommended max length of 128 characters.|
|expired_at||string|Optional ISO 8601 timestamp after which the topic will no longer be spoiled by the post or message.|

<!-- provide a way to contact you -->
## Maintainers
* @33MHz

<!-- provide references to compatible apps / service -->
## Used by
* 
