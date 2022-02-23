# Introduction to R and the Tidyverse

This repo houses the raw and cleaned data as well as the R Markdown files with code for the Introduction to R and the Tidyverse workshop presented at UAB Research Computing Days 2022 (March 2-3).

There are some brief instructions for users prior to the beginning of the workshop regarding installing specific packages for those who have not used R at all before.

## Requesting an RStudio Job (For users using Cheaha)

1. Please go to https://rc.uab.edu. If you do not have a Cheaha account, you will directed to create one by filling out a very short form. Once the form is complete, your account with be ready.

2. Click on Interactive Apps > RStudio Server

3. Use the following inputs for the job:
   - R Version: 4.0.2
   - Number of Hours: 4
   - Partition: short
   - Number of CPU: 1
   - Memory Per CPU: 8

4. Click `Launch`. The job will be entered into the queue. The card created for the job will remain grayed out while the job is being scheduled. This may take a little while depending on the cluster workload. Once the card turns green, the job will have been allocated resources and you will have access to the RStudio program

5. Click `Open RStudio Server`.

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
