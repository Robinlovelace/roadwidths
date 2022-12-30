

The aim of this repo is to document the process of estimating road widths from aerial photography.

That is a worthy aim, as evidenced by feedback to a Tweet asking how to do it: https://twitter.com/robinlovelace/status/1608595571635556352 and this toot: https://fosstodon.org/@robinlovelace/109598027567544977

The approach proposed is as follows:

- Get high resolution imagery, e.g. 25 cm resolution imagery from the Environment Agency via Edina, shown below.
- Create a training dataset by classifying pixels for a sample dataset, e.g. into carriageway, sidewalk (pavement), other. This can be done manually or with reference to other datasets such as MM Topo.
- Download OSM highway data for the area
- For each segment sample at intervals along the segment to get width estimates per OSM way
- Compare the estimated widths with a ground truth dataset (e.g. OSM MM Highways) to generate confidence bands for predictions (e.g. 95% CIs)

![](https://user-images.githubusercontent.com/1825120/210022922-9e1a7d37-ef73-45a0-b89a-8f68122fd95f.png)

## References

Much of the groundwork has already been done.
The most promising repo for image classification seems to be 

- https://github.com/jdalrym2/road_surface_classifier

There is also

- https://github.com/jiankang1991/road_extraction_remote_sensing

and 

- https://twitter.com/andymaclachlan/status/1608574374008991745

