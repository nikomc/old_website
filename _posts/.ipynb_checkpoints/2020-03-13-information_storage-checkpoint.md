---
layout: post
title: "The Future of Information Storage is...Viruses?"
author: "Niko McCarty"
categories: blog
tags: [blog,coronavirus,covid-19,virus,viruses,information,storage,density,data]
image: covid-19.jpg
sect: home
mathjax: true

---
The coronavirus outbreak has been a trying time. I'm obviously not an epidemiologist, or a virologist, or any other profession that anyone should turn to for advice in the weeks to come. I don't have insights to offer, or words of wisdom to follow. I'm just a scientist that is interested in viruses -- especially their remarkable ability to pack a _huge_ punch in a tiny little capsule, a feature that we are observing in real time.

This winter, I was enrolled in a class at Caltech called _Physical Biology of the Cell_. One of our homework problems asked us to consider the information storage capacity of different viruses, a topic that I've decided to expand upon in this inaugural blog post. While I have heard about DNA storage for a long time, it is only through exploring the data directly that I came to appreciate the massive theoretical information storage density that is possible with DNA.

The question that I want to answer, specifically, is: **"What is the information storage capacity, in terms of kilobytes / volume, of different viruses? How does this compare to traditional storage mediums, e.g. CDs and hard drives?"**

Fortunately, tackling this problem is not too difficult, because much of the data on viral genome sizes and dimensions are already known. In answering this question, I relied heavily upon the book _Cell Biology by the Numbers_, especially a section called ["How Big are Viruses?"](http://book.bionumbers.org/how-big-are-viruses/). This dataset provides the capsid architecture (icosahedral, roughly spherical, etc.) for different viruses, along with their genome size and genome type (single-stranded RNA, double-stranded DNA, etc.). I used the given diameters for each virus to calculate the size of their head or capsid, the part of the virus that stores the genome. In these calculations, I approximated _all_ of the viruses as roughly spherical, thus using the formula for the volume of a sphere ($V_{sphere} = \frac{4}{3} \pi r^3$) in my estimates.

![Bacteriophage, Adenovirus, and Retrovirus](../assets/img/viruses_wikimedia.png){:class="img-responsive"}

_Viruses come in different shapes and sizes. [Image from Wikimedia, CNX OpenStax](https://commons.wikimedia.org/wiki/File:Figure_21_01_03.png)_

To calculate "bits per volume" for each virus, I used the simple idea that each base of DNA contains two bits of information. In other words, DNA consists of four bases -- adenine, cytosine, guanine and thymine -- and each of these bases can encode 00, 11, 01, or 10. Thus, calculating bits of information per virus simply demands that we multiply genome sizes by two.

![DNA Structure](../assets/img/DNA_structure.png){:class="img-responsive"}
_DNA is a polymer consisting of four different molecules (or bases): adenine, thymine, cytosine and guanine. [Image by Madeleine Price Ball](https://commons.wikimedia.org/wiki/File:DNA_chemical_structure.svg)_

I used [Pandas](https://pandas.pydata.org/) to store information about each virus and compute volumes and kilobytes of information stored (I even included Covid-19, based on viral dimensions taken from microscopy images, just for fun!). There are 8000 bits in a kilobyte, and the computed values are presented in the simple graph below. Hover over a point to see additional information.

{% include 2020_03_05_viral_storage_capacity.html %}

This data, in itself, is not super interesting. We can see that lambda phage has a decently high storage density, as does herpes simplex virus, but the more interesting question, really, is:

**What volume of viruses would be required to store all 25 million books in the Library of Congress?**

That's quite a loaded question, and it warrants some analysis. 

How much information is actually stored in the Library of Congress? There have been numerous websites and articles that claim that the Library of Congress holds about 10TB of information. But Nicholas Taylor, from the [Library of Congress' Web Archiving Team](https://blogs.loc.gov/thesignal/2011/07/transferring-libraries-of-congress-of-data/), refutes this claim. Instead, he argues that the Library of Congress holds 25 million books, and if one assumes that each _scanned_ book contains about 8 megabytes of data, then there should be approximately 200 million megabytes, or about 200 terabytes, of information in the Library of Congress. 200 TB is $2 \times 10^{11}$ kilobytes of data.

To calculate the number of viruses needed to store that vast amount of information, we can simply divide 200 terabytes by the information storage capacity of different viruses. To compute the volume of viruses needed to store 200 terabytes, we can use our previous calculations, using the information storage capacities of different viruses in terms of their volume ($\mu m^3$).

My calculations for this second question are shown in the figure below which, again, is interactive.

{% include 2020_03_05_virus_library.html %}

If we _actually_ wanted to store all of the information in the Library of Congress, then, it appears that the herpes virus or lambda phage (the most information dense viruses from our previous plot) would be the best bet. They offer the highest information storage capacity in the smallest volume. The herpes virus, for example, could store the entire Library of Congress in a volume smaller than $6 \times 10^{6}$ $\mu m^3$, or $6 \times 10^{-12}$ $m^3$. For context, that is about **five orders of magnitude smaller than a drop of water**. It is unbelievably, almost impossibly, tiny. 

If information storage in DNA has such great potential, why isn't it in computers today? The answer, in short, is because it is terribly difficult to retrieve information from DNA in a cost-effective, rapid manner. DNA is incredibly stable, and it is becoming ever simpler to build, thanks to a plethora of DNA synthesis companies. But retrieval and other aspects of the technology remain difficult or cost-intensive. Thus, these calculations remain largely speculative for now. 

So how does DNA information storage stack up to modern and historical computer hardware? CDs, Blu-Ray discs, hard drives, and that sort of thing? Well, computer storage is largely quantified and assessed based on its [areal density](https://en.wikipedia.org/wiki/Areal_density_(computer_storage)). Stretching back to the 1950s, the areal density of a hard drive has accelerated according to [Moore's Law](https://en.wikipedia.org/wiki/Moore%27s_law).

To explore DNA storage versus canonical computer storage, I calculated the bits per area for many different storage devices, including the 1956 IBM 350, the Univac Uniservo magnetic tape, DVDs, CDs, and some modern hard drives. I compared the areal densities of these devices with a DNA storage system reported in 2017 by scientists at Columbia University (called a [DNA Fountain](https://science.sciencemag.org/content/355/6328/950), which enabled the research team to retrieve a remarkable 215 petabytes per gram of DNA). Also, in 2009, physicists at [Stanford University](https://news.stanford.edu/news/2009/january28/small-012809.html) demonstrated a method to print letters as small as 0.3 nanometers -- "one-third of a billionth of a meter" -- using a method that enables, to my knowledge, the highest areal density of any information storage medium. All of the computed areal densities are presented in the graph below, which was made using Altair. A sample code block is shown at the end of this post.

{% include 2020_03_05_areal_density.html %}

To compute the areal density of DNA from the Columbia study, I simply converted their reported value of "215 petabytes per gram of DNA" into "215 petabytes per X bases of DNA" by using the molar mass of a typical DNA base pair. To compute the area of DNA bases, I used base pair dimension values from [BioNumbers](https://bionumbers.hms.harvard.edu/bionumber.aspx?&id=103777). I obtained a final calculated areal density of $1.85 \times 10^{12}$ $\frac{bits}{in^{2}}$. I was completely shocked to find that this value is very similar to the areal density of a modern Seagate hard drive (2015). In the years to come, however, I expect that DNA information storage capacities will outstrip electrical systems.

Scientists continue to make important strides towards practical DNA and quantum-based information storage devices. To keep up with Moore's Law, drastic developments are certainly needed. Biology, and viruses, may offer a solution.

____________________________________________________________

To make this final graph, I am using Altair in Jupyter notebooks. The [Altair](https://altair-viz.github.io/index.html) package is very straightforward. It calls upon data stored in Pandas DataFrames to make quick, interactive visualizations.


{% highlight python %}
import altair as alt
import pandas as pd

points = alt.Chart(df).mark_circle(size=100).encode(
    alt.X('storage capacity (bit/in^2)', scale=alt.Scale(type='log'), axis=alt.Axis(title='Areal Density (bits per square inch)')),
    color=alt.condition(single, 'name', alt.value('lightgray'))
).add_selection(
    single
).interactive()

text = alt.Chart(df).mark_text(dx=-5, align='right').encode(
    x='storage capacity (bit/in^2):Q',
    text='name',
    opacity=alt.condition(single, alt.value(1.0), alt.value(0.0))
)
points + text
{% endhighlight %}

I hope that you enjoyed this brief exploration of viral information storage. All of my Jupyter notebooks can be found in one of my [GitHub](https://github.com/nikomc/Interactives_Python) repositories.

