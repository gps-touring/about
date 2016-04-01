# about
About the gps-touring project.

## Background

This project stems from the experience of touring by bicycle, with navigation using an iPhone running the ViewRanger app. The way I do this at the moment is outlined here:

- Grab some GPX files directly from the web - easily obtained for most of the major cycle routes in Europe.
- Plan other sections using Google Maps, and the excellent [gpsvisualizer](http://www.gpsvisualizer.com/) to convert Google's routes into GPX.
- Download GPX files containing POIs for campsites (e.g. from http://www.archiescampings.eu/).
- Load the route GPX files into http://my.viewranger.com/, ready for loading into the iPhone app.
- Load the POI GPX files (for campsites) into the iPhone ViewRanger app via dropbox.

## Problems

The above process works OK, but there are some problems, or at least opportunities to make things better:

- Large GPX files will slow the ViewRanger app. 
- GPX files can be difficult to find on the ViewRanger app (by the side of the road in the rain!) if there are tens (or more) of them downloaded to the Viewranger app.
- ViewRanger strips elevation data from the GPX files (you can get at elevation data from the VIewRanger app if you use certain paid-for maps - so not with OpenCycleMap).
- During the afternoon, I'll check to see which campsites might be reachable by the evening. This is a largely manual process, with some assistance (e.g. crows-flight distance from current location) from ViewRanger. This process could be improved.

## Solutions

The aim of this project is to provide software to solve these problems:

- Gather together all source GPX files for the route.
- Generate new GPX files, of limited size (to imprive ViewRanger performance), and with a sensible naming convention to make it easier to find the files.
- Provide planning information about campsites (or any other point of interest (POI) that may be visited).
- Recognize GPX routes that are alternatives (e.g. a detour to a POI).
- Provide planning information that heeds the elevation data in the GPX files. (Going up hill on a bike is much harder than going downhill!). e.g. estimated number of days for a journey, with a day-by-day breakdown.
- Trim GPX files for POIs so that they contain only those POIs within reach of the route. For example, an original POI GPX file of campsites may contain all campsites for an entire country - thousands - this will make the ViewRanger app go very slowly.
- Remove redundant points from GPX route files. Many downloaded from the web have redundant information, e.g. a track point recorded every N seconds, even when stationary.
