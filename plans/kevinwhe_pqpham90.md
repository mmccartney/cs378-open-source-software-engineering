## Status

Our enviroments are fully functional. We finished moving from Leaflet to Openlayers and now need to get data into the baseball cards. We would like to decouple the cards from where they are getting the data from and put the wms (web map service) data request logic somewhere besides the cards directive. 

We also need to find a way to make things faster, as our map takes too long to load.

## Goal

We will implement the following use cases:

* As web developers we would like the map to be working in a clean and intuitive manner.

* As Geomesa clients we would like to get the features implemented with data pulled from the cloud.

## Plan

1. Learn the APIs for Openlayers 3 to see if there's a built in solution to the issue. Also, continue learning Angular.
2. Get Jim's advice on how to organize the data retrieval logic.
3. Submit a pull request so Jim and coworkers can see our work and give feedback.
4. Centralize the team around a single git repo.
5. Get data retrieval from cloud working.
6. Get cards displaying this data.
 -- Also write tests along the way.
