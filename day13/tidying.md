# Tidy Data

---

# From last time...

## Does payroll differ between the American League and the National League?

- Load the `tidyverse`
- Install and load the `Lahman` R package 
- Look at the `Salaries` and `Teams` data tables
- Devise a way to clearly compare the team payroll between the two leagues over the years

---

# Definition: tidy data

![inline](http://r4ds.had.co.nz/images/tidy-1.png)

1. Each variable forms a column
2. Each observation (case) forms a row
3. Each type of observational unit forms a table

---

# Gathering

`table4a %>%`
`gather(key = "year", value = "cases", -country)`


![inline](http://r4ds.had.co.nz/images/tidy-9.png)

---

# Spreading 

`table2 %>%`
`spread(key = type, value = count)`

![inline](http://r4ds.had.co.nz/images/tidy-8.png)


---

## Your turn

- Data: `french_fries.csv`

- 10 week sensory experiment, 12 individuals asked to assess taste of french fries on several scales (how potato-y, buttery, grassy, rancid, paint-y do the fries taste?)

- French fries fried in 1 of 3 different oils, each week individuals had to assess 6 batches of french fries (all 3 oils, replicated 2x)

- Create boxplots of the numeric ratings by scale


---

# Separate

`table3 %>%`
`separate(rate, into = c("cases", "population"))`

![inline](http://r4ds.had.co.nz/images/tidy-17.png)

---

# Unite

`table5 %>%`
`unite(year, century, year, sep = "")`


![inline](http://r4ds.had.co.nz/images/tidy-18.png)

---

# Why do we care?

- In the `tidyverse` input and outputs of all functions are encouraged to follow the tidy data format

- You might not be able to analyze the data in wide/long format depending on the type of analysis you want to run, or the plot you want to create

---

## Your turn

`polls.csv` contains the results of various presidential polls conducted during July 2016, and was scraped from RealClear Politics.

1. Briefly describe why it is not considered to be tidy data and what changes need to be made to tidy it.

2. Use `separate` and `gather` to tidy the data set.

---

## Your turn

under5mortality.csv contains the child mortality rate per 1,000 children born for each country from 1800 to 2015. 

1. Briefly describe why it is not considered to be tidy data and what changes need to be made to tidy it.

2. Create a tidy data set with columns country, year and mortality. Use `parse_numeric` to ensure that the  year column is numeric (see `?parse_numeric` for help).

---

## Your turn

`mlb2016.csv` contains the salary information presented by USA Today for all 862 players in Major League Baseball. 

1. Briefly describe why it is not considered to be tidy data and what changes need to be made to tidy it.

2. Tidy this data set.