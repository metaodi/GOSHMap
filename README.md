[Versión en español](leer.md)

# Welcome to the Open Science Hardware collaborative Map!

[**The Map**](http://u.osmfr.org/m/255581/) 

This initiative aims to build a collaborative database -and map- of open hardware projects around the world. It started with projects from Latin America as part of my [PhD](https://thessaly.github.io/phd/) and now we want to make it global as part of the [Global Open Source Hardware](https://openhardware.science) community. 

We're discussing the specifics of the map in [this thread](https://forum.openhardware.science/t/map-cadastre-list-of-open-science-hardware-initiatives-in-chile-latam/835/3), in case you want to check the latest news. It's still 'work in progress'.


### How does it work?

The database is contained in a .csv file you'll find in this repo, called [openhwmap.csv](https://github.com/thessaly/OpenHWMap/blob/master/openhwmap.csv).

Users can collaborate by generating pull requests to this file, that are reviewed and merged. 

The .csv file is then converted to a map by [Umap](http://umap.openstreetmap.fr), based on [Open Street Map](http://openstreetmap.org).


### How to collaborate?

If you know about an open hardware project (or maybe it's your own project!) that isn't listed in our map, do the following:

#### 1. [Fork](https://help.github.com/articles/fork-a-repo/) this repo

#### 2. Add the project info to **openhwmap.csv** 

A comma-separated values (CSV) file stores tabular data (numbers and text) in plain text. Each line of the file is a data record (in our case, each row is an open hardware project). Each record consists of one or more fields, separated by commas. 

So you just need to edit the file, go to the last row and add another row, with the following format:

##### > fields
`latitude,longitude,geometry,name,GOSH,status,type,url`

##### > example
`-31.4116703,-64.2315674,Point,"AlterMundi - Redes libres comunitarias",n,active,Non-academic,http://altermundi.net`

##### > data required

Up to now, we're requiring the following data for each Open Hardware project:

```
latitude: in decimal values    

longitud: in decimal values
```

If you don't have the coordinates for your point, you can easily obtain them by going to [GeoJSON.io](http://geojson.io), selecting the marker tool (A), creating a point (B) and copy&pasting the data (C) as follows (**IMPORTANT**: note that you have to enter the latitude value **first** and then the longitude value in the csv, but geojson.io gives you the values **the other way round**) 

![coordinates](/screenshots/coordinates.png) 

```
geometry: by default, value is always 'Point'    

name: name of the project    

GOSH: this field admits two different values - 'y'/'n'  
  y= this project is part of the GOSH community
  n= this project is not part of the GOSH community   

status: this field admits two different values - 'active'/'inactive'    
  active= project had some activity going on during the last year    
  inactive= there's been no activity in the project for the last year    

type: this field admits four different values - 'academic'/'non-academic'/'artist'/'business'    
  academic= depending on university or research institution    
  non-academic= outside academia community project   
  artist= independent or collective artists    
  business= for profit developments    

url: website, repo, a reference url where to find more about the project    
```

#### 3. Create a [pull request](https://help.github.com/articles/creating-a-pull-request-from-a-fork/)

#### 4. Wait for it to be approved and merged into the main file (won't take long, promise!)
