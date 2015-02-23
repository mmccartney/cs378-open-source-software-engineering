## Status

I have my development environment up and feel comfortable making code changes.
I have an idea of how the library will be used and the customers who will use it.
I'm currently trying to implement a space filling curve in scala from a java implementation of a HilbertCurve (see 2 under Plan).
## Goal

* As an SFCurve developer, I would like to create a common interface (API) to : test and benchmark implementations of space filling curves

* To do the above, I would like to have a scalable test and benchmark framework implemented  

* Other great goals to have would be flawless documentation, high test coverage, and example use cases 

## Plan

1. Find implementations of space filling curves other than geotrellis/mesa and google's uzaygezen to get an idea of a general interface for testing and benchmarking them
1. Implement bennight [code](https://github.com/chrisbennight/wgs84lexicoder) as exercise and an example of a framework for testing and benchmarking space filling curves
1. Implement simple space filling curves as a baseline
1. Read up on literature (papers sent by Jim) 
1. Refactor GeoMesa/geohash/ space filling curves implementation into SFCurves/ project
