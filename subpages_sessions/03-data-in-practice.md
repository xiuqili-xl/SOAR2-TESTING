---
layout: page
title: "Module 2: Data in Practice"
permalink: /sessions/module2/
---

## Module Description 

Work hands-on with data and learn how to organize, explore, and visualize it using tools like Excel and coding language (e.g., R or Python). You’ll see how structuring data thoughtfully makes your work easier to understand and build on. Along the way, you’ll get a glimpse of how coding supports more efficient and reproducible workflows.

<br/>


## Instructors

TBA

<br/>


## Code?

This website is built with Jekyll. Jekyll will render Markdown, but don't think it will execute R chunks like a .qmd file? 🤔 Open to suggestions 🙏

We could, however, embed non-running code chunks. See below

```r
library(readr)
library(dplyr)
library(ggplot2)

bw_data <- read_csv("session_materials/temp/motrpac_rat_8wk_bw_data.csv")

bw_summary <- bw_data %>%
  group_by(sex, study_group, timepoint, training_day) %>%
  summarise(wt_mean = mean(weight),
            wt_sd = sd(weight))

ggplot(data = bw_summary, 
       mapping = aes(x = training_day, y = wt_mean, group = study_group, color = study_group)) +
  geom_line() +
  geom_point(size = 2) +
  geom_errorbar(mapping = aes(ymin = wt_mean - wt_sd, ymax = wt_mean + wt_sd), 
                width = 0.5) +
  facet_wrap(~sex, ncol = 1, scales = "free_y") +
  theme_bw() +
  labs(title = "Body weights of rats over 8 week training period (mean +/- sd)",
       x = "Days of training", y = "Body weight (g)", color = "Group")
```


So if we want to share any script with students and ask them to run it...

- We could have code chunks on a .md file as part of this website. We'll then ask student to copy and paste into their IDE.
- OR we could create a repo just for that modules, and hyperlink that repo here. Students will only need to pull that module-specific repo and work with it. 
    - This is probably the cleaner option: students don't have to deal with the repo for this website, which has way too much unrelated layers and content...

