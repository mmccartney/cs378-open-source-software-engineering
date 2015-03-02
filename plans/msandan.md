## Status

* Trying to digest this [issue](https://github.com/geotrellis/curve/issues/3) to get a handle on first bulletpoint in Goal. Currently (2) in Plan

* Finishing up the HilbertCurve's RangeQuery implementation, crossing out (2) in the plan

* Adding benchmarks to zCurves

(1) in the plan has been mostly addressed by @brett61

## Goal

* As an SFCurve developer, I would like to create a common interface (API) to : test and benchmark implementations of space filling curves

* To do the above, I would like to have a scalable test and benchmark framework implemented  

* Other great goals to have would be flawless documentation, high test coverage, and example use cases 

## Plan

1. ~~Find implementations of space filling curves other than geotrellis/mesa and google's uzaygezen to get an idea of a general interface for testing and benchmarking them~~
1. ~~Implement bennight [code](https://github.com/chrisbennight/wgs84lexicoder) as exercise and an example of a framework for testing and benchmarking space filling curves~~
1. Add benchmarks for existing SFC's
1. Add to the conversation in this [issue](https://github.com/geotrellis/curve/issues/3)
1. Implement simple space filling curves as a baseline
1. Read up on literature (papers sent by Jim) 
1. Refactor GeoMesa/geohash/ space filling curves implementation into SFCurves/ project
