#  A document listing observation seets for validation

Summary -- In particular for the galaxy input catalogs, a set of observations and their biases and selection
effects needs to be assembled for use in validating the simulated catalogs.

## Key Tasks
* Key Task CS4.1.1 ( 03/16 ): Produce a document outlining all data sets and their validation criteria for all
available requirements.

### Suggested organization
Repositories are available per deliverable.  Each key task has a subdirectory.
We have a `source` directory in each key task area for any supporting
code that goes with an effort.  There will also be a `doc` directory to hold documents in markdown,
latex, or binary formats.  The idea is to version everything and give us a good way to diff things.

Each deliverable is slightly different, so these repositories should grow to support the different need.

Please feel free to use github issues on each repository to organize work.

What are the three primary distributions you need to get correct from the mock catalogs?
POCs: working group leads
Rahul: SNe, Simon: LSS, Katrin: clusters, Eve: Photo-z, Adrian: SL, Wentao: WL

#### Photo-z:
(Katrin,Adrian) x (Alex,Sam,Jeff)

Tests:
* general population galaxies
  * test color distributions over a broad range of galaxy types, redshifts, and luminosities
  * DEEP2+COSMOS data
  * CFHT observed filters
  * simple cuts
* red sequence galaxies
  * test colors of a specific, important galaxy sub-population
  * DES data
  * DES observed filters
  * more complicated cuts

Photo-z WG tasks:
* collect data
* provide filter curves
* supply code that applies appropriate cuts and creates correct plot for comparison

CS WG tasks:
* show photo-z WG how to use validation framework at NERSC so that they can generate the same comparison plots for their tweaked versions of simulated catalogs

Outstanding issues/questions:
* file formats (eg. fits or hdf5, does it even matter with python?)
* are there photometric calibration issues (eg. zero points) to worry about or can the plotting code take care of that easily?
* SAMs need to turn on extinction/reddening, tune parameters somewhat, and may eventually want to incorporate emission lines
