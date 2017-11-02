# scala-eval

## Description
Use a web microservice framework of your choosing to produce a service that proxies gif requests to Giphy. A GET call will need to identify a user and a query to retrieve a random gif from giphy's API. The service will cache this result and not return the same gif for the same query again. A seperate POST will clear the cache for a unique user so that the gif can be returned again. 

This is a take home eval but should only take a few hours. If you're interested, stretch to using a file based RDBMS and akka. If you're uncomfortable doing this, I recommmend hitting the requirments 100% rather than attempt areas you may be weak in. Please unit and mock test both commands fully.

## Requirements
* Use sbt build a web microservice. 
* Add a GET that will search giphy (https://developers.giphy.com) for a query and return random image.
  * Json response `{ url: URL, desc: String }`
* Add a POST to reset cache for a unique user.
  * Json response `{ itemsCleared: Int }`
* Store images in a cache for each unique user.
* Only return images that haven't been seen before.
* Use Futures.
* Tests and mock tests using framework of your choice.

### Stretch
* Use a file RDBMS as persistent cache (like sqlite or h2)
* Akka

## Delivery
Please submit a zip that can be executed with `sbt run`.
