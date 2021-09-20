
This lesson shows you how to make a single request for the location of a device using the getLastLocation() method in the fused location provider. 


 # Choose the best location estimate

The FusedLocationProviderClient provides several methods to retrieve device location information. Choose from one of the following, depending on your app's use case:

_getLastLocation()_ gets a location estimate more quickly and minimizes battery usage that can be attributed to your app. However, the location information might be out of date, if no other clients have actively used location recently.

_getCurrentLocation()_ gets a fresher, more accurate location more consistently. However, this method can cause active location computation to occur on the device

This is the recommended way to get a fresh location, whenever possible, and is safer than alternatives like starting and managing location updates yourself using requestLocationUpdates(). If your app calls _requestLocationUpdates()_, your app can sometimes consume large amounts of power if location isn't available, or if the request isn't stopped correctly after obtaining a fresh location.