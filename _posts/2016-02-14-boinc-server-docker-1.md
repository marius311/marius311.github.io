---
layout: post
title: Turbocharged Science on BOINC (with Docker)
comments: true
excerpt_separator: <!--more-->
---


I run a [BOINC](http://boinc.berkeley.edu/) volunteer computing project, [Cosmology@Home](http://www.cosmologyathome.org). I love BOINC, but I think its ridiculously difficult to develop a project. In the past I would have never recommend to a colleague to create their own project, at least not a colleague that was serious about doing science instead of spending all day maintaining their BOINC project. But with what I'll show you here, [boinc-server-docker](https://github.com/marius311/boinc-server-docker), I think it can be so easy to develop for BOINC that it's realistic actually to do your *day-to-day* computation on a BOINC project.

<!--more-->

In this ~10 minute video I'll take you through creating a BOINC project and developing an application with boinc-server-docker. The key to do this in 10 minutes (really, no cheating!), is that the server as well as the BOINC applications are packaged inside [Docker](https://www.docker.com/).

Cosmology@Home already runs this way and it works well. But there's plenty to be improved, and for that I need help. So any BOINC and/or Docker experts want to help turn BOINC into something *even* more useful? Please, lets talk and collaborate on this project!

<div style="text-align: center;">
<iframe width="600" height="450" src="https://www.youtube.com/embed/U1cdEC7xBhY" frameborder="0" allowfullscreen></iframe>
</div>

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
