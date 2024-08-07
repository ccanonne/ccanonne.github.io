# [COLT 2021](http://www.learningtheory.org/colt2021/virtual/) Tutorial: Statistical Inference in Distributed or Constrained Settings
## Techniques and Recipes

⏰ _Tutorial time:_ [August 4, 18:30–21:30 Mountain Time](https://www.timeanddate.com/worldclock/converter.html?iso=20210805T003000&p1=224&p2=tz_mt&p3=179&p4=tz_gmt&p5=136&p6=195&p7=tz_ist&p8=tz_sgt&p9=tz_aet)

The goal of this tutorial is to provide the attendees with an overview of techniques and recipes for distributed estimation and testing under constraints. Over the recent years, many papers have obtained both upper and lower bounds for statistical
estimation under communication, local privacy, and memory constraints: these questions are motivated by applications in machine learning and distributed computing, and are at the intersection of theoretical
computer science, machine learning, statistics, and information theory.

This tutorial will provide a primer of those techniques, aiming to give both an understanding of the underlying challenges and ideas, and “plug-and-play” general recipes the attendees could then apply to the problems of their choice. Our focus will be on
establishing lower bounds for statistical estimation, in particular for parameter estimation (single- and high-dimensional) and testing. The tutorial will cover various models: nonadaptive, sequentially adaptive, blackboard model, and memory-constrained settings; with applications to high-dimensional parameter estimation and testing.

__Presenters:__ [Jayadev Acharya](https://people.ece.cornell.edu/acharya/), [Clément Canonne](https://ccanonne.github.io/), and [Himanshu Tyagi](https://ece.iisc.ac.in/~htyagi/)

__Recitation tutors__: [Aditya Vikram Singh](https://aditya-vs.github.io/), [Ziteng Sun](http://www.zitengsun.com/)

* 🧑‍🏫 _Tutorial_ 
  * Part 0 (15mn): Setting the stage: scope, models [📄 [slides for parts 0 and 1](slides-part01.pdf), 🎞️ [video](https://www.youtube.com/watch?v=LbkT9ujrKzY)]
  * Part 1 (45mn): Lower bounds for learning/estimation problems over discrete univariate domains, and some general upper bound techniques
  * Part 2 (45mn): Lower bounds for learning/estimation problems: generalisation to high dimensions [📄 [slides](slides-part2.pdf), 🎞️ [video](https://www.youtube.com/watch?v=ajvrb3d8GQo)]
* 📝 _Recitation_ (45mn) ([exercises](recitation.pdf), [solutions](recitation-solutions.pdf))
  * Mean estimation under local privacy or communication constraints: upper and lower bounds for product and Gaussian distributions
  * Extra exercises and applications: "Simulate-and-Infer," some sanity checks, and miscellaneous useful tricks.

📚 __Bibliography__: [available here](https://bibbase.org/show?bib=https%3A%2F%2Fccanonne.github.io%2Ftutorials%2Fcolt2021%2Fbibliography.bib&fullnames=1&theme=default) ([BibTex source](bibliography.bib))
