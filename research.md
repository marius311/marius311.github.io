---
layout: page
title: My Reseach
---


##For non-experts

Cosmology is the study of the properties of the universe as a whole. How did the universe start? How did it evolve, and how did galaxies and other structures form? What is the universe made up of, for example what is dark matter and what is dark energy? Today they make up about 95% of the energy in the universe but we know surprisingly little about them. And can we use cosmological probes, observations on the biggest scales known to man, to learn about elementary particles, some of the smallest things we know of? 

Of all of the different things we have thought to observe looking out into space, the Cosmic Microwave Background (CMB) has proven to be the most informative for the types of questions cosmologists ask. If our eyes could see microwaves instead of visible light (yep, just like the microwave oven, or your home wireless), and you looked out into space, you would see a single highly uniform glow coming from all directions. If on top of that your eyes also had their contrast turned up by a factor of about 10,000x, you could make out that this glow is not exactly uniform, but a little bluer in some spots and a little redder in others (well, at least the red/blue analog of microwaves, meaning higher/lower frequencies). The video below is an animation showing what the CMB looks like from Earth. (credit [NASA](http://www.jpl.nasa.gov/video/details.php?id=1205))

<img class="gfyitem" data-id="SnoopyGorgeousHalibut" style="width: 100%;"/>

The CMB was created about 13.8 billion years ago when the universe was much denser and hotter than today. Just like a piece of metal glows red-hot, the entire *universe* back then was glowing. As the universe cooled due to the expansion of space, there came a critical time when it turned from opaque to transparent, releasing this glow and creating the CMB, the light from which has been traveling to us ever since. 

The patterns of hot and cold spots encode in them the properties of the universe when the CMB was released, as well as how the CMB photons have been affected by their journey throughout the universe since then until today. These patterns are sensitive to what properties we assume the dark matter has, what the dark energy is, how the universe began and evolved, and the properties of many known and hypothetical elementary particles. It is quite amazing how many different aspects of physics all play a role in making the CMB look like the way it does! 

My research is mainly focused on analyzing the properties of these hot and cold spots in CMB, and turning this into definite answer to questions about physical law. Some of this analysis is pretty computationally intensive, meaning we use some fairly sophisticated computational tools. I have been largely working on answering questions about two specific types of particles, [neutrinos](http://en.wikipedia.org/wiki/Neutrino) and [axions](http://en.wikipedia.org/wiki/Axion), although my interests are generally broader. More indirectly I also work with other cosmological probes coming, for example, from observations of galaxies, super novas, and cosmic rays.



##For experts

My research is focused on the interplay between cosmological data and fundamental physics. Ultimately
I'm interested in revealing the answers to fundamental questions, but I find the process of extracting this
information is rewarding and ensuring the fidelity of these answers is important.

###Cosmological data analysis
As a member of Planck and South Pole Telescope collaborations, I worked extensively on analyzing the power spectrum of the Cosmic Microwave Background (CMB). For Planck, I developed the [Mspec](https://github.com/marius311/mspec) likelihood, a intensity and polarization multi-frequency maps-to-parameters pipeline which was used in the 2015 release of Planck results (in the [parameter](http://xxx.lanl.gov/abs/1502.01589) and likelihood paper, in prep). Mspec is efficiently parallelized with [mpi4py](http://mpi4py.scipy.org/) and [h5py](http://www.h5py.org/) in order to run across hundreds of cores at computing centers such as [NERSC](https://www.nersc.gov/). Mspec accounts for galactic and extra-galactic CMB foregrounds, and area in which I've been [interested](http://adsabs.harvard.edu/abs/2012ApJ...746....4M). I also developed the parameter estimation code, [CosmoSlik](https://github.com/marius311/cosmoslik), as a replacement for the often-used [CosmoMC](http://cosmologist.info/cosmomc/). CosmoSlik has advantages such as being more modular and being written in Python and Cython. 

Probably my most widely used analysis software is [PICO](https://sites.google.com/a/ucdavis.edu/pico/), which computes the CMB power spectrum orders of magnitude faster than codes like [CAMB](camb.info) or [CLASS](http://class-code.net/) by interpolating the $C_\ell$'s as a function of cosmological parameters based on a training set, rather than directly solving the CMB Boltzmann equations each time. Part of the training for PICO happens with [Cosmology@Home](http://www.cosmologyathome.org/), where I have contributed to development.


###Constraining fundamental physics

####Neutrinos
Right now is an extremely exciting time for cosmological neutrino physics. Constraints on the masses of the neutrinos, $\Sigma m\_\nu$, and the number of neutrino-like species, $N\_{\rm eff}$, have been improving significantly as CMB experiments measure further into the damping tail of the temperature and polarization power spectrum, and as they measure the gravitational lensing potential. Within the next decade, we are essentially [guaranteed](http://adsabs.harvard.edu/abs/2013arXiv1309.5383A) to detect $\Sigma m\_\nu$ to 3$\sigma$, and even the tiny energy imparted on the neutrinos from electron-positron annihilation to within 2$\sigma$. 

My research on neutrinos has focused on determining the [physical effects](http://adsabs.harvard.edu/abs/2013PhRvD..87h3008H) leading to our constraints on neutrino parameters, and in some cases [isolating](http://adsabs.harvard.edu/abs/2015arXiv150307863F) these effects to give novel constraints. 


####Axions
Among the slew of hypothetical particles predicted by various theories, axions are arguably the most likely to actually exist. Their predicted weak coupling makes them difficult to detect in the laboratory, but cosmological constraints can be complementary. I've worked out the [latest](http://adsabs.harvard.edu/abs/2015arXiv150104097M) constraints on high mass axions, which ruled out some interesting regions of parameter space. I also showed a way in which axions can hide the presence of additional thermalized sterile neutrinos, an idea which can be tested with next generation electron-positron colliders. I continue to be interested in ways to constrain axions (in any mass range) with cosmological observations. 
