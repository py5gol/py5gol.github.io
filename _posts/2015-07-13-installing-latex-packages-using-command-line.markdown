---
layout: post
title:  "Installing latex packages using the command line tool"
date:   2014-03-15 22:10:37
categories: latex
---

I have been using Latex for some time, but I'm certainly not an expert. Partially because I spent a lot of time comparing the alternatives available and avoid going deep on any of them.

After some flirting with markdown and pandoc, I decided to give a try again to latex to organize my writing activity. Since I started working on research, most of my writing includes lots of references and having a good tool to help me with it is important. After a bit of research, I discovered that BibTeX, the traditional solution from referencing, has alternatives such as biblatex. The changing process took a few hours since some details should be better-explained, and I had to gather information from many sites.

One of the problems I faced was a missing package. I could install the operating system package (Debian, apt-get), but some of the LaTex packages are huge (texlive-extra is around 300MB). So, I finally decided to look for the latex package manager (tlmgr).

The tlmgr works similar to other package managers such as apt (Debian), pip (Python), etc. So, to install a package, one just need to type.

{% highlight ruby %}
tlmgr install <package>
{% endhighlight %}

Simple like that, from now on, every time I need a package, I can just type tlmgr install + the name of the package.

Cheers
