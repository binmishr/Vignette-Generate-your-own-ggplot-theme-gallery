# Vignette-Generate-your-own-ggplot-theme-gallery

The details of the codeset and plots are included in the attached Adobe Acrobat reader (.pdf) file in this repository. 
You need to download the same to view the contents. There are referrals to other contents in BLUE colour also to follow.

A Brief Introduction
======================

DIY ggplot theme gallery
===========================
1. Start with a list of plots and a list of themes

The outcome I want to achieve from this is to create something that would make it easier to decide which ggplot theme to pick for the visualisation at hand. The solution doesn’t need to be fancy: it would be helpful enough to generate all the combinations of plot types X themes, so I can browse through them and get inspirations more easily.

I took a leaf out of Shayne Lynn’s book/blog and created a couple of “base plots” using iris (yes, boring, but it works). I did these for four types of plots:

    scatter plot
    bar plot
    box plot
    density plot

I then assigned these four plots into a list object called plot_list, and converted them into a tibble (plot_base) that I could use for joining afterwards.

This step is then repeated for themes, where I virtually punched in all the existing themes in {ggplot2} and {ggthemes} into a named list (theme_list), and also create a tibble (theme_base). You can make this list as long and exhaustive as you want, but for this example I didn’t want to go into overkill.

You’ll see that I’ve made the names quite elaborate in terms of specifying the package source. The reason for this is because these names will be used afterwards in the plot output, and it will be helpful for identifying the function for generating the theme in the gallery.

