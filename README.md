# RMPSS

Contains R package and MATLAB codes.

# To install the R package execute following code
library(devtools) 

install_github("priyamdas2/RMPSS")

library(RMPSS)

?RMPSS_opt
g <- function(y)
return(-20 * exp(-0.2 * sqrt(0.5 * (y[1] ^ 2 + (y[2]-1) ^ 2)))
 - exp(0.5 * (cos(2 * pi * y[1]) + cos(2 * pi * (y[2]-1))))
 + exp(1) + 20)

### global min value is 0, achieved at c(0,1)
starting_point <- c(0.4,0.6)
g(starting_point)
solution <- RMPSS_opt(starting_point,g)
g(solution)

