## Population

All subjects of interest have been surveyed and are available for analysis

## Sample

A subset of the population has been surveyed and will provide estimates for the population.

# Descriptive Statistics

Describe, show or summarize data from a sample in a meaningful way.

- Mean
- Distribution
- Standard deviation
- Range
- Variance
- Skew
- Outlier Identification
- Regression
- Contingency table
- Correlation matrix
- Pearson correlation coefficient
- Discriminant analysis
- Factor analysis
- Canonical correlation

<!-- Expand to Graphical methods, central tendency, Dispersion, measures of association, -->

# Inferential Statistics (Hypothesis Tests)

Make conclusions from the data sample by using the null and alternative hypotheses that are subjected to random variation.

Parametric: Numerical data that is normally distributed
Non-parametric: Statistics that do not estimate population parameters. Normality assumption are not met.

## One-sample

<!-- prettier-ignore -->
| Normality Assumption | Test | Evaluation | Conditions |
| --- | --- | --- | --- |
| Parametric | [Paired t-test](https://en.wikipedia.org/wiki/Student%27s_t-test) | Hypothesized population mean | Quantitative |
| Non-parametric | [Sign Test](https://en.wikipedia.org/wiki/Sign_test) | Hypothesized population median | Quantitative |
| Non-parametric | [Wilcoxon's signed rank test](https://en.wikipedia.org/wiki/Wilcoxon_signed-rank_test) | Hypothesized population median <br> Ranks all data points | Quantitative |

## Two-sample

<!-- prettier-ignore -->
| Normality Assumption | Test | Evaluation | Conditions |
| --- | --- | --- | --- |
| Parametric | [Unpaired t-test](https://en.wikipedia.org/wiki/Student%27s_t-test) | Compare two population means | Quantitative <br> Independent samples |
| Parametric | [Paired t-test](https://en.wikipedia.org/wiki/Student%27s_t-test) | Compare two population means | Quantitative <br> Paired samples |
| Non-parametric | [Sign Test](https://en.wikipedia.org/wiki/Sign_test) | Compare two population medians | Quantitative <br> Paired samples |
| Non-parametric | [Wilcoxon's signed rank test](https://en.wikipedia.org/wiki/Wilcoxon_signed-rank_test) | Compare random population by random sample <br> Ranks all data points | Quantitative <br> Paired samples |
| Non-parametric | [Mann-Whitney U test](https://en.wikipedia.org/wiki/Mann%E2%80%93Whitney_U_test) | Compare two population by random sample | Quantitative <br> Independent samples |
| Non-parametric | [Kolmogorov-Smirnov test](https://en.wikipedia.org/wiki/Kolmogorov%E2%80%93Smirnov_test) | Compare two populations by probability distribution <br> Goodness of fit test if comparing with normal curve | Quantitative <br> Paired samples |

## K-sample

<!-- prettier-ignore -->
| Normality Assumption | Test | Evaluation | Conditions |
| --- | --- | --- | --- |
| Parametric | [One-way ANOVA](https://en.wikipedia.org/wiki/One-way_analysis_of_variance) | Compare two+ population means | Continuous DV <br> Equal population variances <br>  |
| Parametric | [Two-way ANOVA](https://en.wikipedia.org/wiki/Analysis_of_variance) | Compare two+ population means <br> Identify IV interaction effect | Continuous DV <br> Equal population variances <br> 2 categorical IVs |
| Non-parametric | [Kruskal-Wallis test](https://en.wikipedia.org/wiki/Kruskal%E2%80%93Wallis_one-way_analysis_of_variance) | Evaluate if two samples originate from same distribution | Ordinal DV <br> Independent samples |
| Non-parametric | [Jonckheere's trend test](https://en.wikipedia.org/wiki/Jonckheere%27s_trend_test) | Evaluate if two samples originate from same distribution | Ordinal DV <br> Independent samples |
| Non-parametric | [Friedman test](https://en.wikipedia.org/wiki/Friedman_test) | Evaluate if two samples differ with treatment | Ordinal DV <br> Paired samples |

<!-- Descriptive statistic of two variables
| Non-parametric | [Spearman rank order](https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient) | Rank correlation between two variables | Ordinal DV <br> Independent samples |
| [Chi-square goodness of fit](https://en.wikipedia.org/wiki/Goodness_of_fit#Categorical_data) | How well a model fits a set of observations |  |
[Article](https://stats.idre.ucla.edu/spss/whatstat/what-statistical-analysis-should-i-usestatistical-analyses-using-spss/)
-->

## Categorical

<!-- prettier-ignore -->
| Test | Evaluation | Conditions |
| --- | --- | --- |
| [Chi-square test](https://en.wikipedia.org/wiki/Chi-squared_test) | Test expected and observed frequencies |  |
| [Fisher’s exact test](https://en.wikipedia.org/wiki/Fisher%27s_exact_test) | Test expected and observed frequencies | Good for small populations |
| [Binomial test](https://en.wikipedia.org/wiki/Binomial_test) | Test expected and observed frequencies | Two groups |

# Regression

- Logistic Regression
- Linear Regression
- Multiple regression
- Multivariate multiple regression
- Analysis of covariance
