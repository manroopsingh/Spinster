# Spinster(Bike Sharing Android Application)

[![Build Status](https://travis-ci.org/bparmentier/Spinster.svg?branch=master)](https://travis-ci.org/bparmentier/Spinster)

Spinster is an Android application that displays the availability of shared bikes in your
city.

It uses the [CityBikes API](http://api.citybik.es/v2/) that provides data for more than 400 cities in around 40 countries and displays this data in a list or on an [OpenStreetMap](https://www.openstreetmap.org) layer
thanks to the [osmdroid](https://github.com/osmdroid/osmdroid) library (multiple layers are available).

### Translations

Translations are managed on [Weblate](https://hosted.weblate.org/). Please follow [these instructions](https://hosted.weblate.org/engage/Spinster/) if you want to help.

## Build

If you use Android Studio, you can import the project directly from GitHub.

Otherwise you can build it from the command line with
[Gradle](https://developer.android.com/sdk/installing/studio-build.html).  
Clone the repo and type:

    ./gradlew build

(You may need to `chmod +x` the `gradlew` script)

The Gradle script will take care of downloading the necessary libraries and will generate the APK's
in `app/build/outputs/apk`.

## Permissions

The following permissions are needed by Spinster (those are the same that are required by
osmdroid):

* ACCESS_COARSE_LOCATION
* ACCESS_FINE_LOCATION
* ACCESS_WIFI_STATE
* ACCESS_NETWORK_STATE
* INTERNET
* WRITE_EXTERNAL_STORAGE

Internet access is needed to download the map tiles and the stations. Location access is only used
to locate you on the map. Access to the SD card is required by osmdroid to cache the tiles.
