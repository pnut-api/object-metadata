# Movie review

> ### io.aya.movie.review

This is for embedding movie reviews in messages. 

This raw object is typically attached to a message posted in the Movie Club channel (#591), but it can be attached to any message posted in any chat room.

It is required to provide the movie's title, release date, rating, review and TMDb id (see https://www.themoviedb.org/documentation/api).

It is highly recommended to also provide the original title if the movie is foreign (the main title is US-centric), and to provide a link to the movie's IMDb page. 

If a movie poster is available, it is recommended to include a public URL of the image. Other optional fields should not be omitted if the data is publicly available.

A message where this raw is attached must present a formatted representation of the data.

## Examples

### Complete

~~~ js
{
    "io.aya.movie.review": [
        {
            "title": "the US film title",
            "original_title": "the original title for foreign films",
            "imdb_url": "the link to the film's IMDb page",
            "rating": 4.5,
            "release_date": "1973-08-14",
            "tmdb_id": 334246,
            "review": "the film's review",
            "director": ["director1"],
            "cast": ["actor1", "actor2", "actor3", "actor4", "actor5"],
            "poster_url": "the link to the film's poster"
        }
    ]
}
~~~

### Minimal

~~~ js
{
    "io.aya.movie.review": [
        {
            "title": "the US film title",
            "rating": 2,
            "release_date": "2020",
            "review": "the film's review",
            "tmdb_id": 334246
        }
    ]
}
~~~

## Fields

| Field | Required? | Type | Description |
| ----- | --------- | ---- | ----------- |
| `type` | Required  | string | "io.aya.movie.review" |
| `title` | Required  | string | The US film title. |
| `rating` | Required  | float | Between 0 and 5 by steps of 0.5. |
| `release_date` | Required  | string | Recommended: "year-month-day". Acceptable: "year"  |
| `review` | Required  | string | The film's review. |
| `tmdb_id` | Required  | int | The film's id given by the TMDb API. |
| `original_title` | Optional  | string | The original title for foreign films. |
| `imdb_url` | Optional  | string | The link to the film's IMDb page. |
| `director` | Optional  | string[] | The director(s)' name(s). |
| `cast` | Optional  | string[] | The main cast. Include at least one name. Recommended: four or five. |
| `poster_url` | Optional  | string | The public link to the film's poster image. |

## Maintainers

- [@ericd](https://pnut.io/@ericd)

## Used by

- MovieNut