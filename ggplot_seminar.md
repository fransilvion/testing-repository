ggplot seminar
================
German Novakovskiy
9 January 2018

Mpg plot
--------

At first we should load tidyverse library:

``` r
library(tidyverse)
```

    ## Warning: package 'tidyverse' was built under R version 3.4.3

    ## -- Attaching packages ---------------------------------- tidyverse 1.2.1 --

    ## v ggplot2 2.2.1     v purrr   0.2.4
    ## v tibble  1.4.1     v dplyr   0.7.4
    ## v tidyr   0.7.2     v stringr 1.2.0
    ## v readr   1.1.1     v forcats 0.2.0

    ## Warning: package 'ggplot2' was built under R version 3.4.3

    ## Warning: package 'tibble' was built under R version 3.4.3

    ## Warning: package 'tidyr' was built under R version 3.4.3

    ## Warning: package 'readr' was built under R version 3.4.3

    ## Warning: package 'purrr' was built under R version 3.4.3

    ## Warning: package 'dplyr' was built under R version 3.4.3

    ## Warning: package 'forcats' was built under R version 3.4.3

    ## -- Conflicts ------------------------------------- tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

After this we should run this chunk of code in order to build desirable plot:

``` r
ggplot(data = mpg, 
       mapping = aes(x = displ, y = hwy, color = drv, size = class)) +
  geom_point()
```

    ## Warning: Using size for a discrete variable is not advised.

![](ggplot_seminar_files/figure-markdown_github/cars-1.png)
