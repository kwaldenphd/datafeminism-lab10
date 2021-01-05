# Getting Started with Statistics in R/RStudio

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Acknowledgements

Lab procedures for this week come from [Dr. Yibi Huang’s](http://www.stat.uchicago.edu/~yibi/) (Statistics, University of Chicago) Fall 2017 [Statistical Methods and Applications course](http://www.stat.uchicago.edu/~yibi/teaching/stat220/17aut/) ([STAT 220 labs](http://www.stat.uchicago.edu/~yibi/s220/labs/)).

Additional documentation, including definitions and additional resources, for this lab come from Danielle Navarro, [*Learning Statistics With R: A Tutorial for Psychology Students and Other Beginners*](https://learningstatisticswithr.com/book/) (2019).

# Table of Contents
- [Overview](#overview)
  * [How to approach this lab](#how-to-approach-this-lab)
  * [Definitions](#definitions)
- [Option 1: Exploring Numerical Data](#option-1-exploring-numerical-data)
- [Option 2: Exploring Categorical Data](#option-2-exploring-categorical-data)
- [Option 3: Normal Distributions](#option-3-normal-distributions)
- [Option 4: Linear Regression](#option-4-linear-regression)
- [But what about text?!?](#but-what-about-text)

# Overview

[Link to lab overview video in Panopto (ND users only)](https://notredame.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=9cf6097a-1733-4882-a59c-ac9a013f8568)

## How to approach this lab

This lab will be different than how we've approached previous labs. 

The level of mathematics/statistics training across our class varies WIDELY--some folks are ACMS majors, others are coming from American Studies, Gender Studies, etc. Thus, there are four options or "tracks" for this lab. My goal across all of those tracks is for you to have the opportuntity to gain experience working with statistical concepts in R/RStudio. 

First step is to choose an option/track based on your level of familiarity or proficiency with the underlying statistical concepts covered. To be clear--this IS NOT a statistics class, I am not a mathematician/statistician, and the goal of this lab is not "surprise! teach yourself statistics in a week."

But for folks who do have more advanced background/training/knowledge in mathematics and statistics, this lab is an opportunity to explore how we engage those underlying concepts and express them programatically in the R/RStudio environment.

In short--go with the math you know. 

Another key consideration is that this is what I would call a "stretch" lab, in the sense that it is asking you to engage with and apply concepts that we have not covered in a systematic way over the course of the semester. (I'll say again, this is not a statistics-focused data science class, and I am not a mathematician/statistician.) Feeling confused, overwhelmed, frustrated, unclear, etc. are all normal experiences to have when working on this lab.

To that end, I've outlined a few definitions below, each lab procedure includes examples and guided prompts. And for the labs that have significant additional exercises or questions that go beyond what's explicitly covered in the procedure, those are not required elements of the lab notebook (see the "Lab notebook deliverables" section under each option/track). Each lab option/track has links to extensive additional resources from Danielle Navarro's book [*Learning Statistics With R: A Tutorial for Psychology Students and Other Beginners*](https://learningstatisticswithr.com/book/) (2019).

**BUT, I want to reiterate** the goal of this lab is not "surprise! teach yourself statistics in a week." The average amount of time you would normally spend on one of our labs is all that you are expected to devote to this lab. If that means the notebook is only partially completed or there are exercises/questions or you struggle with, that's okay (and frankly, I am expecting this!). I'll say again--whatever amount of time you normally spend on our labs is what you should expect to spend here, regardless of the impact that has on how much of the procedure/questions you're able to get through. This lab should be a challenge or "stretch." It is not intended to be a massive time suck.

## Definitions

**Numerical data:** data that includes some type of measurement. This can include discrete or continuous measures. Discrete measures are numbers or values that can be counted, or listed out. Continuous measures are numbers that cannot be counted or described using intervals on a number line (i.e. speed, weight, age, etc).

**Categorical data:** data that represents characteristics or attributes. Categorical data can include numerical values (i.e. `1` indicating `yes` and `2` indicating `no`), but in that case the numbers do not have mathematical meaning.

**Ordinal data:** data that includes both numerical and categorical data. Data exists in categories and the category numbers have meaning (i.e. responses on a likert rating scale, such as `0` indicating the lowest value and `5` indicating the highest value).

**Univariate data:** data that includes one variable or type.

**Bivariate data:** data that includes two variables or types.

**Multivariate data:** data that includes at least two variables or types.

**Descriptive statistics:** statistics used to describe basic features of dataset or object. Contrasts with inferential statistics, which include conclusions beyond the values represented in the immediate or original dataset. 

**Mean, median, mode, and range:**
- mean: average value in a set of values
- median: middle value in a set of values (sorted numerically)
- mode: value repeated most often in a set of values
- range: smallest value in a set subtracted from the largest value

Example, using the following set of values: `13, 18, 13, 14, 13, 16, 14, 21, 13`
- mean: 15
  * `(13 + 18 + 13 + 14 + 13 + 16 + 14 + 21 + 13) ÷ 9 = 15`
- median: 14
  * `list in numerical order: 13, 13, 13, 13, 14, 14, 16, 18, 21`
  * `(9 + 1) ÷ 2 = 10 ÷ 2 = 5th number`
- mode: 13
- range: 8
  * `21 - 13 = 8`

**Correlation:** statistical measure expressing the relationship between two variables. Most often used to describe extent to which two variables have a linear relationship.

**Regression:** statistical method used to estimate the relationship between two variables. Linear regression finds a line (or linear relationship) between a dependent and independent variable. In regression analysis, dependent variables are sometimes called the "outcome variable," while independent variables are sometimes called the "predictor variable."

# Option 1: Exploring Numerical Data

**[Link to lab procedure](http://www.stat.uchicago.edu/~yibi/s220/labs/lab02.html)**

**Statistical concepts covered:** mean, median, standard deviation, variance, quartiles, interquartile range, min, max

**Visualization types covered:** histograms, boxplots, scatterplots

**Lab notebook deliverables:**
- RScript file that includes your process/progress working through the lab steps.
- Brief summary (or summary comments throughout the lab) that describe challenges you faced and key takeaways.

**Resources:**

Danielle Navarro, [*Learning Statistics With R: A Tutorial for Psychology Students and Other Beginners*](https://learningstatisticswithr.com/book/) (2019).

Chapter 5 [Descriptive Statistics](https://learningstatisticswithr.com/book/descriptives.html)
- 5.1 [Measures of Central Tendency](https://learningstatisticswithr.com/book/descriptives.html#centraltendency)
  * 5.1.1 [The mean](https://learningstatisticswithr.com/book/descriptives.html#mean)
  * 5.1.3 [The median](https://learningstatisticswithr.com/book/descriptives.html#median)
- 5.2 [Measures of variability](https://learningstatisticswithr.com/book/descriptives.html#var)
  * 5.2.1 [Range](https://learningstatisticswithr.com/book/descriptives.html#range)
  * 5.2.2 [Interquartile range](https://learningstatisticswithr.com/book/descriptives.html#interquartile-range)
  * 5.2.4 [Variance](https://learningstatisticswithr.com/book/descriptives.html#variance)
  * 5.2.5 [Standard deviation](https://learningstatisticswithr.com/book/descriptives.html#sd)

Chapter 6 [Drawing graphs](https://learningstatisticswithr.com/book/graphics.html)
- 6.2 [An introduction to plotting](https://learningstatisticswithr.com/book/graphics.html#introplotting)
- 6.3.1 [Visual style of your histogram](https://learningstatisticswithr.com/book/graphics.html#visual-style-of-your-histogram)
- 6.5.1 [Visual style of your boxplot](https://learningstatisticswithr.com/book/graphics.html#visual-style-of-your-boxplot)
- 6.6 [Scatterplots](https://learningstatisticswithr.com/book/graphics.html#scatterplots)

# Option 2: Exploring Categorical Data

**[Link to lab procedure](http://www.stat.uchicago.edu/~yibi/s220/labs/lab03.html)**

**Statistical concepts covered:** mean, median, standard deviation, variance, min/max, range, interquartile range, sample frequency, relative frequency distribution

**Visualization types covered:** boxplots, histograms, bar plots/charts, mosaic plots

**Lab notebook deliverables:**
- PART 6 EXERCISES NOT REQUIRED
- RScript file that includes your process/progress working through the lab steps
- Documentation for five exercises included in the lab
- Brief summary (or summary comments throughout the lab) that describe challenges you faced and key takeaways.

**Resources:**

Danielle Navarro, [*Learning Statistics With R: A Tutorial for Psychology Students and Other Beginners*](https://learningstatisticswithr.com/book/) (2019).

Chapter 5 [Descriptive Statistics](https://learningstatisticswithr.com/book/descriptives.html)
- 5.1 [Measures of Central Tendency](https://learningstatisticswithr.com/book/descriptives.html#centraltendency)
  * 5.1.1 [The mean](https://learningstatisticswithr.com/book/descriptives.html#mean)
  * 5.1.3 [The median](https://learningstatisticswithr.com/book/descriptives.html#median)
- 5.2 [Measures of variability](https://learningstatisticswithr.com/book/descriptives.html#var)
  * 5.2.1 [Range](https://learningstatisticswithr.com/book/descriptives.html#range)
  * 5.2.2 [Interquartile range](https://learningstatisticswithr.com/book/descriptives.html#interquartile-range)
  * 5.2.4 [Variance](https://learningstatisticswithr.com/book/descriptives.html#variance)
  * 5.2.5 [Standard deviation](https://learningstatisticswithr.com/book/descriptives.html#sd)

Chapter 6 [Drawing graphs](https://learningstatisticswithr.com/book/graphics.html)
- 6.2 [An introduction to plotting](https://learningstatisticswithr.com/book/graphics.html#introplotting)
- 6.3.1 [Visual style of your histogram](https://learningstatisticswithr.com/book/graphics.html#visual-style-of-your-histogram)
- 6.5.1 [Visual style of your boxplot](https://learningstatisticswithr.com/book/graphics.html#visual-style-of-your-boxplot)
- 6.6 [Scatterplots](https://learningstatisticswithr.com/book/graphics.html#scatterplots)
- 6.7 [Bar graphs](https://learningstatisticswithr.com/book/graphics.html#bargraph)

# Option 3: Normal Distributions

**[Link to lab procedure](http://www.stat.uchicago.edu/~yibi/s220/labs/lab05.html)**

**Statistical concepts covered:** probability distributions, normal distributions, percentiles

**Visualization types covered:** histograms, probability plots

**Lab notebook deliverables:**
- RScript file that includes your process/progress working through the lab steps
- Documentation for five exercises included in the lab
- Responses to the “On Your Own” section questions
- Brief summary (or summary comments throughout the lab) that describe challenges you faced and key takeaways.

**Resources:**

Danielle Navarro, [*Learning Statistics With R: A Tutorial for Psychology Students and Other Beginners*](https://learningstatisticswithr.com/book/) (2019).

Chapter 9 [Introduction to Probability](https://learningstatisticswithr.com/book/probability.html)
- 9.3 [Basic probability theory](https://learningstatisticswithr.com/book/probability.html#basicprobability)
  * 9.3.1 [Introducing probability distributions](https://learningstatisticswithr.com/book/probability.html#introducing-probability-distributions)
- 9.5 [The normal distribution](https://learningstatisticswithr.com/book/probability.html#normal)

Chapter 6 [Drawing graphs](https://learningstatisticswithr.com/book/graphics.html)
- 6.2 [An introduction to plotting](https://learningstatisticswithr.com/book/graphics.html#introplotting)
- 6.3.1 [Visual style of your histogram](https://learningstatisticswithr.com/book/graphics.html#visual-style-of-your-histogram)

# Option 4: Linear Regression

**[Link to lab procedure](http://www.stat.uchicago.edu/~yibi/s220/labs/lab10.html)**

**Statistical concepts covered:** linear models, correlation coefficients, sum of squared residuals, regression line, regression models

**Visualization types covered:** regression plots, linear model plots, histograms, xy plots

**Lab notebook deliverables:**
- ON YOUR OWN EXERCISES NOT REQUIRED
- RScript file that includes your process/progress working through the lab steps
- Documentation for seven exercises included in the lab
- Brief summary (or summary comments throughout the lab) that describe challenges you faced and key takeaways.

**Resources:**

Danielle Navarro, [*Learning Statistics With R: A Tutorial for Psychology Students and Other Beginners*](https://learningstatisticswithr.com/book/) (2019).

Chapter 5 [Descriptive Statistics](https://learningstatisticswithr.com/book/descriptives.html)
- 5.7 [Correlations](https://learningstatisticswithr.com/book/descriptives.html#correl)
  * 5.7.3 [The correlation coefficient](https://learningstatisticswithr.com/book/descriptives.html#the-correlation-coefficient)
  * 5.7.4 [Calculating correlations in R](https://learningstatisticswithr.com/book/descriptives.html#calculating-correlations-in-r)
  * 5.7.5 [Interpreting a correlation](https://learningstatisticswithr.com/book/descriptives.html#interpretingcorrelations)
  * 5.7.7 [The `correlate()` function](https://learningstatisticswithr.com/book/descriptives.html#the-correlate-function)

Chapter 6 [Drawing graphs](https://learningstatisticswithr.com/book/graphics.html)
- 6.2 [An introduction to plotting](https://learningstatisticswithr.com/book/graphics.html#introplotting)
- 6.3.1 [Visual style of your histogram](https://learningstatisticswithr.com/book/graphics.html#visual-style-of-your-histogram)
- 6.5.1 [Visual style of your boxplot](https://learningstatisticswithr.com/book/graphics.html#visual-style-of-your-boxplot)
- 6.6 [Scatterplots](https://learningstatisticswithr.com/book/graphics.html#scatterplots)

Chapter 15 [Linear Regression](https://learningstatisticswithr.com/book/regression.html)
- 15.1 [What is a linear regression model?](https://learningstatisticswithr.com/book/regression.html#introregression)
- 15.2.1 [Using the `lm()` function](https://learningstatisticswithr.com/book/regression.html#lm)

# But what about text?!?

This lab (and the majority of our labs this semester) have focused on working with structured numerical and categorical data in R/RStudio. There is a whole other universe of things you can do in R/RStudio (as well as Python) for different kinds of analysis using unstructured textual data. This kind of analysis can be described a number of different ways: natural language processing (NLP), text analysis, computational linguistics, distant reading, among other terms.

If you're interested in learning more about these methods, a number of different resources that can get you started...

Tutorials:
- [Basic Text Processing in R](https://programminghistorian.org/en/lessons/basic-text-processing-in-r) *Programming Historian*
- [Corpus Analysis with Antconc](https://programminghistorian.org/en/lessons/corpus-analysis-with-antconc) *Programming Historian*
- [Getting Started with Topic Modeling and MALLET](https://programminghistorian.org/en/lessons/topic-modeling-and-mallet) *Programming Historian*
- [R for Social Scientists](https://datacarpentry.org/r-socialsci/) *Data Carpentry*
- [Humanities Data in R Workshop materials](https://github.com/statsmaths/uwm-humanities-data-r) (Taylor Arnold and Lauren Tilton, University of Richmond)
- [More distant reading tutorials from *Programming Historian*](https://programminghistorian.org/en/lessons/?topic=distant-reading)

GitHub repositories:
- [Multilingual Natural Language Processing Resources](https://github.com/multilingual-dh/nlp-resources) (Quinn Dombrowski, Stanford)
- [cleanNLP: A Tidy Data Model for Natural Language Processing](https://github.com/statsmaths/cleanNLP) (Taylor Arnold, University of Richmond)

Syllabi:
- ["Digital Humanities Across Borders" textual analysis syllabus](https://github.com/quinnanya/dlcl204) (Quinn Dombrowski, Stanford)
- ["Practical Approaches to Data Science With Text" syllabus](https://github.com/laurenfklein/emory-qtm340) (Lauren F. Klein, Emory)
- ["Computational Social Science" syllabus](https://github.com/laurenfklein/gt-css-class) (Lauren F. Klein, Georgia Tech)

Additional resources:
- [Chapter 11, "Text"](https://statsmaths.github.io/eds_book/text.html) from Taylor Arnold's [*Exploratory Data Analysis* in-progress book](https://statsmaths.github.io/eds_book/index.html).
- [McGill University .txtLAB blog](https://txtlab.org/)
- Johanna Drucker, "Why Distant Reading Isn't," *PMLA 132, 3* (2017): 628-635. https://doi.org/10.1632/pmla.2017.132.3.628. 
  * [Link to access through Hesburgh Libraries](https://onesearch.library.nd.edu/permalink/f/7uudnk/TN_gale_ofa511153638)
- [*Journal of Cultural Analytics*](https://culturalanalytics.org/)
- Ted Underwood, *Distant Horizons: Digital Evidence and Literary Change* (University of Chicago Press, 2019). [Link to access through Hesburgh Libraries](https://onesearch.library.nd.edu/permalink/f/1phik6l/ndu_aleph005323126)
- [Ted Underwood's blog "The Stone and the Shell"](https://tedunderwood.com/) 
