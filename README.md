# Magellan Maperitive Render Rules

Ruleset for [Maperitive](http://maperitive.net/), with high-contrast color scheme for tourism and mapping.

The ruleset was developed for using with the Magellan Triton / Explorist GPS for several purposes: tourism, traveling and for cartographic use, gathering data and [OSM](http://www.openstreetmap.org/) editing. The generated tiles also can be used with other devices and smartphones. For example in the [OsmAnd](http://osmand.net/) app.

## Features

* Support for the latest and rare OSM tags: `natural=gully`, `natural=earth_bank`, `natural=valley`, `waterway=drystream`, `leisure=resort`, `amenity=social_facility`, `exit=no` and `fixme=continue` at the end of the road, `drinking_water=yes/no` for springs.
* The high contrast, increased lines and font thickness for convenient outdoor use in GPS.
* Color scheme is based on the original style of Magellan GPS vector maps.

## Screenshots

![A](/Screenshots/a.png?raw=true)
![B](/Screenshots/b.png?raw=true)
![C](/Screenshots/c.png?raw=true)

## Map creation for Magellan Triton/Explorist

* Download [Maperitive](http://maperitive.net) and install it.
* Add files from Magellan style to Maperitive directory.
* Load and apply Magellan rules with the command line:

```
use-ruleset location=Rules/Magellan.mrules as-alias=magellan
apply-ruleset
```

* Generate tiles using the `generate-tiles` command. e.g. for 13-17 zooms:
```
generate-tiles minzoom=13 maxzoom=17
```

* Create a Magellan RMP map file using [Mobile Atlas Creator](http://mobac.sourceforge.net/). Use [custom source script](http://mobac.sourceforge.net/wiki/index.php/Custom_XML_Map_Sources) for local tiles:

```
<?xml version="1.0" encoding="UTF-8"?>
<localTileFiles>
	<name>Maperetive</name>
	<sourceFolder>C:\Maperitive\Tiles</sourceFolder>
	<backgroundColor>#000000</backgroundColor>
</localTileFiles>
```

The map size should not be more than 18000 to 18000 pixels (for Triton).

* Transfer RMP maps to the GPS device through [VantagePoint](http://www.magellangps.com/Store/VantagePoint_Software/VantagePoint).

## Credits + Licence

Rules based on default rendering rules for [Maperitive](http://maperitive.net), created by Igor Brejc, Updated by Michael <quelbs_at_gmail.com>

Released under the [Creative Commons Attribution-ShareAlike 3.0 License](http://creativecommons.org/licenses/by-sa/3.0/)

Icons used: Map icons CC-0 from [SJJB Management](http://www.sjjb.co.uk/mapicons)
