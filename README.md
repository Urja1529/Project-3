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
  - 3 url links to git pages. Details below.

### Visual Data Explorer

#### TimeLine: Surprise Me! (Jiaolu Xie): /js/plotb.js
  - Code Structure:
    * Select one geoCode randomly.
    * Try to pick 1 object for each era, randomly.
    * If unable to find 1 object in each era, then make sure to pick 5 objects in total, randomly. Avoid overlapping by removing selected objects.
Select information, add as string, insert to html div.
  - Button Design:
    * Clean div by id after click.
    * Run previous code with a new region. 

#### Map (): /js/map.js
#### Bar Plot and Animation (): /js/plota.js, /js/plotc.js, /js/plota-animation.js

#### Timeline: Overview (): /

