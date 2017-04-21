
# Joining
# Data Tables

---

## Motivation

An online retailer stores customer data in two places: <br>

```
orders                      customers
  order id   date              id    name
1     1  4 Jan-01            1  4   Tukey
2     2  8 Feb-01            2  8 Wickham
3     3 42 Apr-15            3 15   Mason
4     4 50 Apr-17            4 16  Jordan
                             5 23   Patil
                             6 42     Cox
```

---

## Types of joins

1. **Mutating joins** - add new variables to one data frame from matching observations in another
<br>

2. **Filtering joins** - filter observations from one data frame based on whether or not they match an observation in the other

---
  
## Keys

Used to connect two data tables

- **primary key** uniquely identifies an observation in its own table

- **foreign key** uniquely identifies an observation in another table


---

## `inner_join`

An `inner_join` matches pairs of observations when their keys are equal

![inline](http://r4ds.had.co.nz/diagrams/join-inner.png)

---

## `inner_join`

```{r}
inner_join(x = orders, y = customers, by = "id")
```

![inline](inner_join2.png)


---

## Outer joins

**Outer joins** keeps the rows (observations) that appear in a specified table

---

![left 220%](http://r4ds.had.co.nz/diagrams/join-outer.png)

A **left join** keeps all observations in the `x` table

<br>
<br>

A **right join** keeps all observations in the `y` table

<br>
<br>
<br>

A **full join** keeps all observations in both the `x` and `y` tables


---

```{r}
left_join(x = orders, y = customers, by = "id")
```

---

```{r}
right_join(x = orders, y = customers, by = "id")
```

---

```{r}
full_join(x = orders, y = customers, by = "id")
```

---

## Filtering joins

Filtering joins still match observations between two data tables, but do not add additional variables, they only impact the rows returned.

1. `semi_join(x, y)` keeps all observations in `x` that have a match in `y`

2. `anti_join(x, y)` drops all observations in `x` that have a match in `y`

---

## `semi_join(x, y)`

![inline](http://r4ds.had.co.nz/diagrams/join-semi.png)

Observations will never be duplicated.

![inline](http://r4ds.had.co.nz/diagrams/join-semi-many.png)


---

## `anti_join(x, y)`

![inline](http://r4ds.had.co.nz/diagrams/join-anti.png)

---


```{r}
semi_join(x = orders, y = customers, by = "id")
```

---

What if we had an extra order?

```{r}
extra_order <- data.frame(order = 5, id = 42, date = "May-01")
extra_order
```

```{r}
orders2 <- rbind(orders, extra_order)
orders2
```

---

How do `semi_join` and `inner_join` differ?

```{r}
semi_join(x = customers, y = orders2, by = "id")
```


```{r}
inner_join(x = customers, y = orders2, by = "id")
```

---

For an `anti_join`, order matters

```{r}
anti_join(x = orders, y = customers, by = "id")
```

```{r}
anti_join(x = customers, y = orders, by = "id")
```

---

## Common complications

---

## Joining by multiple variables, 

You must specify a vector of variable names: 

`by = c("var1", "var2", "var3")`. 

Here all three columns must match in both tables.

---

## Use all variables that appear in both tables

Leave the `by` argument blank.

---

## Column names differ between tables

`by = c("left_var" = "right_var")`.

---

# Your Turn


----

## Set up for today

1. Load the tidyverse

2. Download the data folder from the webpage and put it in a logical directory on your computer. 

3. Open an R markdown file and load the data using the appropriate relative file path.


```{r}
orders <- read.csv("data/orders.csv", as.is = TRUE)
customers <- read.csv("data/customers.csv", as.is = TRUE)
```
