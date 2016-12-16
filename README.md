# Python Client for Google Maps Services

Use Python? Want to geocode something? Looking for directions? Maybe matrices of directions? This library brings the Google Maps API Web Services to your Python application. 

The Python Client for Google Maps Services is a Python Client library for the following Google Maps APIs:

<br/>
> [Directions API](https://developers.google.com/maps/documentation/directions/)

Help your users find their way.
Return multi-part directions for a series of waypoints. Directions for several modes of transportation are available.

![Direction API](https://github.com/gamboabdoulraoufou/google-maps-API/blob/master/direction.png)
<br/>

> [Distance Matrix API](https://developers.google.com/maps/documentation/distancematrix/)

Retrieve duration and distance values based on the recommended route between start and end points.

![Distance MAtrix](https://github.com/gamboabdoulraoufou/google-maps-API/blob/master/distance_matrix.png)
<br/>

> Elevation API

The Google Maps Elevation API provides elevation data for all locations on the surface of the earth, including depth locations on the ocean floor (which return negative values).

```sh 
# Request
https://maps.googleapis.com/maps/api/elevation/json?locations=39.7391536,-104.9847034&key=YOUR_API_KEY

# Response
{
   "results" : [
      {
         "elevation" : 1608.637939453125,
         "location" : {
            "lat" : 39.73915360,
            "lng" : -104.98470340
         },
         "resolution" : 4.771975994110107
      }
   ],
   "status" : "OK"
}

``` 

> Geocoding API

Geocoding is the process of converting addresses (like a street address) into geographic coordinates (like latitude and longitude), which you can use to place markers on a map, or position the map.

Reverse geocoding is the process of converting geographic coordinates into a human-readable address. The Google Maps Geocoding API's reverse geocoding service also lets you find the address for a given place ID.

```sh  
# Request
https://maps.googleapis.com/maps/api/geocode/json?address=1600+Amphitheatre+Parkway,+Mountain+View,+CA&key=YOUR_API_KEY

# Response
{
   "results" : [
      {
         "address_components" : [
           ...
         ],
         "formatted_address" : "1600 Amphitheatre Parkway, Mountain View, CA 94043, USA",
         "geometry" : {
            "location" : {
               "lat" : 37.4224764,
               "lng" : -122.0842499
            },
            "location_type" : "ROOFTOP",
            ...
         },
         "place_id" : "ChIJ2eUgeAK6j4ARbn5u_wAGqWA",
         "types" : [ "street_address" ]
      }
   ],
   "status" : "OK"
}

```


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

- _Snap to roads_: This service returns the best-fit road geometry for a given set of GPS coordinates. This service takes up to 100 GPS points collected along a route, and returns a similar set of data with the points snapped to the most likely roads the vehicle was traveling along.  
- _Nearest roads_: This service returns individual road segments for a given set of GPS coordinates. This services takes up to 100 GPS points and returns the closest road segment for each point. The points passed do not need to be part of a continuous path.
- _Speed limits_: This service returns the posted speed limit for a road segment. 

> Places API

- _Location Awareness_: 
Use the power of mobile to give your users contextual information about where they are, when they’re there.

- _Search Everywhere_:
Search for and retrieve rich information about local businesses and points of interest, available on every screen.

- _Autocomplete_:
Add autocomplete to any application, providing type-ahead location-based predictions like the search on Google Maps.
