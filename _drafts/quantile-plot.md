---
layout: default
title: "qq plot"
subtitle: "learning from quantile plot"
tags: [data-science]
---

# {{ page.title }}
tags: {% for tag in page.tags %}{{ tag }} {% endfor %}

### {{ page.subtitle }}, {{ page.date | date_to_string }}

---

For me, data analysis is about taking a particular viewpoint and produce personal interpretation about the data. Viewpoints are usually made of a set of statistical measurement. Then interpretation is made with viewpoints as the support. Here, I want to highlight that viewpoint is fact while interpretation is not. In this post, I want us to look at one statistical measurement that we could use to build our viewpoint, called Q-Q plot (quantile-quantile plot).

Q-Q plot is a tool to compare two distributions. Usually the distributions of interest are sample distribution and theoretical distribution. Theoretical distribution is the distribution of data that we believe. We want to check if data truly comes from the theoretical distribution. If data points form straight line, the theoretical distribution is most likely true, and vice versa.

Why don't we just compare the pdf or pmf?
I guess comparing distribution using pdf/pmf is tricky. Parametric pdfs/pmfs have parameters that could influence their shape. For example, Gamma distribution has shape and scale parameters. Different value of both parameters could produce quite different distribution graph. So, comparing theoretical pdf/pmf and data plot is hard because it is sometimes unclear visually. Using Q-Q plot, we could just evaluate by looking graph forms straight line.

How does it (series of quantiles) form a straight line?
Q-Q plot works by getting two quantile values. One is from the data and second is quantile given the data is sampled from the theoretical distribution. If the distribution is similar, both quantiles values will be very similar as well, hence producing a linear plot.