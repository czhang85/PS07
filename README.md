PS07
================
Cindy Zhang

## Introduction

As an admitted and enrolled students of Class of 2025, I'm curious to learn about the acceptance rate of Smith undergraduate admission since the start of application. To see the change in trend, I chose to use line graphs and collected data from 2011-21 for the visualization. 

## Including Code

You can include R code in the document as follows:

``` r
smith_admission <- read_csv("/Users/cindyzhang/Desktop/Smith Class/2021 Fall/SDS 192/Problem Set/PS07/smith_admission.csv")
```

    ## Rows: 11 Columns: 3

    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## dbl (3): Year, Acceptance_Rate, Yield

    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

```{r pressure, echo=FALSE}
ggplot(data = smith_admission, 
       mapping = aes(x = Year, y = Acceptance_Rate)) +
  ylim(25, 55) +
  ylab("Acceptance Rate") +
  labs(title = "Smith College Undergraduate Admission Acceptance Rate", subtitle = "from 2011-2021") +
  geom_text(aes(label = Acceptance_Rate), size = 3, vjust = -1.3) +
  geom_line()
```

## Including Plots

You can also embed plots, for example:

![](README_download/smith_admission.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.

## Conclusion

From the line graph, we can see that the acceptance rate of Smith undergraduate admission is generally decreasing, from about 45% in 2011 to 36% in 2021. This could possibly reflect the fact that there are now more applicants each year, and the college admission has became more selective as a result. Knowing this data, I'm glad that I'm one of the admitted students and officially joined as a member of Class of 2025.
