## Coursera - Building Cloud Services with the Java Spring Framework

This assignment is a very basic application
for uploading video to a cloud service and managing the video's metadata and its content.
This covers the core knowledge needed to create much more sophisticated cloud services.
There are four HTTP APIs in this:
 
GET /video
   - Returns the list of videos that have been added to the
     server as JSON.
     
POST /video
   - The video metadata is provided as an application/json request
     body. The JSON generates a valid instance of the 
     Video class when deserialized by Spring's default 
     Jackson library.
   - Returns the JSON representation of the Video object that
     is stored along with any updates to that object made by the server. 

GET /video/{id}
   - Returns the video with the given id or 404 if the video is not found.
     
POST /video/{id}/like
   - Allows a user to like a video. Returns 200 Ok on success, 404 if the
     video is not found, or 400 if the user has already liked the video.
     
POST /video/{id}/unlike
   - Allows a user to unlike a video that he/she previously liked. Returns 200 OK
      on success, 404 if the video is not found, and a 400 if the user has not 
      previously liked the specified video.

GET /video/search/findByName?title={title}
   - Returns a list of videos whose titles match the given parameter or an empty
     list if none are found.
    
GET /video/search/findByDurationLessThan?duration={duration}
   - Returns a list of videos whose durations are less than the given parameter or
     an empty list if none are found.

