---
layout: page
title: Home
---

![Picture of me](/public/me.jpg) 

I'm a [cosmologist](http://en.wikipedia.org/wiki/Cosmetology) and [Lagrange Fellow](http://ilp.upmc.fr/fellowships/postdoc-fellowships.php) at the [Insitut Lagrange de Paris](http://ilp.upmc.fr/index.php). This fall I join the [Berkeley Center for Cosmological Physics](http://bccp.berkeley.edu/) as a BCCP Fellow. On this site you'll find a little about my research, links to my papers, slides from my talks, and the occasional blog post. Feel free to email me at <a
  target="_blank"
  id="contact"
  href="https://www.google.com/recaptcha/mailhide/d?k=01RgRLgvxEUrUhAUtFCSPNRA==&amp;c=0nIRqiLvmUU-5ifT56SvMSY2hB9qsGA9T0u6dIWkHPI=">
    marius<span style="display:none">obfuscation</span>millea@gm<span style="display:none">obfuscation</span>ail.com</a>, unless of course you're a robot. 



<!-- See: https://gist.github.com/joshdick/961154 -->

<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.6/jquery.min.js"></script>
<script type="text/javascript">
  $(document).ready(function(){

    //First, remove the invisible <span>s from the link - now the plain-text e-mail address is in the DOM
    $("#contact span").remove();

    //Next, set the link's href attribute to be 'mailto:' plus the link text (the plain-text e-mail address from the previous step.)
    //BAM--instant simple mailto: link, except spam bots can't harvest it.
    $("#contact").attr("href", "mailto:" + $.trim($("#contact").text()));

  });
</script>
