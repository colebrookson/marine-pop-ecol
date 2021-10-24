---
permalink: /resources/
layout: single
title: Course Resources
excerpt: Refer to this page for links and short descriptions, videos, and references, to content and material that will help you as you navigate this course. 
author_profile: false
classes: wide
sidebar:
  nav: "Course Materials"
sidebar:
  nav: "Course Materials"
header:
  overlay_filter: 0.5
  overlay_image: /assets/images/ides.jpg
  caption: "Photo credit: Stack Overflow"
toc: true 
---

This section of the website will be continually updated with different links/descriptions/videos describing how to perform some of the essential skills you'll need for this course. Hopefully it will also act as a resource to you after this course is over. 


## Git/GitHub

In this class we use version control implemented through Git/GitHub. [Git](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F) is a mature, open source version control system developed by Linus Torvalds (who also developed the Linux operating system kernel), that interfaces with [GitHub](https://kinsta.com/knowledgebase/what-is-github/), an (unfortunately) for-profit company that acts as a git repository hosting service. Git is a command line-based tool, but GitHub, is the web-based graphical interface that lets us interact with our repositories. 

For our purposes, there are a few things you'll need:

1. A GitHub account - sign up [here](https://github.com/)
2. A version of Git installed on your computer. 
    **Please note: we will be using git from the command line. All demos/tutorials will be done from the command line. That means that if you choose to use a GUI alternative (e.g. GitHub desktop), you are more than welcome to do so, but we cannot help you troubleshoot problems.**
3. A working knowledge of a few simple git commands: `add`, `commit`, and `push`

If you have been using GitHub for a while, you'll notice you now need to set up your repositories using an `ssh` connection, not an `https`. For instructions on how to set up a secure ssh key, see this [documentation on the topic](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh). 

## RMarkdown

You will submit all of your assignments for this course in RMarkdown files, an interface between the programming language R, and the simple and yet powerful markdown language. If you are not familiar, check out the [introduction on the RMarkdown website](https://rmarkdown.rstudio.com/lesson-1.html) and check out this video:

<iframe src="https://player.vimeo.com/video/178485416" width="1200" height="900" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen=""></iframe>

## GitHub Classroom

This course uses GitHub Classroom to collaborate on and submit assignments. Submission instructions are specific to each assignment, but all include cloning, editing, and then commiting changes to a repository that we give you as a 'shell' repository to base yours off of. More information will be provided in the Git/GitHub lab and then posted here.  

## RStudio & General Helpful Links:

Some helpful tips & tricks to work more effectively in [RStudio](https://towardsdatascience.com/tips-and-tricks-in-rstudio-and-r-markdown-7a464508b0c)

Possibly the most useful resource, the [Big Book of R](https://www.bigbookofr.com) is a comprehensive collection of books about/for/involving/referencing R, and includes everything from the basics to in-depth full volumes on dynamic programming in R

## An aside on Packages -- To use Base or Tidy (or data.table)?

There are a million discussions on whether or not to use Base R or TidyR. Keep in mind that a lot of these are written by the people who work at RStudio, who are amazing and do great work in R education, but also are the ones who built and maintain the tidyverse, so the opinion you will get from them should be interpreted with that in mind. Here's a [good even-handed discussion](https://wetlandscapes.com/blog/a-comparison-of-r-dialects/) of the various merits, but also more importantly a comparison of the different ways to do things.

My favourite [blog](https://www.r-bloggers.com/2019/12/why-i-dont-use-the-tidyverse/) on why to use Base R. I (Cole) used to be an *ardent* believer in the Tidyverse, and I still use it for most of my day to day work, but this blog convinced me to think about teaching Base R and I think there are some great points made here.

For the sake of even-handedness, here is a [blog](https://www.r-bloggers.com/2018/09/why-learn-the-tidyverse/#:~:text=Why%20is%20Tidyverse%20so%20popular,build%20an%20ecosystem%20of%20applications.) that believes Tidyverse is the way to go. 

As with everything in programming, there are many ways to do things. Arguing about which way is better is usually less helpful than picking the right tool for the specific job and executing it rigorously. 

## Using iNaturalist

In the course, for species ID we will be using the popular and user-friendly identification tool, [iNaturalist](https://www.inaturalist.org/pages/getting+started). This software works most usefully as an app on your phone that you download and use to photograph and identify organisms. 

There is an excellent series of videos that iNaturalist put out helping new users get up to speed with their app and usage:

<iframe src="https://player.vimeo.com/video/162581545?h=c4adb054f2" width="1200" height="900" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

## Matrix Math in Latex and Matrix Analysis in R

A summary of our class lecture/live-coding session on writing Latex, and doing simple matrix analysis in `R`. 

<embed src="https://colebrookson.github.io/marine-pop-ecol/lectures/matrix-math.pdf" type="application/pdf" width=2000 height=2800/>