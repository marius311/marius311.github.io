---
layout: page
title: Research
---


## For non-experts
For non-experts
---------------

Cosmology is the study of the properties of the universe as a whole. How did the universe start? How did it evolve, and how did galaxies and other structures form? What is the universe made up of, for example what is dark matter and what is dark energy? Today they make up about 95% of the energy in the universe but we know surprisingly little about them. And can we use cosmological probes (observations on the biggest scales known to man) to learn about elementary particles (some of the smallest things we know of)?

Of all of the different things we have thought to observe looking out into space, the cosmic microwave background (CMB) has proven to be the most informative for the types of questions cosmologists ask. If our eyes could see microwaves instead of visible light (yep, microwaves just like your microwave oven or your home wireless), and you looked out into space, you would see a single highly uniform glow coming from all directions. If on top of that your eyes also had the contrast turned up by a factor of about a 10,000, you could make out that this glow is not exactly uniform, but a little bluer in some spots and a little redder in others (that is, the red/blue analog for microwaves, which also corresponds to hotter and colder). The animation below gives you an idea of what these hot and cold spots look like (credit [NASA](http://www.jpl.nasa.gov/video/details.php?id=1205)).

<img class="gfyitem" data-id="SnoopyGorgeousHalibut" style="width: 100%;"/>

The CMB was created about 13.8 billion years ago when the universe was much denser and hotter than today. Just like a piece of metal glows red-hot, the entire *universe* back then was glowing. As the universe cooled due to the expansion of space, there came a critical time when it turned from opaque to transparent, releasing this glow and creating the CMB, the light from which has been traveling to us ever since. 

The patterns of hot and cold spots encode in them the properties of the universe when the CMB was released, as well as how the CMB photons have been affected by their journey throughout the universe since then until today. These patterns are sensitive to what properties we assume the dark matter has, what the dark energy is, how the universe began and evolved, and the properties of many known and hypothetical elementary particles. It is quite amazing how many different aspects of physics all play a role in making the CMB look like the way it does! This is what makes it such a powerful probe of physics. 

My research is mainly focused on analyzing the properties of these hot and cold spots in CMB, and turning this into definite answers to questions about the laws of physics. Some of this analysis is pretty computationally intensive, so the use of sophisticated computational tools is necessary (and fun!). I have been largely working on using the CMB to learn about two specific types of particles, [neutrinos](http://en.wikipedia.org/wiki/Neutrino) and [axions](http://en.wikipedia.org/wiki/Axion), although my interests are generally broader. More indirectly I also work with other cosmological probes coming from, for example, observations of galaxies, supernovas, and cosmic rays.



##For experts


My research is focused on the interplay between cosmological data and fundamental physics. Ultimately what drives me is revealing the answers to fundamental questions, but I find the process of extracting this information is rewarding and ensuring the fidelity of these answers is extremely important. My main expertise lies in the data and physics relevant to the CMB. I have worked out the latest cosmological bounds on axions and axion-like particles from the combination of CMB and big bang nucleosynthesis (BBN) data. I have also studied and isolated  the effects of neutrinos and how these physically lead to constraints on the number of neutrino-like species from CMB data. Throughout my research, I have not only used CMB data but heavily participated in its production and validation. This has included examining the impact of foregrounds and secondaries on the CMB power spectrum, and developing analysis pipelines and testing for systematics. Despite my main focus on the CMB and astroparticle physics, my interests are quite broad and include any not-too-far-off cosmological observations and the theories and physics pertaining to them.

###Cosmological data analysis
I'm a member of the Planck and South Pole Telescope collaborations, where I worked extensively on analyzing the power spectrum of the CMB. For Planck, I developed the [Mspec](https://github.com/marius311/mspec) likelihood, a intensity and polarization multi-frequency maps-to-parameters pipeline which was used in the 2015 release of Planck results (in the [parameter](http://xxx.lanl.gov/abs/1502.01589) and likelihood paper, in prep). Mspec is efficiently parallelized with [mpi4py](http://mpi4py.scipy.org/) and [h5py](http://www.h5py.org/) in order to run across hundreds of cores at computing centers such as [NERSC](https://www.nersc.gov/). Mspec accounts for galactic and extra-galactic CMB foregrounds, and area in which I've been [interested](http://adsabs.harvard.edu/abs/2012ApJ...746....4M). I also developed the parameter estimation code, [CosmoSlik](https://github.com/marius311/cosmoslik), as a replacement for the often-used [CosmoMC](http://cosmologist.info/cosmomc/). CosmoSlik has advantages such as being more modular and being written in Python and Cython. 

Probably my most widely used analysis software is [PICO](https://sites.google.com/a/ucdavis.edu/pico/), which computes the CMB power spectrum orders of magnitude faster than codes like [CAMB](camb.info) or [CLASS](http://class-code.net/). This is achieved by interpolating the $C_\ell$'s as a function of cosmological parameters based on a training set, rather than directly solving the CMB Boltzmann equations each time. Part of the training for PICO happens with [Cosmology@Home](http://www.cosmologyathome.org/), which I have helped in developing. 


###Constraining fundamental physics

####Neutrinos
The present time is an extremely exciting time for cosmological neutrino physics. Constraints on the sum of the neutrino masses, $\Sigma m\_\nu$, and the number of neutrino-like species, $N\_{\rm eff}$, have been improving significantly as CMB experiments measure further into the damping tail of the temperature and polarization power spectrum, and as they infer the gravitational lensing potential. Within the next decade, we are essentially [guaranteed](http://adsabs.harvard.edu/abs/2013arXiv1309.5383A) a first detection of non-zero $\Sigma m\_\nu$ to at least 3$\sigma$, giving important clues to the otherwise speculative origin for the masses of the neutrinos. For $N\_{\rm eff}$, the sensitivity will reach the level needed distinguish even the tiny energy imparted on the neutrinos from electron-positron annihilation to within 2$\sigma$, and more importantly further test for any non-standard physics affecting very early times. 

My research on neutrinos has focused on determining the [physical effects](http://adsabs.harvard.edu/abs/2013PhRvD..87h3008H) leading to our constraints on neutrino parameters, and in some cases [isolating](http://adsabs.harvard.edu/abs/2015arXiv150307863F) these effects to give novel constraints. 


####Axions
Among the slew of hypothetical particles predicted by various theories, axions are arguably the most likely to actually exist. Their predicted weak coupling makes them difficult to detect in the laboratory, but cosmological constraints can be complementary. I've worked out the [latest](http://adsabs.harvard.edu/abs/2015arXiv150104097M) constraints on high mass axions, which ruled out some interesting regions of parameter space. I also showed a way in which axions can hide the presence of additional thermalized sterile neutrinos, an idea which can be tested with next generation electron-positron colliders. I continue to be interested in ways to constrain axions (in any mass range) with cosmological observations. 
