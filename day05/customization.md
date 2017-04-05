# [fit] Polishing
# [fit] Graphics

---

# New packages

Be sure to install these packages: `RColorBrewer`, `ggthemes`, `viridis`

<br>

`install.packages("RColorBrewer")`
`install.packages("ggthemes")`
`install.packages("viridis")`

---

# Timeline

- HW-2 due Sunday by 11:59 p.m.
- Mini-project 1 due by Fri., April 14 at 9:50 a.m.
	+ Work in pairs
	+ Choose your own data set
	+ Create a data graphic
	+ Write a short "blog post"
	+ Present your graphic

---

# What we know

- A basic set of geometries
- How to map variables to aesthetics
- How to *set* colors
- How to change axis labels and titles
- How to add text annotations

---

# What else is there?

- Reordering factors
- Changing color scales
- Changing themes

---

## Your turn

---

**Task:** Recreate this graphic from *The Economist*

- `ScorecardSmallNarrow.csv` available on the course website
- Variables include:
	1. `CONTROL`: public (1) or private (2) institution. 
	2. `ADM_RATE`: admissions rate (%)
	3. `income_group`: income quintile
	4. `net_cost`: avg. net cost for students
- Hint: `geom_smooth` will help
￼


![left fit](20160919_woc701.png)

---

# Polishing

---

![left 110%](https://espnfivethirtyeight.files.wordpress.com/2014/05/silver-feature-names-dead2.png?quality=90&strip=all&w=575&ssl=1)

## Goals
- bar chart for names
- faceting and fill by sex
- flip the axes
- text giving the percentages

---

# Changing scales

**Recipe:** `scale_<aes>_<method>`

**Examples:**

- `scale_fill_manual`
- `scale_fill_brewer`
- `scale_color_viridis`
- `scale_shape_manual`

---

# Changing themes

Loading `ggthemes` allows you to access numerous [prebuilt themes](https://cran.r-project.org/web/packages/ggthemes/vignettes/ggthemes.html)

- `theme_wsj()`
- `theme_few()`
- `theme_hc()`
- `theme_gdocs()`

---

# Custom themes

- `theme()` function allows us to fine tune every aspect of our plot canvas
- A LOT of decisions (run `?theme` to see more)
- A LOT of control

---

![left fit](538plot.pdf)

```
dnplot2 +
  theme_fivethirtyeight() +
  theme(legend.position = "none",     
        panel.grid = element_blank(), 
        strip.text = element_blank(), 
        axis.text.x = element_blank() 
        )
```