# Error bars lab meeting presentation

error_bars.Rmd - source file containing all text & code for the presentation. You may need to install some new R packages to run the code (see the `library()` commands early in the file). The file should run and compile quickly, in a few seconds.

error_bars.html - compiled slides used for presentation.

## Misc notes

Standard deviation: would not change if we collect more data, as sample size increases, we would get closer to the population variability. As N increases, we are summing over more deviations, but we also account for it in N-1. 
Standard error (of the mean): shrinks because of division by sqrt N. We have a population, and we obtain samples, we can compute the mean. If we take larger and larger samples, the means are going to be more and more similar across repeated measures. I.e. standard error of the mean quantifies uncertainty in the population mean given the data at hand. How variable would the sample means be if you were to do this over and over again? 
Central limit theorem: IID samples will approximate a normal distribution with std being equal to the standard error. 
The simplest link between standard error and CI: Mean +- 1.96 standard error will approximate the 95% CI.

**Inference about differences in populations?**
~If error bars don't overlap, the means are significantly different. When does this hold? 
We need to take into account how many observations went into the error bar.
Which inference can we draw about error bars within 2 conditions?
If they DON'T overlap, we are safe. If we have (1-alpha) confidence interval do not overlap, we know that with (1-alpha) that the underlying means are different! Bayesian stats: usually the error bars show the 95% of the probability mass. Each posterior distribution has 5% probability mass left. The most probable that it could be that those two are not distinct would be if the remaining 5% are on opposite sides... I.e. from non-overlap, we can conclude 1-alpha confidence in difference between conditions. 
If two confidence intervals do overlap, that does not mean that you cannot conclude that the means are not different. So we can have a lot of overlap, but still get significant different means! Because of paired t-test ! I.e. we take the differences within participant. We take the direction into account. BUT the error bars did not! If we just took the differences in the spaghetti plot, we could plot the CI and if that does not overlap with zero, the difference would be significant. 
Loftus & Masson 1994: We can subtract out each subject's mean from that subject's data in all conditions. They argued that between-subject variance typically plays no role in statistical analyses. Between subject differences are subtracted out in the paired t-test. 
The estimate of the mean cannot really be inferred because we throw away the between subject variance. 

**Item effects**
Items are different, i.e. observations are not IID and therefore naive standard errors and CIs would be invalid. 
We can compute the subject-level means, and then compute the error over that. 
IF we don't take into account groupings, we might be overly confident.
We can use LMEs to code hierarchies. 

