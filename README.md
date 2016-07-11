##  Validation

Summary -- In particular for the galaxy input catalogs, a set of observations and their biases and selection
effects needs to be assembled for use in validating the simulated catalogs.

### Key Tasks
* Key Task CS4.1.1 ( 03/16 ): Produce a document outlining all data sets and their validation criteria for all
available requirements.

#### Suggested organization
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

#### Clusters:
(Katrin)x(Steve, Ian)
* Need accurrate prediction for mass function over range of cosmology, 5% or better
* Specific concerns:
  * How do cluster masses depend on cluster center finder
  * Overdensity mass definitions in different halo finders
  * Hydrodynamics effects?
* For validation framework: provide mass function measurement tool, mass function fits to check how well catalog reproduces mass function prediction (simulation concerns are mainly about resolution, volume)
* Correct colors and distribution of galaxy cluster members, including correct redshift distribution

Cluster WG task:
* Provide data to validate cluster galaxy distribution and color

CS WG task:
* Develop accurate mass function prediction

#### Weak Lensing
(Simon)x(Will Dawson, Michael Schneider)
Notes from a side session at the Argonne DESC meeting.
*******
Q: What are the most important observables to get right?
A: 
1. Shear two point correlations.  In particular, the small angle shear correlation amplitude is important.
The best definition of an observable is:
0.5 arcmin to 2 deg shear 2pt correlation amplitude (this will require Gpc scale simulations)
Henk Hoekstra found that the catalogs need to be quite deep (2 mags deeper than the flux cut in the analysis catalog) otherwise you don't get the shear bias right.
One could think about inventing a SAM mechanism to help get that right without needing ultra high resolution simulations.

*Compare to DLS.*

2. Number density -- raw number density (the number counts from space).  No dataset specified, but need hubble number counts.

3. Ellipticity distributions are too hard to get right.  They should be close to e.g. *COSMOS*.

