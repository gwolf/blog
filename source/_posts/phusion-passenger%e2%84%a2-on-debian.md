title: "Phusion Passenger™ on Debian"
date: 2009/8/7 17:32:02
tags:
- apache
- beer
- debconf
- debian
- nginx
- passenger
- rails
---
During <a href="http://debconf9.debconf.org">DebConf9</a> I had the opportunity to work together with <a href="http://www.flickr.com/photos/sfllaw/1263528602/">Señor Micah</a> to try to bring <a href="http://www.modrails.com/">Passenger</a> back to shape and get it back to the <a href="http://ftp-master.debian.org/new.html">NEW queue on Debian</a>. We spent way too much time dealing with the build  for the <a href="http://pkg-ruby-extras.alioth.debian.org/subversion.html">pkg-ruby-extras build model</a> than to the actual fixing and updating. At the end we came up with a very well updated and <strong>DFSG-compatible</strong> (in contrast to the one that <a href="http://www.brightbox.co.uk/">Brightbox</a> provides, which isn't bad either to be honest) package for the 2.2.4 version.

Our current main interest was trying to get the package into Debian by cleaning up the <a href="http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=488753">licensing issues</a> on some of the included files and try to come up with improvements in the near future (such as using Passenger directly from <a href="http://nginx.net/">Nginx</a>, instead of the <a href="http://httpd.apache.org">Apache</a>-only module). The future is bright and it'll bring sunshine to all of us.

Given that the package is still on the queue and there's a hell lot of other packages to be processed, you can grab the package <a href="http://damog.net/debian/libapache2-mod-passenger_2.2.4debian-1_i386.deb">here</a> and if it fulfills your expectations, make sure you offer me and/or Micah a beer next time you see us around.