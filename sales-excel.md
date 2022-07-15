Sales
================
Morgan Shumaker

``` r
library(tidyverse)
library(readxl)
```

-   Read in the Excel file called `sales.xlsx` from the `data-raw/`
    folder such that it looks like the following.

<img src="images/sales-1.png" width="20%" />

``` r
sales <- read_excel("data-raw/sales.xlsx", skip = 3, col_names = c("id","n"))
```

-   **Stretch goal:** Manipulate the sales data such such that it looks
    like the following.

``` r
sales %>%
mutate(is_brand_name = str_detect(id, "Brand"))
```

    ## # A tibble: 9 × 3
    ##   id      n     is_brand_name
    ##   <chr>   <chr> <lgl>        
    ## 1 Brand 1 n     TRUE         
    ## 2 1234    8     FALSE        
    ## 3 8721    2     FALSE        
    ## 4 1822    3     FALSE        
    ## 5 Brand 2 n     TRUE         
    ## 6 3333    1     FALSE        
    ## 7 2156    3     FALSE        
    ## 8 3987    6     FALSE        
    ## 9 3216    5     FALSE

<img src="images/sales-2.png" width="25%" />
