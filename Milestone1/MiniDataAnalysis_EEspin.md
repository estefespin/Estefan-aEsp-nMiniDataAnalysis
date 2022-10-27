Mini Data-Analysis Deliverable 1
================
Estefania Espin
2022-10-09

# Welcome to your (maybe) first-ever data analysis project!

And hopefully the first of many. Let’s get started:

1.  Install the [`datateachr`](https://github.com/UBC-MDS/datateachr)
    package by typing the following into your **R terminal**:

<!-- -->

    install.packages("devtools")
    devtools::install_github("UBC-MDS/datateachr")

2.  Load the packages below.

``` r
library(datateachr)
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
    ## ✔ ggplot2 3.3.6      ✔ purrr   0.3.4 
    ## ✔ tibble  3.1.8      ✔ dplyr   1.0.10
    ## ✔ tidyr   1.2.1      ✔ stringr 1.4.1 
    ## ✔ readr   2.1.2      ✔ forcats 0.5.2 
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

3.  Make a repository in the <https://github.com/stat545ubc-2022>
    Organization. You will be working with this repository for the
    entire data analysis project. You can either make it public, or make
    it private and add the TA’s and Lucy as collaborators. A link to
    help you create a private repository is available on the
    \#collaborative-project Slack channel.

# Instructions

## For Both Milestones

-   Each milestone is worth 45 points. The number of points allocated to
    each task will be annotated within each deliverable. Tasks that are
    more challenging will often be allocated more points.

-   10 points will be allocated to the reproducibility, cleanliness, and
    coherence of the overall analysis. While the two milestones will be
    submitted as independent deliverables, the analysis itself is a
    continuum - think of it as two chapters to a story. Each chapter, or
    in this case, portion of your analysis, should be easily followed
    through by someone unfamiliar with the content.
    [Here](https://swcarpentry.github.io/r-novice-inflammation/06-best-practices-R/)
    is a good resource for what constitutes “good code”. Learning good
    coding practices early in your career will save you hassle later on!

## For Milestone 1

**To complete this milestone**, edit [this very `.Rmd`
file](https://raw.githubusercontent.com/UBC-STAT/stat545.stat.ubc.ca/master/content/mini-project/mini-project-1.Rmd)
directly. Fill in the sections that are tagged with
`<!--- start your work below --->`.

**To submit this milestone**, make sure to knit this `.Rmd` file to an
`.md` file by changing the YAML output settings from
`output: html_document` to `output: github_document`. Commit and push
all of your work to the mini-analysis GitHub repository you made
earlier, and tag a release on GitHub. Then, submit a link to your tagged
release on canvas.

**Points**: This milestone is worth 45 points: 43 for your analysis, 1
point for having your Milestone 1 document knit error-free, and 1 point
for tagging your release on Github.

# Learning Objectives

By the end of this milestone, you should:

-   Become familiar with your dataset of choosing
-   Select 4 questions that you would like to answer with your data
-   Generate a reproducible and clear report using R Markdown
-   Become familiar with manipulating and summarizing your data in
    tibbles using `dplyr`, with a research question in mind.

# Task 1: Choose your favorite dataset (10 points)

The `datateachr` package by Hayley Boyce and Jordan Bourak currently
composed of 7 semi-tidy datasets for educational purposes. Here is a
brief description of each dataset:

-   *apt_buildings*: Acquired courtesy of The City of Toronto’s Open
    Data Portal. It currently has 3455 rows and 37 columns.

-   *building_permits*: Acquired courtesy of The City of Vancouver’s
    Open Data Portal. It currently has 20680 rows and 14 columns.

-   *cancer_sample*: Acquired courtesy of UCI Machine Learning
    Repository. It currently has 569 rows and 32 columns.

-   *flow_sample*: Acquired courtesy of The Government of Canada’s
    Historical Hydrometric Database. It currently has 218 rows and 7
    columns.

-   *parking_meters*: Acquired courtesy of The City of Vancouver’s Open
    Data Portal. It currently has 10032 rows and 22 columns.

-   *steam_games*: Acquired courtesy of Kaggle. It currently has 40833
    rows and 21 columns.

-   *vancouver_trees*: Acquired courtesy of The City of Vancouver’s Open
    Data Portal. It currently has 146611 rows and 20 columns.

**Things to keep in mind**

-   We hope that this project will serve as practice for carrying our
    your own *independent* data analysis. Remember to comment your code,
    be explicit about what you are doing, and write notes in this
    markdown document when you feel that context is required. As you
    advance in the project, prompts and hints to do this will be
    diminished - it’ll be up to you!

-   Before choosing a dataset, you should always keep in mind **your
    goal**, or in other ways, *what you wish to achieve with this data*.
    This mini data-analysis project focuses on *data wrangling*,
    *tidying*, and *visualization*. In short, it’s a way for you to get
    your feet wet with exploring data on your own.

And that is exactly the first thing that you will do!

1.1 Out of the 7 datasets available in the `datateachr` package, choose
**4** that appeal to you based on their description. Write your choices
below:

**Note**: We encourage you to use the ones in the `datateachr` package,
but if you have a dataset that you’d really like to use, you can include
it here. But, please check with a member of the teaching team to see
whether the dataset is of appropriate complexity. Also, include a
**brief** description of the dataset here to help the teaching team
understand your data.

<!-------------------------- Start your work below ---------------------------->

# *Task 1 Choosing my favorite dataset*

I chose the following four datasets according to the description of each
of them and my personal interests.

1: cancer_sample 2: vancouver_trees 3: flow_sample 4: apt_buildings

<!----------------------------------------------------------------------------->

1.2 One way to narrowing down your selection is to *explore* the
datasets. Use your knowledge of dplyr to find out at least *3*
attributes about each of these datasets (an attribute is something such
as number of rows, variables, class type…). The goal here is to have an
idea of *what the data looks like*.

*Hint:* This is one of those times when you should think about the
cleanliness of your analysis. I added a single code chunk for you below,
but do you want to use more than one? Would you like to write more
comments outside of the code chunk?

<!-------------------------- Start your work below ---------------------------->

## Exploring cancer_sample dataset

I called the data set and used the **glimpse** function in order to have
an idea of the variables names and type.I have experience in the
molecular oncology of breast cancer research, but this dataset has
variables related to the phyisical characteristics of the tumor tissue,
and I considered that to have a research question answered I would need
to make correlations analysis, which I have not learned yet. Thus, I
discarded this option.

``` r
### EXPLORE HERE ###
cancer_sample
```

    ## # A tibble: 569 × 32
    ##          ID diagnosis radius_m…¹ textu…² perim…³ area_…⁴ smoot…⁵ compa…⁶ conca…⁷
    ##       <dbl> <chr>          <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>
    ##  1   842302 M               18.0    10.4   123.    1001   0.118   0.278   0.300 
    ##  2   842517 M               20.6    17.8   133.    1326   0.0847  0.0786  0.0869
    ##  3 84300903 M               19.7    21.2   130     1203   0.110   0.160   0.197 
    ##  4 84348301 M               11.4    20.4    77.6    386.  0.142   0.284   0.241 
    ##  5 84358402 M               20.3    14.3   135.    1297   0.100   0.133   0.198 
    ##  6   843786 M               12.4    15.7    82.6    477.  0.128   0.17    0.158 
    ##  7   844359 M               18.2    20.0   120.    1040   0.0946  0.109   0.113 
    ##  8 84458202 M               13.7    20.8    90.2    578.  0.119   0.164   0.0937
    ##  9   844981 M               13      21.8    87.5    520.  0.127   0.193   0.186 
    ## 10 84501001 M               12.5    24.0    84.0    476.  0.119   0.240   0.227 
    ## # … with 559 more rows, 23 more variables: concave_points_mean <dbl>,
    ## #   symmetry_mean <dbl>, fractal_dimension_mean <dbl>, radius_se <dbl>,
    ## #   texture_se <dbl>, perimeter_se <dbl>, area_se <dbl>, smoothness_se <dbl>,
    ## #   compactness_se <dbl>, concavity_se <dbl>, concave_points_se <dbl>,
    ## #   symmetry_se <dbl>, fractal_dimension_se <dbl>, radius_worst <dbl>,
    ## #   texture_worst <dbl>, perimeter_worst <dbl>, area_worst <dbl>,
    ## #   smoothness_worst <dbl>, compactness_worst <dbl>, concavity_worst <dbl>, …

``` r
glimpse(cancer_sample)
```

    ## Rows: 569
    ## Columns: 32
    ## $ ID                      <dbl> 842302, 842517, 84300903, 84348301, 84358402, …
    ## $ diagnosis               <chr> "M", "M", "M", "M", "M", "M", "M", "M", "M", "…
    ## $ radius_mean             <dbl> 17.990, 20.570, 19.690, 11.420, 20.290, 12.450…
    ## $ texture_mean            <dbl> 10.38, 17.77, 21.25, 20.38, 14.34, 15.70, 19.9…
    ## $ perimeter_mean          <dbl> 122.80, 132.90, 130.00, 77.58, 135.10, 82.57, …
    ## $ area_mean               <dbl> 1001.0, 1326.0, 1203.0, 386.1, 1297.0, 477.1, …
    ## $ smoothness_mean         <dbl> 0.11840, 0.08474, 0.10960, 0.14250, 0.10030, 0…
    ## $ compactness_mean        <dbl> 0.27760, 0.07864, 0.15990, 0.28390, 0.13280, 0…
    ## $ concavity_mean          <dbl> 0.30010, 0.08690, 0.19740, 0.24140, 0.19800, 0…
    ## $ concave_points_mean     <dbl> 0.14710, 0.07017, 0.12790, 0.10520, 0.10430, 0…
    ## $ symmetry_mean           <dbl> 0.2419, 0.1812, 0.2069, 0.2597, 0.1809, 0.2087…
    ## $ fractal_dimension_mean  <dbl> 0.07871, 0.05667, 0.05999, 0.09744, 0.05883, 0…
    ## $ radius_se               <dbl> 1.0950, 0.5435, 0.7456, 0.4956, 0.7572, 0.3345…
    ## $ texture_se              <dbl> 0.9053, 0.7339, 0.7869, 1.1560, 0.7813, 0.8902…
    ## $ perimeter_se            <dbl> 8.589, 3.398, 4.585, 3.445, 5.438, 2.217, 3.18…
    ## $ area_se                 <dbl> 153.40, 74.08, 94.03, 27.23, 94.44, 27.19, 53.…
    ## $ smoothness_se           <dbl> 0.006399, 0.005225, 0.006150, 0.009110, 0.0114…
    ## $ compactness_se          <dbl> 0.049040, 0.013080, 0.040060, 0.074580, 0.0246…
    ## $ concavity_se            <dbl> 0.05373, 0.01860, 0.03832, 0.05661, 0.05688, 0…
    ## $ concave_points_se       <dbl> 0.015870, 0.013400, 0.020580, 0.018670, 0.0188…
    ## $ symmetry_se             <dbl> 0.03003, 0.01389, 0.02250, 0.05963, 0.01756, 0…
    ## $ fractal_dimension_se    <dbl> 0.006193, 0.003532, 0.004571, 0.009208, 0.0051…
    ## $ radius_worst            <dbl> 25.38, 24.99, 23.57, 14.91, 22.54, 15.47, 22.8…
    ## $ texture_worst           <dbl> 17.33, 23.41, 25.53, 26.50, 16.67, 23.75, 27.6…
    ## $ perimeter_worst         <dbl> 184.60, 158.80, 152.50, 98.87, 152.20, 103.40,…
    ## $ area_worst              <dbl> 2019.0, 1956.0, 1709.0, 567.7, 1575.0, 741.6, …
    ## $ smoothness_worst        <dbl> 0.1622, 0.1238, 0.1444, 0.2098, 0.1374, 0.1791…
    ## $ compactness_worst       <dbl> 0.6656, 0.1866, 0.4245, 0.8663, 0.2050, 0.5249…
    ## $ concavity_worst         <dbl> 0.71190, 0.24160, 0.45040, 0.68690, 0.40000, 0…
    ## $ concave_points_worst    <dbl> 0.26540, 0.18600, 0.24300, 0.25750, 0.16250, 0…
    ## $ symmetry_worst          <dbl> 0.4601, 0.2750, 0.3613, 0.6638, 0.2364, 0.3985…
    ## $ fractal_dimension_worst <dbl> 0.11890, 0.08902, 0.08758, 0.17300, 0.07678, 0…

## Exploring vancouver_trees dataset

I called the data set and used the **glimpse** function in order to have
an idea of the variables names and type.I found this dataset not related
to my research area, but with a diversity of variables that might be
interesting for formulating research questions.

``` r
### EXPLORE HERE ###
vancouver_trees
```

    ## # A tibble: 146,611 × 20
    ##    tree_id civic_number std_st…¹ genus…² speci…³ culti…⁴ commo…⁵ assig…⁶ root_…⁷
    ##      <dbl>        <dbl> <chr>    <chr>   <chr>   <chr>   <chr>   <chr>   <chr>  
    ##  1  149556          494 W 58TH … ULMUS   AMERIC… BRANDON BRANDO… N       N      
    ##  2  149563          450 W 58TH … ZELKOVA SERRATA <NA>    JAPANE… N       N      
    ##  3  149579         4994 WINDSOR… STYRAX  JAPONI… <NA>    JAPANE… N       N      
    ##  4  149590          858 E 39TH … FRAXIN… AMERIC… AUTUMN… AUTUMN… Y       N      
    ##  5  149604         5032 WINDSOR… ACER    CAMPES… <NA>    HEDGE … N       N      
    ##  6  149616          585 W 61ST … PYRUS   CALLER… CHANTI… CHANTI… N       N      
    ##  7  149617         4909 SHERBRO… ACER    PLATAN… COLUMN… COLUMN… N       N      
    ##  8  149618         4925 SHERBRO… ACER    PLATAN… COLUMN… COLUMN… N       N      
    ##  9  149619         4969 SHERBRO… ACER    PLATAN… COLUMN… COLUMN… N       N      
    ## 10  149625          720 E 39TH … FRAXIN… AMERIC… AUTUMN… AUTUMN… N       N      
    ## # … with 146,601 more rows, 11 more variables: plant_area <chr>,
    ## #   on_street_block <dbl>, on_street <chr>, neighbourhood_name <chr>,
    ## #   street_side_name <chr>, height_range_id <dbl>, diameter <dbl>, curb <chr>,
    ## #   date_planted <date>, longitude <dbl>, latitude <dbl>, and abbreviated
    ## #   variable names ¹​std_street, ²​genus_name, ³​species_name, ⁴​cultivar_name,
    ## #   ⁵​common_name, ⁶​assigned, ⁷​root_barrier

``` r
glimpse(vancouver_trees)
```

    ## Rows: 146,611
    ## Columns: 20
    ## $ tree_id            <dbl> 149556, 149563, 149579, 149590, 149604, 149616, 149…
    ## $ civic_number       <dbl> 494, 450, 4994, 858, 5032, 585, 4909, 4925, 4969, 7…
    ## $ std_street         <chr> "W 58TH AV", "W 58TH AV", "WINDSOR ST", "E 39TH AV"…
    ## $ genus_name         <chr> "ULMUS", "ZELKOVA", "STYRAX", "FRAXINUS", "ACER", "…
    ## $ species_name       <chr> "AMERICANA", "SERRATA", "JAPONICA", "AMERICANA", "C…
    ## $ cultivar_name      <chr> "BRANDON", NA, NA, "AUTUMN APPLAUSE", NA, "CHANTICL…
    ## $ common_name        <chr> "BRANDON ELM", "JAPANESE ZELKOVA", "JAPANESE SNOWBE…
    ## $ assigned           <chr> "N", "N", "N", "Y", "N", "N", "N", "N", "N", "N", "…
    ## $ root_barrier       <chr> "N", "N", "N", "N", "N", "N", "N", "N", "N", "N", "…
    ## $ plant_area         <chr> "N", "N", "4", "4", "4", "B", "6", "6", "3", "3", "…
    ## $ on_street_block    <dbl> 400, 400, 4900, 800, 5000, 500, 4900, 4900, 4900, 7…
    ## $ on_street          <chr> "W 58TH AV", "W 58TH AV", "WINDSOR ST", "E 39TH AV"…
    ## $ neighbourhood_name <chr> "MARPOLE", "MARPOLE", "KENSINGTON-CEDAR COTTAGE", "…
    ## $ street_side_name   <chr> "EVEN", "EVEN", "EVEN", "EVEN", "EVEN", "ODD", "ODD…
    ## $ height_range_id    <dbl> 2, 4, 3, 4, 2, 2, 3, 3, 2, 2, 2, 5, 3, 2, 2, 2, 2, …
    ## $ diameter           <dbl> 10.00, 10.00, 4.00, 18.00, 9.00, 5.00, 15.00, 14.00…
    ## $ curb               <chr> "N", "N", "Y", "Y", "Y", "Y", "Y", "Y", "Y", "Y", "…
    ## $ date_planted       <date> 1999-01-13, 1996-05-31, 1993-11-22, 1996-04-29, 19…
    ## $ longitude          <dbl> -123.1161, -123.1147, -123.0846, -123.0870, -123.08…
    ## $ latitude           <dbl> 49.21776, 49.21776, 49.23938, 49.23469, 49.23894, 4…

## Exploring flow_sample dataset

I called the data set and used the **glimpse** function in order to have
an idea of the variables names and type.This is a dataset not related to
my research area as well, but it´s small size could be helpful to start
learning about datasets analysis.

``` r
### EXPLORE HERE ###
flow_sample
```

    ## # A tibble: 218 × 7
    ##    station_id  year extreme_type month   day  flow sym  
    ##    <chr>      <dbl> <chr>        <dbl> <dbl> <dbl> <chr>
    ##  1 05BB001     1909 maximum          7     7   314 <NA> 
    ##  2 05BB001     1910 maximum          6    12   230 <NA> 
    ##  3 05BB001     1911 maximum          6    14   264 <NA> 
    ##  4 05BB001     1912 maximum          8    25   174 <NA> 
    ##  5 05BB001     1913 maximum          6    11   232 <NA> 
    ##  6 05BB001     1914 maximum          6    18   214 <NA> 
    ##  7 05BB001     1915 maximum          6    27   236 <NA> 
    ##  8 05BB001     1916 maximum          6    20   309 <NA> 
    ##  9 05BB001     1917 maximum          6    17   174 <NA> 
    ## 10 05BB001     1918 maximum          6    15   345 <NA> 
    ## # … with 208 more rows

``` r
glimpse(flow_sample)
```

    ## Rows: 218
    ## Columns: 7
    ## $ station_id   <chr> "05BB001", "05BB001", "05BB001", "05BB001", "05BB001", "0…
    ## $ year         <dbl> 1909, 1910, 1911, 1912, 1913, 1914, 1915, 1916, 1917, 191…
    ## $ extreme_type <chr> "maximum", "maximum", "maximum", "maximum", "maximum", "m…
    ## $ month        <dbl> 7, 6, 6, 8, 6, 6, 6, 6, 6, 6, 6, 7, 6, 6, 6, 7, 5, 7, 6, …
    ## $ day          <dbl> 7, 12, 14, 25, 11, 18, 27, 20, 17, 15, 22, 3, 9, 5, 14, 5…
    ## $ flow         <dbl> 314, 230, 264, 174, 232, 214, 236, 309, 174, 345, 185, 24…
    ## $ sym          <chr> NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, N…

## Exploring apt_buildings dataset

I called the data set and used the **glimpse** function in order to have
an idea of the variables names and type.I discarded this dataset due to
the reason that I saw many missing data and complex answers for the
variables.

``` r
### EXPLORE HERE ###
apt_buildings
```

    ## # A tibble: 3,455 × 37
    ##       id air_c…¹ ameni…² balco…³ barri…⁴ bike_…⁵ exter…⁶ fire_…⁷ garba…⁸ heati…⁹
    ##    <dbl> <chr>   <chr>   <chr>   <chr>   <chr>   <chr>   <chr>   <chr>   <chr>  
    ##  1 10359 NONE    Outdoo… YES     YES     0 indo… NO      YES     YES     HOT WA…
    ##  2 10360 NONE    Outdoo… YES     NO      0 indo… NO      YES     YES     HOT WA…
    ##  3 10361 NONE    <NA>    YES     NO      Not Av… NO      YES     NO      HOT WA…
    ##  4 10362 NONE    <NA>    YES     YES     Not Av… YES     YES     NO      HOT WA…
    ##  5 10363 NONE    <NA>    NO      NO      12 ind… NO      YES     NO      HOT WA…
    ##  6 10364 NONE    <NA>    NO      NO      Not Av… <NA>    YES     NO      HOT WA…
    ##  7 10365 NONE    <NA>    NO      YES     Not Av… NO      YES     NO      HOT WA…
    ##  8 10366 CENTRA… Indoor… YES     NO      Not Av… NO      YES     YES     HOT WA…
    ##  9 10367 NONE    <NA>    YES     YES     0 indo… NO      YES     YES     ELECTR…
    ## 10 10368 NONE    Indoor… YES     YES     Not Av… NO      YES     NO      HOT WA…
    ## # … with 3,445 more rows, 27 more variables: intercom <chr>,
    ## #   laundry_room <chr>, locker_or_storage_room <chr>, no_of_elevators <dbl>,
    ## #   parking_type <chr>, pets_allowed <chr>, prop_management_company_name <chr>,
    ## #   property_type <chr>, rsn <dbl>, separate_gas_meters <chr>,
    ## #   separate_hydro_meters <chr>, separate_water_meters <chr>,
    ## #   site_address <chr>, sprinkler_system <chr>, visitor_parking <chr>,
    ## #   ward <chr>, window_type <chr>, year_built <dbl>, year_registered <dbl>, …

``` r
glimpse(apt_buildings)
```

    ## Rows: 3,455
    ## Columns: 37
    ## $ id                               <dbl> 10359, 10360, 10361, 10362, 10363, 10…
    ## $ air_conditioning                 <chr> "NONE", "NONE", "NONE", "NONE", "NONE…
    ## $ amenities                        <chr> "Outdoor rec facilities", "Outdoor po…
    ## $ balconies                        <chr> "YES", "YES", "YES", "YES", "NO", "NO…
    ## $ barrier_free_accessibilty_entr   <chr> "YES", "NO", "NO", "YES", "NO", "NO",…
    ## $ bike_parking                     <chr> "0 indoor parking spots and 10 outdoo…
    ## $ exterior_fire_escape             <chr> "NO", "NO", "NO", "YES", "NO", NA, "N…
    ## $ fire_alarm                       <chr> "YES", "YES", "YES", "YES", "YES", "Y…
    ## $ garbage_chutes                   <chr> "YES", "YES", "NO", "NO", "NO", "NO",…
    ## $ heating_type                     <chr> "HOT WATER", "HOT WATER", "HOT WATER"…
    ## $ intercom                         <chr> "YES", "YES", "YES", "YES", "YES", "Y…
    ## $ laundry_room                     <chr> "YES", "YES", "YES", "YES", "YES", "Y…
    ## $ locker_or_storage_room           <chr> "NO", "YES", "YES", "YES", "NO", "YES…
    ## $ no_of_elevators                  <dbl> 3, 3, 0, 1, 0, 0, 0, 2, 4, 2, 0, 2, 2…
    ## $ parking_type                     <chr> "Underground Garage , Garage accessib…
    ## $ pets_allowed                     <chr> "YES", "YES", "YES", "YES", "YES", "Y…
    ## $ prop_management_company_name     <chr> NA, "SCHICKEDANZ BROS. PROPERTIES", N…
    ## $ property_type                    <chr> "PRIVATE", "PRIVATE", "PRIVATE", "PRI…
    ## $ rsn                              <dbl> 4154812, 4154815, 4155295, 4155309, 4…
    ## $ separate_gas_meters              <chr> "NO", "NO", "NO", "NO", "NO", "NO", "…
    ## $ separate_hydro_meters            <chr> "YES", "YES", "YES", "YES", "YES", "Y…
    ## $ separate_water_meters            <chr> "NO", "NO", "NO", "NO", "NO", "NO", "…
    ## $ site_address                     <chr> "65  FOREST MANOR RD", "70  CLIPPER R…
    ## $ sprinkler_system                 <chr> "YES", "YES", "NO", "YES", "NO", "NO"…
    ## $ visitor_parking                  <chr> "PAID", "FREE", "UNAVAILABLE", "UNAVA…
    ## $ ward                             <chr> "17", "17", "03", "03", "02", "02", "…
    ## $ window_type                      <chr> "DOUBLE PANE", "DOUBLE PANE", "DOUBLE…
    ## $ year_built                       <dbl> 1967, 1970, 1927, 1959, 1943, 1952, 1…
    ## $ year_registered                  <dbl> 2017, 2017, 2017, 2017, 2017, NA, 201…
    ## $ no_of_storeys                    <dbl> 17, 14, 4, 5, 4, 4, 4, 7, 32, 4, 4, 7…
    ## $ emergency_power                  <chr> "NO", "YES", "NO", "NO", "NO", "NO", …
    ## $ `non-smoking_building`           <chr> "YES", "NO", "YES", "YES", "YES", "NO…
    ## $ no_of_units                      <dbl> 218, 206, 34, 42, 25, 34, 14, 105, 57…
    ## $ no_of_accessible_parking_spaces  <dbl> 8, 10, 20, 42, 12, 0, 5, 1, 1, 6, 12,…
    ## $ facilities_available             <chr> "Recycling bins", "Green Bin / Organi…
    ## $ cooling_room                     <chr> "NO", "NO", "NO", "NO", "NO", "NO", "…
    ## $ no_barrier_free_accessible_units <dbl> 2, 0, 0, 42, 0, NA, 14, 0, 0, 1, 25, …

<!----------------------------------------------------------------------------->

1.3 Now that you’ve explored the 4 datasets that you were initially most
interested in, let’s narrow it down to 2. What lead you to choose these
2? Briefly explain your choices below, and feel free to include any code
in your explanation.

<!-------------------------- Start your work below ---------------------------->

## Selecting two datasets

1.  ***vancouver_trees*** It is a dataset easy to understand, the
    variables names are clear, and it permits to create many research
    questions. For example I could make plots to find out which are the
    most common species in a certain neighborhood.

2.***flow_sample*** It is a simple data set in size with only 7
variables and 218 observations. It might be easier to make data analysis
for a small size of variables in mind.

<!----------------------------------------------------------------------------->

1.4 Time for the final decision! Going back to the beginning, it’s
important to have an *end goal* in mind. For example, if I had chosen
the `titanic` dataset for my project, I might’ve wanted to explore the
relationship between survival and other variables. Try to think of 1
research question that you would want to answer with each dataset. Note
them down below, and make your final choice based on what seems more
interesting to you!

<!-------------------------- Start your work below ---------------------------->

## Research Questions for Datasets Selected

## Dataset \| Research Question

cancer_sample \| Which are the main differences in tumor characteristics
between benign and malign diagnosis? vancouver_trees \| What are the
trees distribution around neighborhoods in Vancouver? flow_sample \|
What are the levels of flow across time? apt_buildings \| How safe and
comfortable are the buildings of apartments?
<!----------------------------------------------------------------------------->

# Important note

Read Tasks 2 and 3 *fully* before starting to complete either of them.
Probably also a good point to grab a coffee to get ready for the fun
part!

This project is semi-guided, but meant to be *independent*. For this
reason, you will complete tasks 2 and 3 below (under the **START HERE**
mark) as if you were writing your own exploratory data analysis report,
and this guidance never existed! Feel free to add a brief introduction
section to your project, format the document with markdown syntax as you
deem appropriate, and structure the analysis as you deem appropriate.
Remember, marks will be awarded for completion of the 4 tasks, but 10
points of the whole project are allocated to a reproducible and clean
analysis. If you feel lost, you can find a sample data analysis
[here](https://www.kaggle.com/headsortails/tidy-titarnic) to have a
better idea. However, bear in mind that it is **just an example** and
you will not be required to have that level of complexity in your
project.

# Task 2: Exploring your dataset (15 points)

If we rewind and go back to the learning objectives, you’ll see that by
the end of this deliverable, you should have formulated *4* research
questions about your data that you may want to answer during your
project. However, it may be handy to do some more exploration on your
dataset of choice before creating these questions - by looking at the
data, you may get more ideas. **Before you start this task, read all
instructions carefully until you reach START HERE under Task 3**.

2.1 Complete *4 out of the following 8 exercises* to dive deeper into
your data. All datasets are different and therefore, not all of these
tasks may make sense for your data - which is why you should only answer
*4*. Use *dplyr* and *ggplot*.

1.  Plot the distribution of a numeric variable.
2.  Create a new variable based on other variables in your data (only if
    it makes sense)
3.  Investigate how many missing values there are per variable. Can you
    find a way to plot this?
4.  Explore the relationship between 2 variables in a plot.
5.  Filter observations in your data according to your own criteria.
    Think of what you’d like to explore - again, if this was the
    `titanic` dataset, I may want to narrow my search down to passengers
    born in a particular year…
6.  Use a boxplot to look at the frequency of different observations
    within a single variable. You can do this for more than one variable
    if you wish!
7.  Make a new tibble with a subset of your data, with variables and
    observations that you are interested in exploring.
8.  Use a density plot to explore any of your variables (that are
    suitable for this type of plot).

2.2 For each of the 4 exercises that you complete, provide a *brief
explanation* of why you chose that exercise in relation to your data (in
other words, why does it make sense to do that?), and sufficient
comments for a reader to understand your reasoning and code.

<!-------------------------- Start your work below ---------------------------->

# *Task 2*

## 2.1 Plotting the distribution of a numeric variable

I plotted the diameter of the trees of Vancouver.I chose the diameter
variable since it was a numeric variable that would be expected to be
normally distributed.

``` r
ggplot(vancouver_trees, aes(x=diameter)) + geom_density()
```

![](MiniDataAnalysis_EEspin_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->
\## 2.2 Creating a new variable based on other variables in my data I
decided to calculate the Height-to-diameter ratio (HDR) dividing the
height_range_id variable by the diameter variable. I chose to create the
HDR variable due to the fact that it is a tree-level index of
slenderness and is used for the evaluation of tree and stand stability.

``` r
vancouver_trees %>%
  mutate(HDR = height_range_id * diameter) %>%
  select(tree_id, HDR, height_range_id, diameter)
```

    ## # A tibble: 146,611 × 4
    ##    tree_id   HDR height_range_id diameter
    ##      <dbl> <dbl>           <dbl>    <dbl>
    ##  1  149556    20               2     10  
    ##  2  149563    40               4     10  
    ##  3  149579    12               3      4  
    ##  4  149590    72               4     18  
    ##  5  149604    18               2      9  
    ##  6  149616    10               2      5  
    ##  7  149617    45               3     15  
    ##  8  149618    42               3     14  
    ##  9  149619    32               2     16  
    ## 10  149625    15               2      7.5
    ## # … with 146,601 more rows

## 2.3 Explore the relationship between 2 variables in a plot

I tried to observe the relationship between the height range of the
trees and the street side. I considered it would be interesting to have
an idea of where are the highest trees capable of growing.

``` r
ggplot(data = vancouver_trees) + 
  geom_point(mapping = aes(x = street_side_name, y = height_range_id))
```

![](MiniDataAnalysis_EEspin_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->
\## 2.4 Filter observations in your data according to your own criteria
I filtered the observations to Kitsilano neighborhood. I chose Kistilano
neighborhood because it is a touristic known place of Vancouver, and
people may be interested in what kind of tree species are in there.

``` r
vancouver_trees %>% 
  filter(neighbourhood_name == "KITSILANO") %>% 
  select(neighbourhood_name, species_name, diameter)
```

    ## # A tibble: 8,115 × 3
    ##    neighbourhood_name species_name  diameter
    ##    <chr>              <chr>            <dbl>
    ##  1 KITSILANO          CERASIFERA        10  
    ##  2 KITSILANO          AMERICANA         14.5
    ##  3 KITSILANO          FREEMANI   X       3  
    ##  4 KITSILANO          RUBRUM            16  
    ##  5 KITSILANO          BIGNONIOIDES      30  
    ##  6 KITSILANO          ROBUR             18  
    ##  7 KITSILANO          PENNSYLVANICA     14  
    ##  8 KITSILANO          PENNSYLVANICA     17.8
    ##  9 KITSILANO          CAMPESTRE         10  
    ## 10 KITSILANO          AMERICANA         10  
    ## # … with 8,105 more rows

<!----------------------------------------------------------------------------->

# Task 3: Write your research questions (5 points)

So far, you have chosen a dataset and gotten familiar with it through
exploring the data. Now it’s time to figure out 4 research questions
that you would like to answer with your data! Write the 4 questions and
any additional comments at the end of this deliverable. These questions
are not necessarily set in stone - TAs will review them and give you
feedback; therefore, you may choose to pursue them as they are for the
rest of the project, or make modifications!

<!--- *****START HERE***** --->

## Tasks 3. Research Questions

1.  Which is the diameter of the trees in Vancouver?
2.  Which is the neighborhood with the population of highest trees in
    Vancouver?
3.  What are the most frequent tree species in Kistilano?
4.  Is there any relationship between the height and diameter of the
    trees related to their age?

# Task 4: Process and summarize your data (13 points)

From Task 2, you should have an idea of the basic structure of your
dataset (e.g. number of rows and columns, class types, etc.). Here, we
will start investigating your data more in-depth using various data
manipulation functions.

### 1.1 (10 points)

Now, for each of your four research questions, choose one task from
options 1-4 (summarizing), and one other task from 4-8 (graphing). You
should have 2 tasks done for each research question (8 total). Make sure
it makes sense to do them! (e.g. don’t use a numerical variables for a
task that needs a categorical variable.). Comment on why each task helps
(or doesn’t!) answer the corresponding research question.

Ensure that the output of each operation is printed!

**Summarizing:**

1.  Compute the *range*, *mean*, and *two other summary statistics* of
    **one numerical variable** across the groups of **one categorical
    variable** from your data.
2.  Compute the number of observations for at least one of your
    categorical variables. Do not use the function `table()`!
3.  Create a categorical variable with 3 or more groups from an existing
    numerical variable. You can use this new variable in the other
    tasks! *An example: age in years into “child, teen, adult, senior”.*
4.  Based on two categorical variables, calculate two summary statistics
    of your choosing.

**Graphing:**

5.  Create a graph out of summarized variables that has at least two
    geom layers.
6.  Create a graph of your choosing, make one of the axes logarithmic,
    and format the axes labels so that they are “pretty” or easier to
    read.
7.  Make a graph where it makes sense to customize the alpha
    transparency.
8.  Create 3 histograms out of summarized variables, with each histogram
    having different sized bins. Pick the “best” one and explain why it
    is the best.

Make sure it’s clear what research question you are doing each operation
for!

<!------------------------- Start your work below ----------------------------->

## Task 4. **Question 1**: Which is the diameter of the trees in Vancouver?

I computed the following summary statistics: mean, median, minimum and
maximum. This task could help to have a broader information about the
diameter of the trees in Vancouver according to each neighborhood.

``` r
vancouver_trees %>%
  group_by(neighbourhood_name) %>%
  summarise(range(diameter), mean(diameter), median(diameter), min(diameter), max(diameter))
```

    ## `summarise()` has grouped output by 'neighbourhood_name'. You can override
    ## using the `.groups` argument.

    ## # A tibble: 44 × 6
    ## # Groups:   neighbourhood_name [22]
    ##    neighbourhood_name `range(diameter)` `mean(diameter)` media…¹ min(d…² max(d…³
    ##    <chr>                          <dbl>            <dbl>   <dbl>   <dbl>   <dbl>
    ##  1 ARBUTUS-RIDGE                   0               11.9     10      0         62
    ##  2 ARBUTUS-RIDGE                  62               11.9     10      0         62
    ##  3 DOWNTOWN                        1                7.45     6      1        151
    ##  4 DOWNTOWN                      151                7.45     6      1        151
    ##  5 DUNBAR-SOUTHLANDS               0               13.9     12      0        305
    ##  6 DUNBAR-SOUTHLANDS             305               13.9     12      0        305
    ##  7 FAIRVIEW                        1.25            10.6      9      1.25      99
    ##  8 FAIRVIEW                       99               10.6      9      1.25      99
    ##  9 GRANDVIEW-WOODLAND              0               11.4      8.5    0         63
    ## 10 GRANDVIEW-WOODLAND             63               11.4      8.5    0         63
    ## # … with 34 more rows, and abbreviated variable names ¹​`median(diameter)`,
    ## #   ²​`min(diameter)`, ³​`max(diameter)`

I made a box plot of the mean of the diameter of the trees in Vancouver
at each neighborhood.The mean diameter of the trees in Vancouver is
between 11.48 and 11.50. It could answer the first research question.

``` r
vancouver_trees %>%
  ggplot(mapping = aes(x=mean(diameter), y=neighbourhood_name)) + geom_boxplot()
```

![](MiniDataAnalysis_EEspin_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

## Task 4. **Question 2**: Which is the neighborhood with the population of highest trees in Vancouver?

First, I computed the number of trees with a height range higher than 9.
Then, counted the number of trees of that height in each neighborhood.

``` r
  vancouver_trees %>% 
  filter(height_range_id > 9 ) %>%
  select(neighbourhood_name, height_range_id)
```

    ## # A tibble: 12 × 2
    ##    neighbourhood_name       height_range_id
    ##    <chr>                              <dbl>
    ##  1 KITSILANO                             10
    ##  2 KITSILANO                             10
    ##  3 MARPOLE                               10
    ##  4 KENSINGTON-CEDAR COTTAGE              10
    ##  5 KENSINGTON-CEDAR COTTAGE              10
    ##  6 KERRISDALE                            10
    ##  7 SHAUGHNESSY                           10
    ##  8 RENFREW-COLLINGWOOD                   10
    ##  9 RILEY PARK                            10
    ## 10 DUNBAR-SOUTHLANDS                     10
    ## 11 DUNBAR-SOUTHLANDS                     10
    ## 12 ARBUTUS-RIDGE                         10

Later, I plotted the trees bigger than height range 10 in each
neighborhood. I transformed the X axis to logarithmic; however, it was
non informative.

``` r
  vancouver_trees %>% 
  filter(height_range_id > 9 ) %>%
  select(neighbourhood_name, height_range_id) %>%
  ggplot (mapping = aes(x=height_range_id, y =neighbourhood_name)) + geom_bar(stat="identity") +
 ylab("Neighborhoods in Vancouver") +
 scale_x_log10()
```

![](MiniDataAnalysis_EEspin_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->
Therefore, I returned to the plot without the logarithmic axis and
improved the x axis label. I concluded that Kitsilano, Kensington-Cedar
Cottage, and Arbutus-Ridge are the neighborhoods with the higher trees
in Vancouver.

``` r
  vancouver_trees %>% 
  filter(height_range_id > 9 ) %>%
  select(neighbourhood_name, height_range_id) %>%
  ggplot (mapping = aes(x=height_range_id, y =neighbourhood_name)) + geom_bar(stat="identity") +
 ylab("Neighborhoods in Vancouver") +
  xlab("Number of Trees with a height range > 9")
```

![](MiniDataAnalysis_EEspin_files/figure-gfm/unnamed-chunk-14-1.png)<!-- -->
\## Task 4. **Question 3**: What are the most frequent tree species in
Kistilano? Considering the previous conclusions, I focused in one of the
neighborhoods with the highest trees, Kitsilano. I wanted to find out
which species is the most frequent in that neighborhood, and possibly
that species is one of the highest trees in Vancouver. First, I computed
the number of trees of each species in Kistilano, and sort them in a
descendant order.

``` r
vancouver_trees %>% 
  filter(neighbourhood_name == "KITSILANO") %>% 
  count (species_name) %>%
  arrange(desc(n))
```

    ## # A tibble: 171 × 2
    ##    species_name      n
    ##    <chr>         <int>
    ##  1 PLATANOIDES    1188
    ##  2 SERRULATA       559
    ##  3 CERASIFERA      435
    ##  4 EUCHLORA   X    432
    ##  5 RUBRUM          315
    ##  6 KOBUS           289
    ##  7 HIPPOCASTANUM   277
    ##  8 ROBUR           263
    ##  9 AMERICANA       260
    ## 10 SYLVATICA       246
    ## # … with 161 more rows

Second, I created a graph for visualization of the 10 most frequent
species in Kitsilano, but first I filtered only the trees with a
frequency number bigger than 240. I identified Platanoides species as
the most frequent in Kitsilano.

``` r
vancouver_trees %>% 
  filter(neighbourhood_name == "KITSILANO") %>% 
  count (species_name) %>%
  arrange(desc(n)) %>%
  filter(n > 240) %>%
  ggplot(mapping = aes(x=species_name, y=n)) +
  geom_bar(stat="identity", width = 0.7) +
  ylab("Number of trees") +
  coord_flip()
```

![](MiniDataAnalysis_EEspin_files/figure-gfm/unnamed-chunk-16-1.png)<!-- -->
\## Task 4. **Question 4**: Is there any relationship between the height
and diameter of the trees related to their age? I plotted the height of
the trees versus the date in which they were planted, and assigned the
alpha aesthetic to the diameter of the tree.

``` r
vancouver_trees %>% 
  ggplot(mapping = aes(x = height_range_id, y = date_planted, alpha = diameter)) +
  geom_point()
```

    ## Warning: Removed 76548 rows containing missing values (geom_point).

![](MiniDataAnalysis_EEspin_files/figure-gfm/unnamed-chunk-17-1.png)<!-- -->
Next, I computed the number of trees with a height range \> 8 according
to the date when the trees where planted. I hypothesized that the older
the date of planting, the highest the tree; however it could not be
answered with this computing excercise since there are many missing data
for the “date_planted” variable.

``` r
vancouver_trees %>% 
  select(date_planted, height_range_id, diameter) %>%
  filter(height_range_id > 8 ) %>% 
  count (date_planted) 
```

    ## # A tibble: 8 × 2
    ##   date_planted     n
    ##   <date>       <int>
    ## 1 1995-12-15       1
    ## 2 1998-01-06       1
    ## 3 1998-02-02       1
    ## 4 1999-09-23       1
    ## 5 2001-04-11       1
    ## 6 2006-02-13       1
    ## 7 2006-02-14       1
    ## 8 NA             208

<!----------------------------------------------------------------------------->

### 1.2 (3 points)

Based on the operations that you’ve completed, how much closer are you
to answering your research questions? Think about what aspects of your
research questions remain unclear. Can your research questions be
refined, now that you’ve investigated your data a bit more? Which
research questions are yielding interesting results?

<!-------------------------- Start your work below ---------------------------->

### Task 4 conclusions

I formulated simple and specific research questions intentionally,
considering the basic analysis I am capable of doing at this point of my
learning curve of data analysis in R. In a near future I would like to
fomulate more interesting questions that involve analysis of
correlations, regressions, and some others.

As the questions were simple, most of them were answered. I determined
that the mean diameter of trees in Vancouver is between 11.48 and 11.50
for the first question. Then, I determined that Kitsilano,
Kensington-Cedar Cottage, and Arbutus-Ridge are the neighborhoods with
the higher trees in Vancouver, my second research question.
Subsequently, I observed that Platanoides is the most popular species of
tree in Kistilano. Finally, I could not determine if there is any
relationship between the height and diameter of the trees related to
their age. I could have an idea that the highest trees have the biggest
diameters, but I could not relate that to the planting date of the tree.
One reason is that there were many missing data in the planting date
variable, but also more complex analysis as correlations could answer
this last question.
<!----------------------------------------------------------------------------->

### Attribution

Thanks to Icíar Fernández Boyano for mostly putting this together, and
Vincenzo Coia for launching.
