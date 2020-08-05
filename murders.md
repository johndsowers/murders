Report on Gun Murders
================
Rafael Irizarry
2020-08-04

library(tidyverse) load(“rda/murders.rda”)

murders %\>% mutate(abb = reorder(abb, rate)) %\>% ggplot(aes(abb,
rate)) + geom\_bar(width = 0.5, stat = “identity”, color = “black”) +
coord\_flip()

ggsave(“figs/barplot.png”)
