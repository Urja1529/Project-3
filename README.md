#### Summary

Before middle age, limited objects are collected. In general dogs have more count, but in certain areas and era, ie, Egypt B.C., more cats' objects are found. After middle age, objects quantity is more sufficent to draw a conclusion: Dog is more closer to general public's life, hence more objects were left, but Cat shows increase trend as urbanisation.

#### Data Collection and Cleaning (Team Work)
  - Data Resources: The Metropolitan Museum of Art Collection API https://metmuseum.github.io/
  - Data Collection: /py/part_01_met_api.ipnb
    * Required object list by key words “cat” and “dog”, via API.
    * Request object details for each object ID
  - Data Clean: /py/part_01_met_api.ipnb
    * Due to overlapping “cat” and “dog”, the total objects collected is more than 50000 objects.
    * Remove all not related data, about 4600 objects are left for “cat” and “dog”.
    * Assign a team for each object, cat/both/dog.
    * Clean and combine redundant content, such as multiple Date related info. 
  - Map Data: /py/part_02_map_clean.ipnb 
    * Due to the nature of museum collection, location info can be a historical region, which is unable to locate with common country definition. c_# is assigned as geoCode to the close region.
    * Database: data/met_data.sqlite
  - Data for html: 
    * Museum objects details: data/met_data.json
    * GeoLocation correspond to geoCode: data/map_point.json
  - Original Data: /data/original_data
    * Original export from Met API
    * Map geo helping data
    * met_data.csv to convert .sqlite

#### Python Flask (Jiaolu Xie): /py/part_03_app.py
  - Data: data/met_data.sqlite
  - 3 API search based on team, app.route is added as url in the main html script.
  - 3 url links to git pages. https://urja1529.github.io/Project-3/ , backup version https://miwiki612.github.io/GIT-project3/ Details below.

### Visual Data Explorer

#### TimeLine: Surprise Me! (Jiaolu Xie): /js/plotb.js
  - Code Structure:
    * Select one geoCode randomly.
    * Try to pick 1 object for each era, randomly.
    * If unable to find 1 object in each era, then make sure to pick 5 objects in total, randomly. Avoid overlapping by removing selected objects.
    * Select information, add as string, insert to html div.
  - Button Design:
    * Clean div by id after click.
    * Run previous code with a new region. 

#### Map (Urja Dudhwala): /js/map.js
The Historical Objects Map project utilizes Leaflet, a JavaScript library for interactive maps, to display historical objects associated with different teams (cat, dog, both) across various time periods. The map features custom icons for each team and popups with detailed information about the objects.

Here's a brief overview:

Map Initialization: The project starts with a Leaflet map centered at coordinates [0, 0] and a zoom level of 2.

Base Tile Layers: Three base maps are available: OpenStreetMap for streets, Esri World Imagery for satellite imagery, and OpenTopoMap for topographic views.

Data Handling: Data is fetched from external JSON sources containing information about the objects and their locations.

Marker Icons: Custom icons are designed for the three teams: cat, dog, and both.

Layer Groups: Objects are categorized into time periods and organized into LayerGroup overlays for easy visualization.

Popups: Markers display popups with details about the objects, including team, culture, time period, country, and images where available.
    
#### Bar Plot and Animation (Kangna Parekh): /js/plota.js, /js/plotc.js, /js/plota-animation.js
* This code outputs an animated bar chart visualization that compares the search results for different categories ("Cat," "Dog," and "Both") over different centuries. Here's what each part of the output displays:

* Bar Chart Visualization: The main output is an animated bar chart displayed on a web page. The chart has three bars for each century, representing the percentage distribution of search results among the three categories ("Cat," "Dog," and "Both").

* Initial Display: When you first load the page, you will see the initial state of the bar chart. It displays the distribution of search results for the first century in a stacked bar format.

* Slider: Below the bar chart, there is a slider with labels corresponding to each century. This slider allows you to select a specific century and view its search result distribution.

* Animation: By clicking the "Start" button, the animation begins. The bars in the chart smoothly transition from one century's data to the next, showing how the distribution of search results changes over time.

* Control Buttons: The "Start" button initiates the animation, and the "Stop" button halts the animation at the current state.

* Real-Time Update: As the animation progresses, the chart and slider update in real time to reflect the changing search result distribution for each century.

* Overall, this output is an interactive and dynamic visualization that allows viewers to observe trends and changes in search results over centuries for different categories, enhancing the understanding of the data's historical context.


#### Timeline ( Riddhi Mistry): /js/timeline.js

##### Overview
This open-sourced timeline library from KnightLab (https://timeline.knightlab.com) allows to display the art gallery data in chronological order.

This library was essential to our project, it fully highlighted the change of art overtime, showcased the forms of media, and demonstrated how art has evolved over time!

##### Key Features

 1. **Slider**: Ability to pan left and left seemlessly across time
 2. **Zoom functionality**: Ability to zoom in and out, to get more detail views and break down of time.
 3. **Control Buttons**: Left and right button to go to next and previous art piece
 4. **Skip Buttons**: Ability to quickly skip to end or beginning of the timeline
 5. **Real Time Updates**: Fully integrated with a database which it pulls live data from.
 6. **Fully animated library**: Allows for a more modern feel 
 7. **Card View**: Ability to display key information as well as images to illustrate the art piece
 8. **Fully Customizable**: Ability to customize all aspect of the timeline component
 9. **Low memory consumption**: Allows it to be rendered on slower low memory devices
 10. **Quick Set Up**: plug and play

##### Sample of Chronological Timeline

![Sample of Chronological Timeline](https://github.com/UofT-Bootcamp-Data-Analytics/Project_3/assets/32605242/845ac9ca-0195-4651-af79-ec6253d19036)


