---
layout: post
title:  "Upgrading NONMEM to Yosemite"
date:   2014-09-04 09:56:34
categories: nonmem update
---
Apple released their new OS (Yosemite) a few weeks ago. Unfortunately upgrading to the new system breaks the installation of NONMEM, PsN, and Pirana. Here's what I did to get up and running again. Altogether this should take less than 20 minutes. (Please note that I nor Pirana Software & Consulting BV can be held liable for any damage cause directly or indirectly by following the advice bewlow!)

* Step 1

You need to re-install gcc/gfortran. You can install from source, or from e.g. HomeBrew, but I just chose to take the binaries from [this page](http://hpc.sourceforge.net/) which had just updated their versions. Download gcc and gfortran for Yosemite. Then in the console run:

{% highlight bash %}
cd ~/Downloads
sudo tar -xvf gcc-5.0-bin.tar -C / 
sudo tar -xvf gfortran-5.0-bin.tar -C / 
{% endhighlight %}

* Step 2

Re-install the Apple developer tools for Yosemite. [Download](https://developer.apple.com/downloads/index.action#) and install the ones for OSX 10.10.

* Step 3

Now you are ready to re-install NONMEM. I used:

{% highlight bash %}
cd /Users/ronkeizer/Dropbox/Software/NONMEM/nm730CD_essential
sudo /bin/bash SETUP73 /Users/ronkeizer/Dropbox/Software/NONMEM/nm730CD_essential /opt/NONMEM/nm73g gfortran y ar same rec i
{% endhighlight %}

(But change the source and target folders to your own of course!)

* Step 4

Don't forget to update psn.conf if you installed to a new location. Use e.g.:

{% highlight bash %}
sudo nano /Library/Perl/5.16/PsN_4_2_0/psn.conf
{% endhighlight %}

to edit the system-wide configuration file or

{% highlight bash %}
nano ~/psn.conf
{% endhighlight %}

if you have a personal psn.conf file. Also, you might need to re-install some Perl modules for PsN:

{% highlight bash %}
sudo cpan -i Math::Random
sudo cpan -i Statistics::Distributions
{% endhighlight %}

* Step 5

To make Pirana work again, the only thing you need to do is re-install XQuartz, download [here](http://xquartz.macosforge.org/landing/)

That's all, folks!
