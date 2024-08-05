# hugo-apero-website

This is the main website for personal portfolio. 
This is deployed using netlify.

follow this tutorial for instructions - https://hugo-apero-docs.netlify.app/start/setup/

# for serving site loacally for developments

#!/usr/bin/env Rscript
library(blogdown)
blogdown::build_site(build_rmd = "timestamp")
blogdown::serve_site()
