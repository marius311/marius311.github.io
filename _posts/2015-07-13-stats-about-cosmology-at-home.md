---
layout: post
title: Stats about Cosmology@Home
comments: true
excerpt_separator: <!--more-->
---

Perhaps let's start with *what is* [Cosmology@Home](http://www.cosmologyathome.org)? .  

Cosmology@Home (C@H for short) is a distributed volunteer computing project which allows people all over the world to donate their spare computer time when they're not using it (like when their screen-saver is on) to help cosmologists run the computations we need to answer some of the biggest questions about our universe.

<!--more-->

Many of you reading this might already be volunteers, in which case hello and thank you! If you're not but would like to be, [here's how](http://www.cosmologyathome.org/info.php).

I'm currently one of the main developers at C@H. In planning some upgrades, we needed to take a detailed look at some stats about our users. Then we thought, this is cool information that others might be interested in too! So here it is. There's also an IPython [notebook](http://nbviewer.ipython.org/github/marius311/marius311.github.io/blob/master/public/posts/ch/stats.ipynb) if you're curious how these plots were made or would like to do something similar for your own @Home project.

C@H has been around since 2007 and over the years about 50,000 unique computers have run a computation for us. The number of active computers, that is any which have returned a result in the last month, currently sits at about 5700. The data in the remainder of this post are going to be about just these computers. Based on IP addresses, here's where they're located:

<img src="/public/posts/ch/world.svg" alt="World" title="Obviously this blue part here is the land...">

C@H is currently used to create "training sets" for the [PICO](https://sites.google.com/a/ucdavis.edu/pico) code. These training sets consist of samples from the parameter space of possible cosmological models (e.g. a universe with 30% matter and 70% dark energy, or one with 31% matter and 69% dark energy, etc... in reality there's as many as 10 properties we vary). Each sample is sent out to a different computer which computes what such a universe might look like, and is rewarded a number of "credits" for each computation. We use this data to train PICO and see which models best fit the available cosmological data (a more detailed description will be the subject of a future post).

We wanted to make sure our planned upgrade will be compatible with most everyone's operating system, and based on this it will:

![Operating Systems](/public/posts/ch/hosts.svg)

We don't currently support Macs but in fact the upgrade will add support!

The "number of credits" in the plot above represents how many credits were received by computers running that operating system (arbitrarily scaled to appear on the same axes). The interpretation is that, e.g. hosts running Windows Server 2008 R2 are very efficient, while Windows 8.1 computers are less so. A large factor in performance is the number of CPUs a given computer has. Here's what our distribution across all computers looks like:

![Cpus](/public/posts/ch/cpus.svg)

Lots of users running multi-core systems is great as our upgrade will allow more efficient use of these systems. (Also, if you look closely, no, Intel hasn't come out with new 3-core and 7-core processors, its that users can limit how many cores they provide to C@H). 

We are also looking at upgrades targeting 64 bit computers, which are a large and growing majority of the total computation power (based on credits received):

![32vs64](/public/posts/ch/32vs64.svg)


Running jobs means downloading input files and uploading results, and for current purposes, C@H Internet connections are largely sufficient:

![Transfer](/public/posts/ch/transfer.svg)

Finally, an important statistic is turnaround time. That is, how long between when a computer gets sent a job until the result is returned. Here's the distribution of average turnaround times, 

![Turnaround](/public/posts/ch/turnaround.svg)

About half of computers return a result within the first three days. Wait times to submit similarly large jobs on some computing clusters are comparable to this so this is pretty good for a volunteer project! 

There are many more statistics one could look at, for us this was all we needed to know C@H computers look ready for our planned upgrades. Hopefully you found some of this interesting too! Feel free to leave suggestions or comments below.

{% if page.comments %}
<div id="disqus_thread"></div>
<script type="text/javascript">
    /* * * CONFIGURATION VARIABLES * * */
    var disqus_shortname = 'cosmicmar';
    
    /* * * DON'T EDIT BELOW THIS LINE * * */
    (function() {
        var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
        dsq.src = '//' + disqus_shortname + '.disqus.com/embed.js';
        (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript" rel="nofollow">comments powered by Disqus.</a></noscript>
{% endif %}
