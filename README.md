# rna_wrangle
My assignment of week 6
## Files need to be downloaded ##
git clone https://github.com/tgrn510/RNASeqExample.git
### 1. Install packages and import the data ###
#install.packages("dplyr")
#install.packages("reshape")
#install.packages("ggplot2")
library("dplyr")
library("reshape")
library("ggplot2")
setwd("/Users/lyn/test/RNASeqExample/RNASeqExample")
samples<-read.csv("sample_info.csv", header = TRUE, sep = ",", quote = "\"", dec = ".", fill = TRUE, row.names = 1)
genes<-read.csv("expression_results.csv", header = TRUE, sep = ",", quote = "\"", dec = ".", fill = TRUE, row.names = 1)
plot(density(log2(genes$KITA_02[(genes$KITA_02>0)])))
#row.names = 1 definded that gene names in axis or in the first column#

