# Python Client for Google Maps Services

Use Python? Want to geocode something? Looking for directions? Maybe matrices of directions? This library brings the Google Maps API Web Services to your Python application. Analytics

The Python Client for Google Maps Services is a Python Client library for the following Google Maps APIs:

Directions API
Distance Matrix API
Elevation API
Geocoding API

> Time Zone AP

The Google Maps Time Zone API provides time offset data for locations on the surface of the earth. You request the time zone information for a specific latitude/longitude pair and date. The API returns the name of that time zone, the time offset from UTC, and the daylight savings offset.

```sh
# Request
https://maps.googleapis.com/maps/api/timezone/json?location=38.908133,-77.047119&timestamp=1458000000&key=YOUR_API_KEY

# Response
{
   "dstOffset" : 3600,
   "rawOffset" : -18000,
   "status" : "OK",
   "timeZoneId" : "America/New_York",
   "timeZoneName" : "Eastern Daylight Time"
}
``` 

> Roads API

The Google Maps Roads API allows you to map GPS coordinates to the geometry of the road, and to determine the speed limit along those road segments. The API is available via a simple HTTPS interface, and exposes the following services:

- Snap to roads This service returns the best-fit road geometry for a given set of GPS coordinates. This service takes up to 100 GPS points collected along a route, and returns a similar set of data with the points snapped to the most likely roads the vehicle was traveling along. Optionally, you can request that the points be interpolated, resulting in a path that smoothly follows the geometry of the road.
- Nearest roads This service returns individual road segments for a given set of GPS coordinates. This services takes up to 100 GPS points and returns the closest road segment for each point. The points passed do not need to be part of a continuous path.
- Speed limits This service returns the posted speed limit for a road segment. The Speed Limit service is only available to Google Maps APIs Premium Plan customers. If you are an existing customer, you can contact your account manager or file a ticket in the Premium Plan support portal to enable the Google Maps Roads API.

Places API
