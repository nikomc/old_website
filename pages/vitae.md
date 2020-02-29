---
layout: misc
title: Vitae
---

<div style="width: 75%; margin: auto">

## Education

**B.Sc. Biochemistry** - with certificate in Clinical & Translational Science (Honors, University Honors, High Distinction), University of Iowa, *2017*<br/>
**MRes Systems and Synthetic Biology** - Imperial College London, *2018*<br/>
**Ph.D. Bioengineering**, California Institute of Technology, *expected 2024* 
<div style="padding-left: 1em; margin-top:-0.5em;">
<i>Thesis topic:</i> Predicting evolution and high-throughput, quantitative tools for biophysics 
<br/>
<i>Thesis adviser:</i> Professor Rob Phillips
</div>


## Publications
<sup>**☭** </sup> indicates equal contribution


Research:
Graduate Student, Caltech, PI: Rob Phillips 2018-present

Masters Student, Imperial College, PIs: Rodrigo Ledesma-Amaro & Tom Ellis 2017-2018
-Project: Control of metabolic flux in yeast and assembly systems for the multiplexing of gRNAs in vivo.

Co-Founder/Co-Leader, Iowa iGEM 2017
-Project: Development of a biosensor for direct 3-hydroxypropionate detection in B. subtilis. 
-First iGEM team from the University of Iowa. As a team of 12 students, we fundraised $17k, set up a lab space and developed a biosensor.  A lab course is now offered by our faculty mentors in synthetic biology, the first of its kind on campus.

Undergraduate Research Assistant, PI: E. Dale Abel, MD, PhD, 2013-2017
-Project 1: Elucidate the mechanism by which heart failure occurs in mice lacking Insulin Receptor Substrates (IRS) 1 and 2
-Project 2: Determine the mechanism by which murine cardiomyocyte glucose transporter expression is regulated in the context of a high-fat diet

Publications:
McCarty NS, Graham AE, Studena L and Ledesma-Amaro R. Multiplexed CRISPR technologies for gene editing and transcriptional regulation. Nature Communications (2020).

Riehle C, Weatherford ET, Wende AR, Jaishy BP, Seei AW, McCarty NS, Rech M, Shi Q, Reddy GR, Kutschke WJ, Oliveira K, Pires KM, Anderson JC, Diakos NA, Weiss RM, White MF, Drakos SG, Xiang YK and Abel ED. Insulin Receptor Substrates Differentially Exacerbate Insulin-Mediated Left Ventricular Remodeling. JCI Insight (2020).

McCarty NS, Shaw WM, Ellis T and Ledesma-Amaro R. Rapid Assembly of gRNA Arrays via Modular Cloning in Yeast. ACS Synthetic Biology (2019). Plasmids on Addgene.

McCarty NS and Ledesma-Amaro R. Synthetic Biology Tools to Engineer Microbial Consortia for Biotechnology. Trends in Biotechnology (2019).
         -Also featured in Trends Collection on Communication.

Riehle C, Scharf GM, Sieweke JT, Zauner F, Flierl U, Treptau J, Zormpas C, Senf J, McCarty NS, Bauersachs J, Sedding DG and Westhoff-Bleck M. Leukocytoclastic Vasculitis Associated with Endocarditis in a Patient with Transposition of the Great Arteries and Mechanical Valve Replacement. Cardiovascular Pathology. 2017 Jan 23. http://dx.doi.org/10.1016/j.carpath.2017.01.005

Selected Honors:
2019 Pilot Grant, Center for Environmental Microbial Interactions at Caltech
2018 Outstanding Student of the Year in Synthetic Biology (top marks in course)
2018 Barzun Prize for Youth Engagement
2017 Fulbright - Imperial College London Partnership Award
2017 Fellow, Royal Society of Arts
2017 Honors at Iowa Scholar Award
2017 Joseph E. and Ursil I. Callen Prize
2017 Montgomery Biochemistry Scholar's Prize
2016 Barry Goldwater Scholar
2015 Endocrine Society Summer Research Fellowship
2015 American Heart Association Summer Research Fellowship (declined offer)
</div>

{% for post in site.categories.cv %}
  <a href="{{ site.github.url }}{{ post.url }}">
    <div class="featured-posts" {% if post.image %}style="background-image:url({{ site.github.url }}/assets/img/{{ post.image }})"{% endif %}>
      <h2><span>{{ post.title }}</span></h2>
    </div>
  </a>
{% endfor %}


