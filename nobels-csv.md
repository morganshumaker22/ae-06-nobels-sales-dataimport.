Nobel winners
================
Morgan Shumaker

``` r
library(tidyverse)
```

Let’s first load the data:

``` r
nobel <- read.csv("data-raw/nobel.csv")
```

Then let’s split the data into two:

``` r
#stem_laureates
nobel_stem <- nobel %>%
  filter(category %in% c("Physics", "Economics", "Chemistry", "Medicine"))
#not_stem_laureate
nobel_nonstem <- nobel %>%
  filter(!category %in% c("Physics", "Economics", "Chemistry", "Medicine"))
```

And finally write out the data:

``` r
#write.csv(nobel_stem, file = "data/nobel_stem.csv")
```

``` r
#write.csv(nobel_nonstem, file = "data/nobel_nonstem.csv")
```
