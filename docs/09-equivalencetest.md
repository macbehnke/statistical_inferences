



# Equivalence Testing and Interval Hypotheses {#equivalencetest}

Most scientific studies are designed to test the prediction that an effect or a difference exists. Does a new intervention work? Is there a relationship between two variables? These studies are analyzed with a commonly analyzed with a null-hypothesis significance test. When a statistically significant *p*-value is observed, the null-hypothesis can be rejected, and researchers claim that the intervention works, or that there is a relationship between two variables. But if the *p*-value is not statistically significant, researcher very often draw a logically incorrect conclusion: They conclude there is no effect based on *p* > 0.05. 

Open a result section of an article you are writing, or the result section of articles you have recently read. Search for *p* > 0.05, and look carefully what you or the scientists concluded. If you see the conclusion that there was 'no effect' or there was 'no association between variables', you have found an example of forgetting that *absence of evidence is not evidence of absence* [@altman_statistics_1995]. A non-significant result in itself only tells us that we can not reject the null hypothesis. It is tempting to ask after *p* > 0.05 'so, is the true effect zero'? But the *p*-value from a null-hypothesis significance test can not answer that question. It might be useful to think of the answer to the question whether an effect is absent after observing *p* > 0.05 as 無 ([mu](https://en.wikipedia.org/wiki/Mu_(negative)#Non-dualistic_meaning)), used as a non-dualistic answer, neither yes nor no, or 'unasking the question', because it is not possible to answer the question whether an effect is absent based on *p* > 0.05. 

There should be many situations where researchers are interested in examining whether an effect is absent. For example, it can be important to show two groups do not differ on factors that might be a confound in the experimental design (e.g., examining whether a manipulation intended to increase fatigue did not affect the mood of the participants by showing that positive and negative affect did not differ between the groups). Researchers might be interested in whether two interventions work equally well, especially when the newer intervention costs less or requires less effort (e.g., is online therapy just as efficient as in person therapy?). And other times we might be interested to demonstrate the absence of an effect because a theoretical model predicts there is no effect, or because we believe a previously published study was a false positive, and we expect to show the absence of an effect in a replication study.

Statistical approaches have been developed to allow researchers to make claims about the absence of effects. However, it is never possible to show an effect is *exactly* 0. Even if you would collect data from every person in the world, the effect in any single study will randomly vary around the true effect size of 0, and there will be a tiny observed difference. Hodges and Lehman [@hodges_testing_1954] were the first to discuss the statistical problem of testing whether two populations have the same mean. They suggest (p. 264) to: “test that their means do not differ by more than an amount specified to represent the smallest difference of practical interest.” Nunnaly [@nunnally_place_1960] similarly proposed a ‘fixed-increment’ hypothesis where researcher compare an observed effect against a range of values that is deemed too small to be meaningful. Defining a range of values considered practically equivalent to the absence of an effect is known as an **equivalence range** [@bauer_unifying_1996] or a **region of practical equivalence** [@kruschke_bayesian_2013]. The equivalence range should be specified in advance, and requires careful consideration of which effects are too small to be meaningful. 

Although researchers have repeatedly attempted to introduce test against an equivalence range in the social sciences [@cribbie_recommendations_2004; @levine_communication_2008; @hoenig_abuse_2001; @rogers_using_1993; @quertemont_how_2011], this statistical approach became popular during the replication crisis as researchers searched for tools to interpret null-results when performing replication studies. Researchers wanted to be able to publish informative null results when replicating findings in the literature that suspected of being false positives. One notable example were the studies on pre-cognition by Daryl Bem, which ostensibly showed that participants were able to predict the future [@bem_feeling_2011]. Equivalence tests were proposed as a statistical approach to answer the question whether an observed effect is small enough to conclude that a previous study could not be replicated [@anderson_theres_2016; @lakens_equivalence_2017; @simonsohn_small_2015]. Researchers specify a smallest effect size of interest (for example an effect of 0.5, so for a two-sided test any value outside a range from -0.5 to 0.5) and test whether effects more extreme than this range can be rejected. If so, they can reject the presence effects that are large enough to be meaningful.

Equivalence tests are a specific implementation of **interval hypothesis tests**, where instead of testing against a null hypothesis of no effect (or an effect size of 0), an effect is tested against a null hypothesis that represents a range of non-zero effect sizes. One can distinguish a **nil null hypothesis**, where the null hypothesis is an effect of 0, from a **non-nil null hypothesis**, where the null hypothesis is any other effect that 0, for example effects more extreme than the smallest effect size of interest [@nickerson_null_2000]. As Nickerson writes: 

>The distinction is an important one, especially relative to the controversy regarding the merits or shortcomings of NHST inasmuch as criticisms that may be valid when applied to nil hypothesis testing are not necessarily valid when directed at null hypothesis testing in the more general sense. 

Indeed, one of the most widely suggested improvements that mitigates the most important limitations of null-hypothesis significance testing is to replace the nil null hypothesis with the test of a range prediction (by specifying a non-nil null hypothesis) in an interval hypothesis test [@lakens_practical_2021]. To illustrate the difference, panel A in Figure \@ref(fig:intervaltest) visualizes the results that are predicted in a two-sided null hypothesis test with a nil hypothesis, where the test examines whether an effect of 0 can be rejected. Panel B shows an interval hypothesis where an effect between 0.5 and 2.5 is predicted, where the non-nill null hypothesis consists of values smaller than 0.5 or larger than 2.5, and the interval hypothesis tests examines whether values in these ranges can be rejected. Panel C illustrates an equivalence test, which is basically identical to an interval hypothesis test, but the predicted effects are located in a range around 0, and contain effects that are deemed too small to be meaningful. 

<div class="figure" style="text-align: center">
<img src="09-equivalencetest_files/figure-html/intervaltest-1.png" alt="Two-sided null hypothesis test (A), interval hypothesis test (B), equivalence test (C) and minimum effect test (D)." width="100%" />
<p class="caption">(\#fig:intervaltest)Two-sided null hypothesis test (A), interval hypothesis test (B), equivalence test (C) and minimum effect test (D).</p>
</div>

When an equivalence test is reversed, an a researcher designs a study to reject effect less extreme than a smallest effect size of interest (see Panel D in Figure \@ref(fig:intervaltest)), it is called a **minimum effect test** [@murphy_testing_1999]. A researchers might not just be interested in rejecting an effect of 0 (as in a null hypothesis significance test) but in rejecting effects that are too small to be meaningful. All else equal, a study designed to have high power for a minimum effect requires more observations than if the goal had been to reject an effect of zero. As the confidence interval needs to reject a value that is closer to the observed effect size (e.g., 0.1 instead of 0) it needs to be more narrow, which requires more observations. 

One benefit of a minimum effect test compared to a null-hypothesis test is that there is no distinction between statistical significance and practical significance. As the test value is chosen to represent the minimum effect of interest, whenever it is rejected, the effect is both statistically and practically significant [@murphy_statistical_2014]. Another benefit of minimum effect tests is that, especially in correlational studies in the social sciences, variables are often connected through causal structures that result in real but theoretically uninteresting nonzero correlations between variables, which has been labeled the 'crud factor' [@meehl_appraising_1990; @orben_crud_2020]. Because an effect of zero is unlikely to be true in large correlational datasets, rejecting a nil null hypothesis is not a severe test. Even if the hypothesis is incorrect, it is likely that an effect of 0 will be rejected due to 'crud'. For this reason, some researchers have suggested to test against a minimum effect of *r* = 0.1, as correlations below this threshold are quite common due to theoretically irrelevant correlations between variables [@ferguson_providing_2021].

Figure \@ref(fig:intervaltest) illustrates two-sided tests, but it is often more intuitive and logical to perform one-sided tests. In that case, a minimum effect test would, for example, aim to reject effects smaller than 0.1, and an equivalence test would aim to reject effects larger than for example 0.1. Instead of specifying an upper and lower bound of a range, it is sufficient to specify a single value for one-sided tests. A final variation of a one-sided non-nil null hypothesis test is known as a test for **non-inferiority**, which examines of an effect is larger than the lower bound of an equivalence range. Such a test is for example performed when a novel intervention should not be noticeable worse than an existing intervention - but it can be a tiny bit worse. For example, if a difference between a novel and existing intervention is not smaller than -0.1, and effects smaller than -0.1 can be rejected, one can conclude an effect is non-inferior [@schumi_through_2011; @mazzolari_myths_2022]. We see that extending nil null hypothesis tests to non-nil null hypotheses allow researchers to ask questions that might be more interesting.
 
## Equivalence tests

Equivalence tests were first developed in pharmaceutical sciences [@hauck_new_1984; @westlake_use_1972] and later formalized as the **two one-sided tests (TOST)** approach to equivalence testing [@schuirmann_comparison_1987; @seaman_equivalence_1998; @wellek_testing_2010]. The TOST procedure entails performing two one-sided tests to examine whether the observed data is surprisingly larger than a lower equivalence boundary ($\Delta_{L}$), or surprisingly smaller than an upper equivalence boundary ($\Delta_{U}$):

$$
t_{L} = \frac{{\overline{M}}_{1} - {\overline{M}}_{2} - \Delta_{L}}{\sigma\sqrt{\frac{1}{n_{1}} + \frac{1}{n_{2}}}}
$$

and 

$$
t_{U} = \frac{{\overline{M}}_{1} - {\overline{M}}_{2}{- \Delta}_{U}}{\sigma\sqrt{\frac{1}{n_{1}} + \frac{1}{n_{2}}}}
$$

where *M* indicates the means of each sample, *n* is the sample size, and σ is
the pooled standard deviation:

$$
\sigma = \sqrt{\frac{\left( n_{1} - 1 \right)\text{sd}_{1}^{2} + \left( n_{2} - 1 \right)\text{sd}_{2}^{2}}{n_{1} + \ n_{2} - 2}}
$$

If both one-sided tests are significant, we can reject the presence of effects large enough to be meaningful. The formulas are highly similar to the normal formula for the *t*-statistic. The difference between a NHST *t*-test and the TOST procedure is that the lower equivalence boundary $\Delta_{L}$ and the upper equivalence boundary $\Delta_{U}$ are subtracted from the mean difference between groups (in a normal *t*-test, we compare the mean difference against 0, and thus the delta drops out of the formula because it is 0).

To perform an equivalence test, you don't need to learn any new statistical tests, as it is just the well-known *t*-test against a different value than 0. It is somewhat surprising that the use of *t*tests to perform equivalence tests is not taught alongside their use in null-hypothesis significance tests, as there is some indication that this could prevent common misunderstandings of *p*-values [@parkhurst_statistical_2001]. Let's look at an example of an equivalence test using the TOST procedure. 

In a study where researchers are manipulating fatigue by asking participants to carry heavy boxes around, the researchers want to ensure the manipulation does not inadvertently alter participants’ moods. The researchers assess positive and negative emotions in both ocnditions, and want to claim there are no differences in positive mood. Let’s assume that positive mood in the experimental fatigue condition (m1 = 4.55, sd1 = 1.05, n1 = 15) did not differ from the mood in the the control condition (m2 = 4.87, sd2 = 1.11, n2 = 15). The researchers conclude: “Mood did not differ between conditions, *t* = -0.81, *p* = .42”. Of course, mood did differ between conditions, as 4.55 - 4.87 = -0.32. The claim is that there was no *meaningful* difference in mood, but to make such a claim in a correct manner, we first need to specify which difference in mood is large enough to be meaningful. For now, let's assume the researcher consider any effect less extreme half a scale point too small to be meaningful. We test now test if the observed mean difference of -0.32 is small enough such that we can reject the presence of effects that are large enough to matter.  

The TOSTER package (originally created by myself but recently redesigned by Aaron Caldwell) can be used to plot two *t*-distributions and their critical regions indicating when we can reject the presence of effects smaller than -0.5 and larger than 0.5. It can take some time to get used to the idea that we are rejecting values more extreme than the equivalence bounds. Try to consistently ask in any hypothesis test: Which values can the test reject? In a nil null hypothesis test, we can reject an effect of 0, and in the equivalence test in the Figure below, we can reject values lower than -0.5 and higher than 0.5. In Figure \@ref(fig:tdistequivalence) we see two *t*-distributions centered on the upper and lower bound of the specified equivalence range (-0.5 and 0.5). 

<div class="figure" style="text-align: center">
<img src="09-equivalencetest_files/figure-html/tdistequivalence-1.png" alt="The mean difference and its confidence interval plotted below the *t*-distributions used to perform the two-one-sided tests against -0.5 and 0.5." width="100%" />
<p class="caption">(\#fig:tdistequivalence)The mean difference and its confidence interval plotted below the *t*-distributions used to perform the two-one-sided tests against -0.5 and 0.5.</p>
</div>

Below the two curves we see a line that represents the confidence interval ranging from -0.99 to 0.35, and a dot on the line that indicates the observed mean difference of -0.32. Let's first look at the left curve. We see the green highlighted area in the tails that highlights which observed mean differences would be extreme enough to statistically reject an effect of -0.5. Our observed mean difference of -0.32 lies very close to 0.5, and if we look at the left distribution, the mean is not far enough away from 0.5 to fall in the green area that indicates when observed differences would be statistically significant. We can also perform the equivalence test using the TOSTER package, and look at the results. 


```r
TOSTER::tsum_TOST(m1 = 4.55, m2 = 4.87, sd1 = 1.05, sd2 = 1.11,
                  n1 = 15, n2 = 15, low_eqbound = -0.5, high_eqbound = 0.5)
```

```
## 
## Welch Modified Two-Sample t-Test
## Hypothesis Tested: Equivalence
## Equivalence Bounds (raw):-0.500 & 0.500
## Alpha Level:0.05
## The equivalence test was non-significant, t(27.91) = 0.456, p = 3.26e-01
## The null hypothesis test was non-significant, t(27.91) = -0.811, p = 4.24e-01
## NHST: don't reject null significance hypothesis that the effect is equal to zero 
## TOST: don't reject null equivalence hypothesis
## 
## TOST Results 
##                     t        SE       df    p.value
## t-test     -0.8111280 0.3945124 27.91398 0.42415467
## TOST Lower  0.4562595 0.3945124 27.91398 0.32586680
## TOST Upper -2.0785154 0.3945124 27.91398 0.02348582
## 
## Effect Sizes 
##                 estimate        SE   lower.ci  upper.ci conf.level
## Raw           -0.3200000 0.3945124 -0.9911879 0.3511879        0.9
## Hedges' g(av) -0.2881401 0.3812249 -0.9301965 0.3193638        0.9
## 
## Note: SMD confidence intervals are an approximation. See vignette("SMD_calcs").
```

```r
res$TOST$p[1]
```

```
## [1] 0.4241547
```

In the line 't-test' the output shows the traditional nil null hypothesis significance test (which we already knew was not statistically significant: *t* = 0.46, *p* = 0.42. Just like the default *t*-test in R, the tsum_TOST function will by default calculate Welch’s *t*-test (instead of Student’s *t*-test), which is a better default [@delacre_why_2017], but you can request Student’s *t*-test by adding `var.equal = TRUE` as an argument to the function.

We also see a test indicated by TOST Lower. This is the first one-sided test examining if we can reject effects lower than -0.5. From the test result, we see this is not the case: *t* = 0.46, *p* = 0.33. This is an ordinary *t*-test, just against an effect of -0.5. Because we can not reject differences more extreme than -0.5, it is possible that a different we consider meaningful (e.g., a difference of -0.60) is present. When we look at the one-sided test against the upper bound of the equivalence range (0.5) we see that we can statistically reject the presence of mood effects larger than 0.5, as in the line TOST Upper we see *t* = -2.08, *p* = 0.02. Our final conclusion is therefore that, even thought we can reject effects more extreme than 0.5 based on the observed mean difference of -0.32, we can not reject effects more extreme than -0.5. Therefore, we can not completely reject the presence of meaningful mood effects. As the data does not allow us to claim the effect is different from 0, nor that the effect is, if anything, too small to matter (based on an equivalence range from -0.5 to 0.5), the data are **inconclusive**. We can not distinguish between a Type 2 error (there is an effect, but in this study we just did not detect it) or a true negative (there really is no effect large enough to matter).

Note that because we fail to reject the one-sided test against the lower equivalence bound, the possibility remains that there is a true effect size that is large enough to be considered meaningful. This statement is true, even when the effect size we have observed (-0.32) is closer to zero than the equivalence bound of -0.5. One might think the observed effect size needs to be more extreme (i.e., further away from 0) than the equivalence bound to maintain the possibility that there is an effect that is large enough to be considered meaningful. But that is not required. The 90% CI indicates that some values below -0.5 can not be rejected. As we can expect that 90% of confidence intervals in the long run capture the true population parameter, it is perfectly possible that the true effect size is more extreme than -0.5. And, the effect might even be more extreme than the values captured by this confidence interval, as 10% of the time, the computed confidence interval is expected to not contain the true effect size. Therefore, when we fail to reject the smallest effect size of interest, we retain the possibility that an effect of interest exists. If we can reject the nil null hypothesis, but fail to reject values more extreme than the equivalence bounds, then we can claim there is an effect, and it might be large enough to be meaningful. 

One way to reduce the probability of an inconclusive effect is to collect sufficient data. Let's imagine the researchers had not collected 15 participants in each condition, but 200 participants. They otherwise observe exactly the same data. As explained in the chapter on [confidence intervals](#confint), as the sample size increases, the confidence interval becomes more narrow. For a TOST equivalence test to be able to reject both the upper and lower bound of the equivalence range, the confidence interval needs to fall completely within the equivalence range. In Figure \@ref(fig:ciequivalence) we see the observed mean difference (the black dot) and it's confidence interval (the horizontal black line) for a sample size of 200 per group. The colourful plot on top of the mean difference and confidence interval is a confidence density plot [@schweder_confidence_2016], which is a graphical summary of the distribution of confidence.

<div class="figure" style="text-align: center">
<img src="09-equivalencetest_files/figure-html/ciequivalence-1.png" alt="The mean difference and its confidence interval for an equivalence test with an equivalence range of -0.5 and 0.5." width="100%" />
<p class="caption">(\#fig:ciequivalence)The mean difference and its confidence interval for an equivalence test with an equivalence range of -0.5 and 0.5.</p>
</div>

```
## 
## Welch Modified Two-Sample t-Test
## Hypothesis Tested: Equivalence
## Equivalence Bounds (raw):-0.500 & 0.500
## Alpha Level:0.05
## The equivalence test was significant, t(396.78) = 1.666, p = 4.82e-02
## The null hypothesis test was significant, t(396.78) = -2.962, p = 3.24e-03
## NHST: reject null significance hypothesis that the effect is equal to zero 
## TOST: reject null equivalence hypothesis
## 
## TOST Results 
##                    t        SE       df      p.value
## t-test     -2.961821 0.1080417 396.7773 3.242190e-03
## TOST Lower  1.666024 0.1080417 396.7773 4.824893e-02
## TOST Upper -7.589665 0.1080417 396.7773 1.156039e-13
## 
## Effect Sizes 
##                 estimate        SE   lower.ci   upper.ci conf.level
## Raw           -0.3200000 0.1080417 -0.4981286 -0.1418714        0.9
## Hedges' g(av) -0.2956218 0.1008059 -0.4625958 -0.1310411        0.9
## 
## Note: SMD confidence intervals are an approximation. See vignette("SMD_calcs").
```
Because of the larger sample size, the confidence is more narrow, and we see it excludes both the upper and lower equivalence bound, which means we can reject effects outside of the equivalence range (even though with a *p* = 0.048 the one-sided test against the lower equivalence bound is only just statistically significant). If we look at the traditional nil null hypothesis test we see we can also reject an effect of 0. In other words, both the null hypothesis test as the equivalence test have yielded significant results. This means we can claim that the observed effect is statistically different from zero, and that the effect is statistically smaller than effects we deemed large enough to matter when we specified the equivalence range from -0.5 to 0.5. This illustrates how combining equivalence tests and nil null hypothesis tests can prevent us from mistaking statistically significant effects for practically significant effects. Yes, we can reject an effect of 0, but no, the effect is not large enough to be meaningful.

## Reporting Equivalence Tests 

It is common practice to only report the test yielding the higher *p*-value of the two one-sided tests when reporting an equivalence test. Because both one-sided tests need to be statistically significant to reject the null hypothesis in an equivalence test (i.e., the presence of effects large enough to matter), when the larger of the two hypothesis tests rejects the equivalence bound, so does the other test. Unlike in null-hypothesis significance tests it is not common to report standardized effect sizes for equivalence tests, but there can be situations where researchers might want to discuss how far the effect is removed from the equivalence bounds on the raw scale. Prevent the erroneous interpretation to claim there is 'no effect', that an effect is 'absent', that the true effect size is 'zero', or vague verbal descriptions, such as that two groups yielded 'similar' or 'comparable' data. A significant equivalence test rejects effects more extreme that the equivalence bounds. Smaller true effects have not been rejected, and thus it remains possible that there is a true effect. Because a TOST procedure is a frequentist test based on a *p*-value, all other [misconceptions of *p*-values](#misconceptions) should be prevented as well. 

When summarizing the main result of an equivalence test, for example in an abstract, always report the equivalence range that the data is tested against. Reading 'based on an equivalence test we concluded the absence of a meaningful effect' means something very different if the equivalence bounds were d = -0.9 to 0.9 than when the bounds were d = -0.2 to d = 0.2. So instead, write "based on an equivalence test with an equivalence range of d = -0.2 to 0.2, we conclude the absence of a meaningful effect. Of course, whether peers agree you have correctly concluded the absence of a meaningful effect depends on whether they agree with your justification for a smallest effect of interest! A more neutral conclusion would be a statement such as: 'based on an equivalence test, we rejected the presence of effects more extreme than -0.2 to 0.2, so we can act (with an error rate of alpha) as if the effect, is any, is less extreme than our equivalence range'. Here, you do not use value-laden terms such as 'meaningful'. If both a null-hypothesis test and a significant test are non-significant, the findings is best described as 'inconclusive': There is not enough data to reject the null, or the smallest effect size of interest. If both the null-hypothesis test and the equivalence test are statistically significant, you can claim there is an effect, but at the same time claim the effect is too small to be of interest (given your justification for the equivalence range).

Equivalence bounds can be specified in raw effect sizes, or in standardized mean differences. It is better to specify the equivalence bounds in terms of raw effect sizes. Setting them in terms of Cohen's *d* leads to bias in the statistical test, as the observed standard deviation has to be used to translate the specified Cohen's *d* into a raw effect size for the equivalence test (and when you set equivalence bounds in standardized mean differences, TOSTER will warn: "Warning: setting bound type to SMD produces biased results!"). The bias is in practice not too problematic in any single equivalence test, and being able to specify the equivalence bounds in standardized mean differences lowers the threshold to perform an equivalence test when they do not know the standard deviation of their measure. But as equivalence testing becomes more popular, and fields establish smallest effect sizes of interest, they should do so in raw effect size differences, not in standardized effect size differences. 

## Minimum Effect Tests

If a researcher has specified a smallest effect size of interest, and is interested in testing whether the effect in the population is larger than this smallest effect of interest, a minimum effect test can be performed. As with any hypothesis test, we can reject the smallest effect of interest whenever the confidence interval around the observed effect does not overlap with it. In the case of a minimum effect test, however, the confidence interval should be fall completely beyond the smallest effect size of interest. For example, let's assume a researcher performs a minimum effect test with 200 observations per condition against a smallest effect size of interest of a mean difference of 0.5.

<div class="figure" style="text-align: center">
<img src="09-equivalencetest_files/figure-html/tmet-1.png" alt="The mean difference and its confidence interval plotted below the *t*-distributions used to perform the two-one-sided tests against -0.5 and 0.5 when performing a minimum effect test." width="100%" />
<p class="caption">(\#fig:tmet)The mean difference and its confidence interval plotted below the *t*-distributions used to perform the two-one-sided tests against -0.5 and 0.5 when performing a minimum effect test.</p>
</div>

```
## 
## Welch Modified Two-Sample t-Test
## Hypothesis Tested: Minimal Effect
## Equivalence Bounds (raw):-0.500 & 0.500
## Alpha Level:0.05
## The minimal effect test was significant, t(396.78) = 12.588, p = 4.71e-04
## The null hypothesis test was significant, t(396.78) = 7.960, p = 1.83e-14
## NHST: reject null significance hypothesis that the effect is equal to zero 
## TOST: reject null MET hypothesis
## 
## TOST Results 
##                    t        SE       df      p.value
## t-test      7.959893 0.1080417 396.7773 1.827800e-14
## TOST Lower 12.587737 0.1080417 396.7773 1.000000e+00
## TOST Upper  3.332048 0.1080417 396.7773 4.714941e-04
## 
## Effect Sizes 
##                estimate        SE  lower.ci  upper.ci conf.level
## Raw           0.8600000 0.1080417 0.6818714 1.0381286        0.9
## Hedges' g(av) 0.7944836 0.1041808 0.6263676 0.9689959        0.9
## 
## Note: SMD confidence intervals are an approximation. See vignette("SMD_calcs").
```
Below the two curves we again see a line that represents the confidence interval ranging from 0.68 to 1.04, and a dot on the line that indicates the observed mean difference of 0.86. The entire confidence interval lies well above the minimum effect of 0.5, and we can therefore not just reject the nil null hypothesis, but also effects smaller than the minimum effect of interest. Therefore, we can claim that the effect is large enough to be not just statistically significant, but also practically significant (as long as we have justified our smallest effect size of interest well). Because we have performed a two-sided minimum effect test, the minimum effect test would also have been significant if the confidence interval had been completely on the opposite side of -0.5. 

Earlier we discussed how combining traditional NHST and an equivalence test lead to more informative results, and it is also possible to combine a minimum effect test and an equivalence test. One might even say that such a combination is most informative test of a prediction whenever a smallest effect size of interest can be specified. In principle, this is true. As long as we are able to collect enough data, we will always get an informative and straightforward answer when we combine a minimum effect test with an equivalence test: Either we can reject all effects that are too small to be of interest, or we can reject all effects that are large enough to be of interest. As we will see below in the section on power analysis for interval hypotheses, whenever the true effect size is close to the smallest effect size of interest, a large amount of observations will need to be collected. And if the true effect size happens to be identical to the smallest effect size of interest, neither the minimum effect test nor the equivalence test can be correctly rejected (and any significant test would be a Type 1 error). If a researcher can collect sufficient data (so that the test has high statistical power), and is relatively confident that the true effect size will be larger or smaller than the smallest effect of interest, then the combination of a minimum effect test and an equivalence test can be attractive as such a hypothesis test is likely yield a clear answer to the research question. 

## Power Analysis for Interval Hypothesis Tests

When designing a study it is a sensible strategy to always plan for both the presence, as the absence, of an effect. Several scientific journals require a sample size justification for Registered Reports where the statistical power to reject the null hypothesis is high, but where the study is also capable of demonstrating the absence of an effect, for example by also performing a power analysis for an equivalence test. As we saw in the chapter on [error control](#errorcontrol) and [likelihoods](#likelihoods) null results are to be expected, and if you only think about the possibility of observing a null effect when the data has been collected, it is often too late.

The statistical power for interval hypotheses depend on the alpha level, the sample size, the smallest effect of interest you decide to test against, and the true effect size. For an equivalence test, it is common to perform a power analysis assuming the true effect size is 0, but this might not always be realistic. The closer the expected effect size is to the smallest effect size of interest, the larger the sample size needed to reach a desired power. Don't be tempted to assume a true effect size of 0, if you have good reason to expect a small but non-zero true effect size. The sample size that the power analysis indicates you need to collect might be smaller, but in reality you also have a higher probability of an inconclusive result. Earlier versions of TOSTER only enabled researchers to perform power analyses for equivalence tests assuming a true effect size of 0, but a new power function by Aaron Caldwell allows users to specify `delta`, the expected effect size. 

Assume a researchers desired to achieve 90% power for an equivalence test with an equivalence range from -0.5 to 0.5, with an alpha level of 0.05, and assuming a population effect size of 0. A power analysis for an equivalence test can be performed to examine the required sample size. 


```r
TOSTER::power_t_TOST(power = 0.9, delta = 0,
                     alpha = 0.05, type = "two.sample",
                     low_eqbound = -0.5, high_eqbound = 0.5)
```

```
## 
##      Two-sample TOST power calculation 
## 
##           power = 0.9
##            beta = 0.1
##           alpha = 0.05
##               n = 87.26261
##           delta = 0
##              sd = 1
##          bounds = -0.5, 0.5
## 
## NOTE: n is number in *each* group
```

We see that the required sample size is 88 participants in each condition for the independent *t*-test, Let's compare this power analysis to a situation where the researcher expects a true effect of d = 0.1, instead of a true effect of 0. To be able to reliable reject effects larger than 0.5, we will need a larger sample size, just as how we need a larger sample size for a null-hypothesis test powered to detect a d = 0.4 than a null-hypothesis test powered to detect a d = 0.5. 


```r
TOSTER::power_t_TOST(power = 0.9, delta = 0.1,
                     alpha = 0.05, type = "two.sample",
                     low_eqbound = -0.5, high_eqbound = 0.5)
```

```
## 
##      Two-sample TOST power calculation 
## 
##           power = 0.9
##            beta = 0.1
##           alpha = 0.05
##               n = 108.9187
##           delta = 0.1
##              sd = 1
##          bounds = -0.5, 0.5
## 
## NOTE: n is number in *each* group
```

We see the sample size has now increased to 109 participants in each condition. As mentioned before, it is not necessary to perform a two-sided equivalence test. It is also possible to perform a one-sided equivalence test. An example of a situation where such a directional test is appropriate is a replication study. If a previous study observed an effect of d = 0.48, and you perform a replication study, you might decide to consider any effect smaller than d = 0.2 a failure to replicate - including any effect in the opposite direction, such as an effect of d = -0.3. Although most software for equivalence tests requires you to specify an upper and lower bound for an equivalence range, you can mimic a one-sided test by setting the equivalence bound in the direction you want to ignore to a low value so that the one-sided test against this value will always be statistically significant. This can also be used to perform a power analysis for a minimum effect test, where one bound is the minimum effect of interest, and the other bound is set to an extreme value on the other side of the expected effect size. 

In the power analysis for an equivalence test example below, the lower bound is set to -5 (it should be set low enough such that lowering it even further has no noticeable effect). We see that the new power function in the TOSTER package takes the directional prediction into account, and just as with directional predictions in a nil null hypothesis test, a directional prediction in an equivalence test is more efficient, and only 70 observations are needed to achieve 90% power. 


```r
# New TOSTER power functions allows power for expected non-zero effect.
TOSTER::power_t_TOST(power = 0.9, delta = 0,
                     alpha = 0.05, type = "two.sample",
                     low_eqbound = -5, high_eqbound = 0.5)
```

```
## 
##      Two-sample TOST power calculation 
## 
##           power = 0.9
##            beta = 0.1
##           alpha = 0.05
##               n = 69.19784
##           delta = 0
##              sd = 1
##          bounds = -5.0, 0.5
## 
## NOTE: n is number in *each* group
```
Statistical software offers options for power analyses for some statistical tests, but not for all tests. Just as with power analysis for a nil null hypothesis test, it can be necessary to use a simulation-based approach to power analysis.  

## The Bayesian ROPE procedure {#ROPE}

In Bayesian estimation, one way to argue for the absence of a meaningful effect is the **region of practical equivalence** (ROPE) procedure (@kruschke_bayesian_2013), which is “somewhat analogous to frequentist equivalence testing” (@kruschke_bayesian_2017). In the ROPE procedure, an equivalence range is specified, just as in equivalence testing, but the Bayesian highest density interval based on a posterior distribution (as explained in the chapter on [Bayesian statistics](#bayes)) is used instead of the confidence interval. 

If the prior used by Kruschke was perfectly uniform, and the ROPE procedure and an equivalence test used the same confidence interval (e.g., 90%), the two tests would yield  identical results. There would only be philosophical differences in how the numbers are interpreted. The BEST package in R that can be used to perform the ROPE procedure by default uses a ‘broad’ prior, and therefore results of the ROPE procedure and an equivalence test are not exactly the same, but they are very close. One might even argue the two tests are 'practically equivalent'. In the R code below random normally distributed data for two conditions is generated (with means of 0 and a standard deviation of 1) and the ROPE procedure and a TOST equivalence test are performed. 

<img src="09-equivalencetest_files/figure-html/unnamed-chunk-7-1.png" width="100%" style="display: block; margin: auto;" /><img src="09-equivalencetest_files/figure-html/unnamed-chunk-7-2.png" width="100%" style="display: block; margin: auto;" />
The 90% HDI ranges from -0.06 to 0.39, with an estimated mean based on the prior and the data of 0.164. The HDI falls completely between the upper and the lower bound of the equivalence range, and therefore values more extreme than -0.5 or 0.5 are deemed implausible. The 95% CI ranges from -0.07 to 0.36 with an observed mean difference of 0.15. We see that the numbers are not identical, because in Bayesian estimation the observed values are combined with a prior, and the mean estimate is not purely based on the data. But the results are very similar, and will in most cases lead to similar inferences. The BEST R package also enables researchers to perform simulation based power analyses, which take a long time but, when using a broad prior, yield a result that is basically identical to the sample size from a power analysis for an equivalence test. The biggest benefit of ROPE over TOST is that it allows you to incorporate prior information. If you have reliable prior information, ROPE can use this information, which is especially useful if you don’t have a lot of data. If you use informed priors, check the robustness of the posterior against reasonable changes in the prior in sensitivity analyses.

## Which interval width should be used?

Because the TOST procedure is based on two one-sided tests, a 90% confidence interval is used when the one-sided tests are performed at an alpha level of 5%. Because both the test against the upper bound and the test against the lower bound needs to be statistically significant to declare equivalence (which as explained in the chapter on [error control](#multiplecomparisons) is an intersection-union approach to multiple testing) it is not necessary to correct for the fact that two tests are performed. If the alpha level is adjusted for multiple comparisons, or if the alpha level is justified instead of relying on the default 5% level (or both), the corresponding confidence interval should be used, where CI = 100 - (2 * $\alpha$). Thus, the width of the confidence interval is directly related to the choice for the alpha level, as we are making decisions to reject the smallest effect size of interest, or not, based on whether the confidence interval excluded the effect that is tested against.

When using a Highest Density Interval from a Bayesian perspective, such as the ROPE procedure, the choice for a width of a confidence interval does not follow logically from a desired error rate, or any other principle. Kruschke (2014, Chapter 5) writes: “How should we define 'reasonably credible'? One way is by saying that any points within the 95% HDI are reasonably credible.” McElreath has recommended the use of 67%, 89%, and 97%, because "No reason. They are prime numbers, which makes them easy to remember.". There are only two principled solutions. First, if a highest density interval width is used to make claims, these claims will be made with certain error rates, and researchers should quantify the risk of erroneous claim by computing frequentist error rates. This would make the ROPE procedure a Bayesian/Frequentist compromise procedure, where the computation of a posterior distribution allows for Bayesian interpretations of which parameters values are believed to be most probable, while decisions based on whether or not the HDI falls within an equivalence range have a formally controlled error rate. Note that when using an informative prior, a HDI does not match a CI, and the error rate when using a HDI can only be derived through simulations. The second solution is to not make any claims, present the full posterior distribution, and let readers draw their own conclusions.

## Test Yourself

<!-- **Q1**: What is the correct interpretation of the following result if a researchers has performed a nil null hypothesis and an equivalence test (the equivalence bounds are indicated by the vertical dashed lines)?  -->

<!-- ```{r, eq_q_1, echo = FALSE} -->
<!-- res <- TOSTER::tsum_TOST(m1 = 0, m2 = 0.2, sd1 = 1, sd2 = 1, -->
<!--                   n1 = 100, n2 = 100, low_eqbound = -0.34, high_eqbound = 0.34) -->
<!-- plot(res, type = "tnull") -->

<!-- ``` -->

<!-- A) We can reject an effect of 0, and we fail to reject the smallest effect size of interest. Therefore we can claim there is an effect  -->