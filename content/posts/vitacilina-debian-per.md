---
title: "Vitacilina now in Debian + 0.2 released!"
date: 2009-11-29 14:24:51
tag:
- cpan
- debian
- perl
- planet
- planeta linux
- vitacilina
---
<a href="http://damog.net/old/stereonaut/2009/11/2046242410_e38c021cc0.jpg"><img class="size-medium wp-image-1058 alignright" title="2046242410_e38c021cc0" src="http://damog.net/old/stereonaut/2009/11/2046242410_e38c021cc0-300x279.jpg" alt="2046242410_e38c021cc0" width="210" height="195" /></a>Remember <a href="http://stereonaut.net/quick-feed-aggregation-with-vitacilina/">Vitacilina</a>? A small aggregation library I wrote last year to be intended to replace <a href="http://planetplanet.org">Planet</a> on <a href="http://planetalinux.org">Planeta Linux</a>? Well, it never quite replaced it but it achieved some level of stability since I was using it for a number of tasks at work. So, during this long holiday weekend, I received a notification that the Request To Package bug I had <a href="http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=513772">filled</a> against the <a href="http://www.debian.org/devel/wnpp/">Work-Needing and Prospective Packages in Debian</a> has already been taken care of and the library had been uploaded. Of course, I could have made this myself a long time ago, but at the time it was simpler and faster just to hope someone else would do it at some point.

So, <a href="http://qa.debian.org/developer.php?login=debian@midworld.net">Dario</a> did it. He packaged it and uploaded version 0.1 under the umbrella of the <a href="http://pkg-perl.alioth.debian.org/">Debian Perl Group</a>. Hurray!

But then I realized that <a href="http://chorny.net/">Alexandr Ciornii</a> had implemented some nice changes to <a href="http://github.com/damog/vitacilina">Vitacilina</a> back in September that I never got to include or release as a <a href="http://search.cpan.org/">CPAN</a> distribution. And so I just did. I've uploaded 0.2 to CPAN and you can fetch it with <tt><a href="http://search.cpan.org/~miyagawa/App-CPAN-Fresh-0.07/cpanf">cpanf</a> Vitacilina</tt> or wait for the Debian Perl folks to update it :)