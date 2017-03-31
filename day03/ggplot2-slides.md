# [fit] ggplot2

---

## The grammar of graphics


Comprised of **building blocks** of plots that we can combine to create just about any plot we would like

---

## Building blocks

- data
- geometric object (the marks we actually draw)
- aesthetic mappings (how we draw the marks)
- statistical transformations (how we transform data before plotting)
- scales (ranges of values, colors, shapes, sizes, etc.)
- faceting (small multiples)

---

## Geometric objects

- In `ggplot2`, the type of marks we draw are set by `geom`s

- Examples:
	+ `geom_point`
	+ `geom_line`
	+ `geom_bar`
	+ `geom_boxplot`

- [Data vis cheatsheet](https://www.rstudio.com/wp-content/uploads/2016/11/ggplot2-cheatsheet-2.1.pdf) contains a more complete list

---

## Aesthetic mapping

- In `ggplot2`, set with the `aes()` function
- `aes()` **maps variables** to aesthetics
- Different geoms accept different aesthetics
	+ `position` (on the x and y axes)
	+ `color` ("outside" color)
	+ `fill` ("insde" color)
	+ `shape` 
	+ `linetype`

---

## Key questions

1. What do we want R to do? (What is the goal?)
1. What does R need to know?

---
## How do we make this plot?

![inline 170%](first_example_plot.pdf)

---

![left fit](first_example_plot.pdf)

## How do we make this plot?

1. Goal: scatterplot = plot with points
	+ `ggplot() + geom_point()`
1. What does R need to know?
	+ data source: `data = mpg`
	+ aesthetics: 
	`aes(x = displacement, 
	y = highway,
	color = class)`

---

`ggplot(data = mpg, 
  aes(x=displacement, y=highway, color=class)) + 
  geom_point()`

![fit](first_example_plot.pdf)