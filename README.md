# TB-example
Trial TB data for Nextstrain tutorials

### General Tips
* The data do not need to be filtered, but you can play with filtering
* Some sites should be masked
* Some drug resistance mutation sites (DRMs) should be excluded during the `tree` step
* Not all genes should be translated (to save time) - only those involved in drug resistance. A list of them is provided
* A file containing gene annotations is provided

### Geography
* All samples are from one region and one country. Another geographic location field is present in the metadata 
* This field should be used for placing the sequences on the map, for trait reconstruction, and as a colorby
* Latitude & longitudes for these places is not part of `augur` - a list of their lat-longs is provided - you'll need to incorporate this for the sequences to show on the map

### Drug resistance
* Drug resistance can be inferred using the provided list of DRM sites
* To make the resulting drug resistance show up in Auspice, you'll need to ensure the right fields are in your config - see the end of the 'TB'/'VCF' tutorial for some guidance
* Drug resistance information is provided for many drugs, but this dataset may not have resistance to all of them

### Clades
This data can be nicely divided into 4 clades. Here are some mutations that define each clade:

* Clade_1:
  * in "ethA", 'S' at position 484
