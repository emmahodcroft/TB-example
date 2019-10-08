# Tuberculosis Example Data
The data for this example comes from the great paper by Crispell et al. ["Using whole genome sequencing to investigate transmission in a multi-host system: bovine tuberculosis in New Zealand"](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-017-3569-x).
(If you'd like your results to be a surprise, visit the paper after doing the analysis!)


### General Tips
* The data do not need to be filtered, but you can play with filtering
* Some sites should be masked
* Some drug resistance mutation sites (DRMs) should be excluded during the `tree` step
* Not all genes should be translated (to save time) - only those involved in drug resistance. A list of them is provided
* A file containing gene annotations is provided
* Are you able to provide colors for the `host` or `host_cat` traits?

### Geography
* All samples are from one region and one country. Another geographic location field is present in the metadata 
* This field should be used for placing the sequences on the map, for trait reconstruction, and as a colorby
* Latitude & longitudes for these places is not part of `augur` - a list of their lat-longs is provided - you'll need to incorporate this for the sequences to show on the map

### Drug resistance
* Drug resistance can be inferred using the provided list of DRM sites
* These are both AA and nucleotide locations, so you'll need to pass in both AA and nucleotide information
* To make the resulting drug resistance show up in Auspice, you'll need to ensure the right fields are in your config - see the end of the 'TB'/'VCF' tutorial for some guidance
* Drug resistance information is provided for many drugs in the file, but this dataset may not have resistance to all of them
* _(Drug resistance is a bit odd for this dataset; don't be worried if you end up with slightly unexpected results)_

### Clades
This data can be nicely divided into 4 clades. Here are some mutations that define each clade:

* Clade_1:
  * in `ethA`, 'S' at position 484
  * in `icl1`, 'A' at position 400
  * 'T' at nucleotide position 4039
* Clade_2:
  * in `embC`, 'S' at position 940
  * in `Rv3463`, 'K' at position 192
  * 'T' at nucleotide position 4039
* Clade_3:
  * in `Rv2209`, 'I' at position 432
  * in `Rv0323c`, 'S' at position 123
  * 'A' at nucleotide position 67108
* Clade_4:
  * in `eccC2`, 'A' at position 62
  * in `rbsK`, 'G' at position 75
  * 'G' at nucleotide position 27979
