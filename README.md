# InvestmentCaseStudy

companies <- read.delim("companies.txt", header = TRUE)
rounds2 <- read.csv("rounds2.csv", stringsAsFactors = FALSE)

#Table 1.1: Understand the Data Set
#1. How many unique companies are present in rounds2?
#Method1: Using Dplyr: 
count(distinct(rounds2, company_permalink))

#Method2: Without using any external packages: 
length(unique(rounds2$company_permalink))


#2. How many unique companies are present in the companies file?
# Understanding is permalink link coulmn in companes is the primary key. 
# Therefore number of rows equals the unique companies
#Method1: Using Dplyr: 
count(distinct(companies, permalink))

#Method2: Without using any external packages: 
length(unique(companies$permalink))
