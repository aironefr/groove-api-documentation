# TrackActionResult (JSON)   


The object describing a track action result, used by add and delete.

It contains the input ID (the ID provided in the request), the resulting ID (for example, if the track was added to the collection, we generate an ID for it), and an optional error field if the action failed.

##TrackActionResult


The TrackActionResult object has the following specification.

| **Member** | **Type** | **Description**                                                                                         |
|------------|----------|---------------------------------------------------------------------------------------------------------|
| Error      | Error    | Optional. Null if the operation succeeded; otherwise, contains information on why the operation failed. |
| InputId    | string   | ID provided by the caller's request.                                                                    |
| Id         | string   | ID generated by the service (null in case of a delete).                                                 |

##Sample JSON syntax
```json
{
   "InputId": "music.873FB507-0100-11DB-89CA-0019B92A3933",
   "Id": "music.AQQfLejCjRp0CUSXL6Ksx2WU6Ae1P4cAAQ"
}
```
##See also


#### Parent

[Groove Service REST Reference](Groove%20Service%20REST$20Reference.md)