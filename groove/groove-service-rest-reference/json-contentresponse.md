---
title: ContentResponse JSON object | Groove Services
description:  Learn about ContentResponse JSON object in Groove Music API.
keywords: groove music, groove api, groove contentresponse json
author: sakley
ms.assetid: b5b18ec2-b0da-43d7-870d-833cabee265e 
---

# ContentResponse (JSON)   
Base object used in most APIs that return media content.

## ContentResponse
The ContentResponse object has the following specification.

| **Member** | **Type**                                                             | **Description**                                                                                                                                                                                                                                                                                                             |
|------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Error      | [Error](JSON-Error.md)                     | Optional error.                                                                                                                                                                                                                                                                                                             |
| Artists    | List of [Artist](JSON-Artist.md)           | A paginated list of Artists that matched the request criteria.                                                                                                                                                                                                                                                              |
| Albums     | List of [Album](JSON-Album.md)             | A paginated list of Albums that matched the request criteria.                                                                                                                                                                                                                                                               |
| Tracks     | List of [Track](JSON-Track.md)             | A paginated list of Tracks that matched the request criteria.                                                                                                                                                                                                                                                               |
| Playlists  | List of [Playlist](JSON-Playlist.md)       | A paginated list of Playlists that matched the request criteria.                                                                                                                                                                                                                                                            |
| Results    | List of [ContentItem](JSON-ContentItem.md) | A paginated list of ContentItems that matched the request criteria. These items are used for ordered lists mixing multiple types of content such as the [Spotlight](uri-get-spotlight.md) and [NewReleases](uri-get-new-releases.md) APIs. |
| Genres     | GenreList                                  | A list of string representing the different possible genres for a given locale. Used in the [Browse Genres](uri-get-genres.md) API.                                                                                                                                         |
| Culture    | string                                     | The culture used for processing the [Browse Genres](uri-get-genres.md) request, computed from Country and Language parameters, user authentication and/or geolocation.                                                                                                      |
| Activities | List of [Activity](JSON-Activity.md)       | A list of Activities representing the different possible activities for a given locale. Used in the [Browse Activities](uri-get-activities.md) API.                                                                                                                                         |
| Moods      | List of [Mood](JSON-Mood.md)               | A list of Moods representing the different possible moods for a given locale. Used in the [Browse Moods](uri-get-moods.md) API.                                                                                                                                         |
| Radios     | List of [Radio](JSON-Radio.md)             | A list of recently played radios. Retrieved from the [Recently Played Radios](uri-recently-played-radio.md) API.                                                                                                                                         |

## Sample JSON syntax
```json
{
  "Artists": {
    "Items": [
      {
        "Genres": [
          "Electronic / Dance"
        ],
        "Subgenres": [
          "Dance"
        ],
        "Id": "music.C61C0000-0200-11DB-89CA-0019B92A3933",
        "Name": "Daft Punk",
        "ImageUrl": "https://musicimage.xboxlive.com/content/music.C61C0000-0200-11DB-89CA-0019B92A3933/image?locale=en-US",
        "Link": "https://music.microsoft.com/Artist/C61C0000-0200-11DB-89CA-0019B92A3933?partnerID=AwesomePartner",
        "OtherIds": {
          "music.amg": "P   168791"
        },
        "Source": "Catalog",
        "CompatibleSources": "Catalog, Collection"
      }
    ]
  }
}
```

#### Parent
[Groove Service REST Reference](overview.md)
