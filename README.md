# Global Open Science Hardware Map

[:es:](README_es.md)

This initiative aims to build a collaborative database of open science hardware projects around the world. It started with projects from Latin America as part of my [PhD](https://github.com/thessaly/phd/) and now we want to make it global as part of the [Global Open Source Hardware](https://openhardware.science) community. 

[**:earth_americas: Map**](http://tinyurl.com/y2ehx763)   

[**:heart: I want to contribute**](CONTRIBUTING.md)


### How does the map work?
The database of projects is publicly available in [Wikidata](https://www.wikidata.org) and displayed as a map through the [Wikidata Query Service](https://query.wikidata.org).

<details><summary><b>Why Wikidata?</b></summary>
<p>
In very very simple words, Wikidata is like Wikipedia but instead of writing articles you contribute to it with structured data. 

This means you can define your own data model, input data or import it from available sources and then use that same structure to search the database with the Query service. As part of the latter you can visualize results as a table, graph or map (if your data has geo coordinates).

[Database in table format](https://query.wikidata.org/#SELECT%20%3Fitem%20%3FitemLabel%20%3FlugarLabel%20%3FtipoLabel%20%3FareaLabel%20%3Fcoords%20WHERE%20%7B%0A%20%20%3Fitem%20wdt%3AP361%20wd%3AQ62391989%3B%0A%20%20%20%20%20%20%20%20wdt%3AP276%20%3Flugar%3B%0A%20%20%20%20%20%20%20%20wdt%3AP31%20%3Ftipo%3B%0A%20%20%20%20%20%20%20%20wdt%3AP366%20%3Farea.%0A%20%20%3Flugar%20wdt%3AP625%20%3Fcoords.%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%2Cen%22.%20%7D%0A%7D)     
[Example in graph format](/screenshots/graphgosh.png)    


The benefits I see from this approach are:    
- Anyone can contribute;
- Map is updated everytime you visit it;
- Easy to link with other sources of data (wikipedia articles, github repos, journal articles);
- Engagement with the bigger wikimedia community
- Small collaboration == big benefits - By linking our nodes with other info already in wikidata we get a bigger picture

There is a small possibility of vandalism, that's why I keep a periodic [backup](goshmap.csv) of the database in this same repo.

</details>

<details><summary><b>Data model</b></summary>
<p>
This is the minimum proposed structure that allows us to map projects that are part of GOSH community. It's made taking into account the available items (Q) and properties (P) defined by the Wikidata community. 

*Check an example here: [Monitor Abierto de Calidad de Aire (MACA)](https://www.wikidata.org/wiki/Q62395443)*

1. Node must be `instance of (P31)` one of the following:

- `project (Q170584)`
- `community (Q177634)`
- `university research group (Q28863779)`
- `business (Q4830453)`
- `institution (Q178706)`

2. Node must have statement `use (P366)` with one of the following values:

- `education (Q8434)`
- `art (Q735)`
- `academic research (Q62393045)`
- `community science (Q62392920)`

3. Node must have statement `field of work (P101)` with one of the following values or any other value available and useful:

- `microscopy	Q1074953`
- `biohacking	Q5205179`
- `unmanned aerial vehicle	Q484000`
- `microfluidics	Q138845`
- `transfeminism Q3308597`
- `air quality	Q56245086`
- `soil quality	Q2034420`
- `water quality	Q625376`
- `health Q12147`
- `physics	Q413`
- `sound	Q11461`
- `audiovisual	Q2431196`
- `textile	Q28823`
- `social innovation	Q1399209`
- `STEAM education Q62393596`

4. Node must have statement `official website (P856)` with a link pointing to documentation

5. Node must have statement `location (P276)` with value corresponding to item of the city where node happens.

  *Note: if city or region item doesn't have coordinate locations within its own page, node won't be mapped*

6. Node must have statement `part of (P361)` with value `Global Open Science Hardware (Q62391989)`

</details>

### Contributing to the map

You can contribute by adding nodes, translating data, enhancing visualizations or anything else that comes to your mind.

Check the [contribution guidelines](CONTRIBUTING.md) to see how.

### Further uses of the map 

Besides visualizing where GOSH projects are, I think structuring data this way can be useful for other things. E.g. listing resources that people find useful, links to journal articles, institutions supporting open science hardware, events organized by the community and so on. 

This organized information can then feed e.g. a landing page for people outside the community, but also be useful for evaluating through time how the community changes, if nodes are created, disappear or change.

:mailbox: Problems, questions, suggestions? **jarancio[at]fund-cenit.org.ar**
