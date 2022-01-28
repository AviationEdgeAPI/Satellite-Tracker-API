# Satellite Tracker API
Aviation Edge Satellite Tracker API provides provides detailed, real-time position and relevant data of satellites and objects orbiting around the Earth. The API covers real-time position information as well as many other details about the satellite itself such as name, NORAD ID, launch year, size, country of origin, and more. The position data updates constantly which allows building virtual maps for websites or apps as well as tracking and analyzing the movement of these objects.

[Get your API key](https://aviation-edge.com/premium-api/) in a minute and start testing the data right away. The API is provided through API subscriptions. All plans grant access to the Future Schedules API and other APIs with a difference of the monthly API call limit. Choose the best plan for you and upgrade, downgrade or cancel your plan anytime without  commitments.

### Documentation
You may find input parameters, output examples with explanations for each item, filter list, and more in the [documentation](https://aviation-edge.com/developers/).

### Example Fields of Use
- Virtual 2D/3D maps or websites, tools, apps for tracking space objects in real-time
- Tracking popular aerospace products such as SpaceX satellites or the International Space Station
- Orbiting object analysis based on country of origin, speed, quantity, launch year, size and more.

### Request 
All on-orbit satellite information in one call:

**GET** http://aviation-edge.com/v2/public/satelliteDetails?key=[API_KEY]&limit=30000

Individual satellites based on NORAD number:

**GET** http://aviation-edge.com/v2/public/satelliteDetails?key=[API_KEY]&code=408

Satellites based on launch year:

**GET** http://aviation-edge.com/v2/public/satelliteDetails?key=[API_KEY]&launchYear=1961

Individual satellites based on international designator (NSSDC ID) number:

**GET** http://aviation-edge.com/v2/public/satelliteDetails?key=[API_KEY]&intldes=1961-015EH

Filtering based on orbital apogee and perigee:

**GET** http://aviation-edge.com/v2/public/satelliteDetails?key=[API_KEY]&orbitalapogee=1035

**GET** http://aviation-edge.com/v2/public/satelliteDetails?key=[API_KEY]&orbitalperigee=939

### Response
```
[
{
"code":408,
"country":"US",
"intldes":"1961-015EH",
"launchDate":"1961-06-29",
"launchNum":"15",
"launchPart":"EH",
"launchYear":"1961",
"name":"THOR ABLESTAR DEB",
"orbitalApogee":"1035",
"orbitalInclination":"66.79",
"orbitalPerigee":"929",
"orbitalPeriod":"104.73",
"result":{
"ECI":{
"posX":0.5454890369,
"posY":-0.2586148768,
"posZ":-0.9850851542,
"velX":0.0575062685,
"velY":0.0304486006,
"velZ":0.0232874073},
"geography":{
"alt":1006.4047009328,
"lat":-58.6467050931,
"lon":129.4707358377},
"satelliteInfo":{
"classification":"U",
"idLaunchNumber":"015",
"idLaunchPiece":"EH ",
"idLaunchYear":"61",
"orbit":99888,
"rightAscension":21.7828,
"satnumber":408}
},
"size":"MEDIUM",
"tle1":"1 408U 61015EH 20129.79820524 -.00000021 +00000-0 +54301-4 0 9997",
"tle2":"2 408 066.7883 021.7828 0070545 199.3274 220.5694 13.74946678998881",
"type":"DEBRIS",
"updated":1589063274000
}
]
```

### Questions & Support
[Contact us](https://aviation-edge.com/contact/) via email for any questions or support requests.

### License
The use of the API is subject to Aviation Edge [Terms and Conditions](https://aviation-edge.com/api-terms-of-service/).
