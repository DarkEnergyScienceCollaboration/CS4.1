# Actual request to CosmoSim group:
After informal discussions with members of the SN group, we discussed this question at a telecon on May 6. This was followed by an extended discussion over email based on a summary of the telecon discussion available at https://gist.github.com/rbiswas4/308db2c587f629e6c3854159caf1a2ca .

In answer to the cosmoSim request: ""What are the three primary distributions you need to get correct from the mock catalogs?" we would like to have :

- stellar mass, redshift of galaxies (needed for distributing SN in galaxies, also a propetry correlated to SN properties)
- light distribution around the galaxy (in terms of something like sersic profiles, or other measures). 
- Star Formation History of the galaxy (If we convolve this with a time delay distribution, we shoudl be able to get a rte for SN) 

More generally, the main use case for the SN group to use these mock catalogs as host galaxies for simulated SN. The importance of knowing the truths of galaxy properties is the ability to distribute SN in them according to properties. It is known that SN properties are correlated with host galaxy properties (which are themselves correlated), but exact physical drivers are not well understood. Therefore the SN group would like to use different combinations of such properties to study SN simulations. Therefore, there is more interest in getting the distributions of galaxy properties 

Such quantities include:
- Total Mass of galaxy (halo mass = DM + stellar + gas mass) (to be used for lensing? )
- metallicity (again correlated with SN properties)
- morphology of galaxy


### Further issues of interest
- redshifts ranges over which these distributions might be helpful: It would be nice to get redshift limits to about 3. (hosts of superluminous supernovae), Would be necessary to get redshifts till about 1.4, range for SNIa.
- range in stellar mass or luminosity: How low mass will this catalog go? Galaxies that will not be seen will host SN that can be seen. 

## A couple of questions came up for Cosmological Simulations Group
- One might expect that data challanges will happen on the basis of these mock catalogs: producing catalog/image data and analyses to inferring the values of these quantities. The SN group would like to use such analyzed values along with the truth values in their analyses to understand selection effects and biases. Is there a plan to provide such collated information ?
- Would this group like SN simulations added to them?
