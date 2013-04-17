#CLEAR-MOT

A standard metric for evaluating the multiple target tracking algorithm is the CLEAR MOT.  This metric is described in the paper [1] .

## Details

We provide the code that implements the metric CLER-MOT has described by the authors in [1]. The function is implemented in MATLAB and has been tested
on real data generated by a multiple-target tracker.

The tarball contains these MATLAB files:

1. groundtruth.mat contains the labeled annotations of 3 objects. Objects are specificated by bounding box as [tl.x tl.y br.x br.y].
1. result.mat contains the tracking results hypothesis as taken from the ground truth files.
1. evaluateMOT.m is the function that perform the evaluation.
1. demo.m is the main file that you can launch to test the CLEAR-MOT script.
1. GreedyAssociation.m is the file that performs the association give the distance matrix. You can replace with other solver like Hungarian algorithm. These files are an example: if you want to use the script to evaluate you multiple target tracking, you have to recreate the structures groundtruth.mat and result.mat with your own data.


## Demo Example
To run our code and have a brief results just copy-paste this code:

	load groundtruth
	load result
	VOCscore = 0.5;
	dispON  = true;
	ClearMOT = evaluateMOT(gt,result,VOCscore,dispON);


## Citation

Please cite our paper with the following bibtex if you use our dataset:

``` latex
@article{ masi:multimedia12,
author = {Bagdanov, Andrew D. and Del Bimbo, Alberto and Dini, 
Fabrizio and Lisanti,  Giuseppe and Masi, Iacopo},
title = {Compact and efficient posterity logging of face imagery for
video surveillance},
booktitle = {IEEE Multimedia},
year = {2012}, }
```

## References

[1] Keni Bernardin and Rainer Stiefelhagen. “Evaluating multiple
objec tracking performance: the CLEAR MOT metrics” J. Image Video
Process. 2008, Article 1 (January 2008), 10 pages.” DOI=10.1155/2008/246309
http://dx.doi.org/10.1155/2008/246309

##License
CLEAR-MOT Matlab script is Copyright (c) 2013 of Iacopo Masi and Giusppe Lisanti *\<masi,lisanti\>@dsi.unifi.it*.

[Media Integration and Communication Center (MICC), University of Florence. ](http://www.micc.unifi.it/vim).
