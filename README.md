# 2015-09-21-six-lines-to-install-and-start-sparkr-on-mac-os-x-yosemite

Codes for http://opiateforthemass.es/articles/six-lines-to-install-and-start-sparkr-on-mac-os-x-yosemite/
```
brew update # If you don't have homebrew, get it from here (http://brew.sh/)
brew install hadoop # Install Hadoop
brew install apache-spark # Install Spark
```


``` r
spark_path <- strsplit(system("brew info apache-spark",intern=T)[4],' ')[[1]][1] # Get your spark path
.libPaths(c(file.path(spark_path,"libexec", "R", "lib"), .libPaths())) # Navigate to SparkR folder
library(SparkR) # Load the library
```