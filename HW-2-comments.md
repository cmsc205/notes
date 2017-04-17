# HW-2 Comments

---

## Coding style

### Start a new line for each layer

```
ggplot(dead_names, aes(x = reorder(name, pct_dead), y = pct_dead, fill = sex)) +
  geom_bar(stat = "identity") +
  geom_text(aes(label = pct_dead), hjust = -.1) +
  facet_wrap(~sex, scales = "free_y", ncol = 1) +
  coord_flip() +
  ylim(0, 95) +
  labs(x = NULL, y = NULL, 
       title = "Deadest Names",
       subtitle = "Estimated percentage of Americans with a given name born since\n1900 who were dead as of Jan. 1, 2014") +
  scale_fill_manual(values = c("#f6b900", "#008fd5")) +
  theme_fivethirtyeight() +
  theme(legend.position = "none", panel.grid = element_blank(), 
        strip.text = element_blank(), axis.text.x = element_blank())
```

---

## Label your plots

- Axis labels (unless obvious)
- Informative title
- Informative legend title

---

## Maps

- x = longitude
- y = latitude
