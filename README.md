# Introduction to R and the Tidyverse

This repo houses the raw and cleaned data as well as the R Markdown files with code for the Introduction to R and the Tidyverse workshop presented at UAB Research Computing Days 2022 (March 2-3).

There are some brief instructions for users prior to the beginning of the workshop regarding installing specific packages for those who have not used R at all before.

## Software Installation

For this workshop, we will use R and RStudio on our laptops. Each of these pieces of software is available for free. follow the links to download:

R: https://mirrors.nics.utk.edu/cran/

RStudio: https://www.rstudio.com/products/rstudio/download/. Choose the free RStudio Desktop version on the far left column. DO NOT DOWNLOAD THE RSTUDIO SERVER OR A PAID VERSION.


## Package Installation

Most of this workshop will be centered around using the `tidyverse` suite of packages as well as the `rstatix` package for a simple statistical analysis.

These packages are not available in base R and must be installed by the user. Once installed, you will not need to install them again, only update them when necessary.

To install these packages, paste the following command into the Console window (the large window on the left side of the screen with the blinking cursor and the `>` sign):

``` R
install.packages(c('tidyverse','rstatix'))
```

Package installation will take a few minutes. If you have issues installing these packages, please let me know.

## Data Download

We will be using cleaned versions of data tracking nominal and actual tuition at a number of universities over time. These data were inspired by the [Tidy Tuesday project](https://github.com/rfordatascience/tidytuesday/blob/master/data/2020/2020-03-10/readme.md) looking at the same type of data. Some data was also downloaded from [TuitionTracker](https://www.tuitiontracker.org) where some of the Tidy Tuesday data originally came from.

During class, we will cover how to load the data into the workspace. However, for those who want to look at the data beforehand, you can use the following commands to access the data directly from github:

``` R
# read in tuition cost over time
tuition_cost <- readr::read_csv('https://raw.githubusercontent.com/mdefende/2022_Intro_to_R_Workshop/main/cleaned_data/cost_of_attendance.csv')

# read in graduation rate data over time
grad_rate <- readr::read_csv('https://raw.githubusercontent.com/mdefende/2022_Intro_to_R_Workshop/main/cleaned_data/graduation_rate.csv')
```
