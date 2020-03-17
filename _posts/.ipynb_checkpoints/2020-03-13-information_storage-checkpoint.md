---
layout: post
title: "The Future of Information Storage is...Viruses?"
author: "Niko McCarty"
categories: blog
tags: [blog,coronavirus,covid-19,virus,viruses,information,storage,density,data]
image: covid-19.jpg
# sect: home
mathjax: true

---

The coronavirus outbreak has been a trying time. I'm obviously not an epidemiologist, or a virologist, or any other profession that might be considered useful during the weeks to come. I don't have advice to offer, or words of wisdom to follow. In an ongoing class at Caltech, called _Physical Biology of the Cell_, we were asked to consider the information storage capacity of different viruses -- a topic that I've decided to expand upon here. 

The question that I am asking is: "What is the information storage capacity, in terms of bits / volume, of different viruses? How does this compare to traditional storage mediums, e.g. CDs and hard drives?"

Fortunately, tackling this problem is not too difficult, because much of the data on viral genome sizes and dimensions is already known. In answering this question, I relied heavily upon the book _Cell Biology by the Numbers_, especially a section called ["How Big are Viruses?"](http://book.bionumbers.org/how-big-are-viruses/). This dataset provides the capsid architecture (icosahedral, roughly spherical, etc.) for different viruses, along with their genome size and genome type (single-stranded RNA, double-stranded DNA, etc.). We can use the given diameters to calculate the size of the "heads" on these viruses. In this problem, I will approximate _all_ of the viruses as roughly spherical, thus using the formula for the volume of a sphere,

$V_{sphere} = \frac{4}{3} \pi r^3$

![Bacteriophage, Adenovirus, and Retrovisur](../assets/img/viruses_wikimedia.png){:class="img-responsive"}

_Different viruses store their "genome" within an icosahedron, such as that seen for the bacteriophage (left) or store their genome within a roughly spherical "shell". Either way, I approximate all of these viral containers as spheres. [Image from Wikimedia, CNX OpenStax](https://commons.wikimedia.org/wiki/File:Figure_21_01_03.png)_



Next, we want to compute the "bits" stored by each virus. There are four bases in DNA and RNA...A, T, G, C (or A, U, G, C if RNA).

A could be represented as 00, T as 01, G as 10, and C as 11, for example. Thus, each base stores _two bits_ of information.

Let's now compute the "bits" of each virus, simply by multiplying the genome sizes by two.

Now, how many viruses do we need to store the entire Library of Congress? I have seen blog posts, from the [Library of Congress](https://blogs.loc.gov/thesignal/2011/07/transferring-libraries-of-congress-of-data/), no less, that repute the strangely circulated claim that the LoC holds a mere 10TB of data. In reality, the LoC holds something like 25 million books. Each book, when scanned, contains about 8Mb of data. Thus, there are roughly 200 million Mb of data in the Library of Congress, or about _200 terabytes_. 200 TB is 2e+11 kilobytes of data.

Now, the logical question is: What size volume of viruses do we need to store the entire Library of Congress? The calculation is simple...

The next part of this analysis is based on the notion of [areal density](https://en.wikipedia.org/wiki/Areal_density_(computer_storage)).

The [Stanford study](https://news.stanford.edu/news/2009/january28/small-012809.html) and [Columbia Study](https://science.sciencemag.org/content/355/6328/950) can be read by clicking on the names.

To compute the areal density of DNA from the Columbia study, I simply converted their reported value of "215 petabytes per gram of DNA" into "215 petabytes per X bases of DNA" by using the molar mass of a typical DNA base pair. To compute the area of these DNA bases, I used base pair dimension values from [BioNumbers](https://bionumbers.hms.harvard.edu/bionumber.aspx?&id=103777). I obtained a final calculated areal density of $1.85 \times 10^{12}$ $\frac{bits}{in^{2}}$

{% include 2020_03_05_viral_storage_capacity.html %}


{% include 2020_03_05_virus_library.html %}



{% include 2020_03_05_areal_density.html %}



"Interact with these graphs by zooming in, out. Hover over points to see more information."

Add a standard link to GitHub and Medium / etc

