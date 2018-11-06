class: center, middle

# FISH 546
## Bioinformatics for Environmental Sciences

https://github.com/sr320/course-fish546-2018/wiki

##genefish.co

Week 6


Steven Roberts
@sr320

---

## Reminders

- Manuals (`-help`) can be useful

- Cloud RESOURCES

- Paths

---

class: center, middle


# R : scripting : find & xargs (411)

---


## Intro to R

Next slide have hyperlinks with exercises with answers.



---


## Intro to R

- [R and Rstudio](https://sr320.github.io/course-fish497-2018/assignments/r-intro/)


- [Working with data: dplyr](https://sr320.github.io/course-fish497-2018/assignments/r-data/)


- [Data Visualization: ggplot](https://sr320.github.io/course-fish497-2018/assignments/r-datavis/)


- [Project Structure](https://sr320.github.io/course-fish497-2018/materials/project-structure/)


- [Version Control with R](https://sr320.github.io/course-fish497-2018/materials/version-control-R)


- [knitr / Rmarkdown](https://sr320.github.io/course-fish497-2018/assignments/knitr/)


- [tidyr](https://r4ds.had.co.nz/tidy-data.html)

---


## R and R Studio

![var](http://gannet.fish.washington.edu/seashell/snaps/Introduction_to_R__Data_Science_for_SAFS_2018-11-06_10-22-44.png)

---


## R and R Studio

![projects](http://gannet.fish.washington.edu/seashell/snaps/Screen_Capture_on_2018-11-06_at_10-26-25.gif)


---


![vectors](http://gannet.fish.washington.edu/seashell/snaps/Data_Structures__Data_Science_for_SAFS_2018-11-06_10-28-42.png)

---

![dataframes](http://gannet.fish.washington.edu/seashell/snaps/Data_Structures__Data_Science_for_SAFS_2018-11-06_10-29-41.png)

---


![d](http://gannet.fish.washington.edu/seashell/snaps/Data_Structures__Data_Science_for_SAFS_2018-11-06_10-30-30.png)


---

## dplyr

---

![basic](http://gannet.fish.washington.edu/seashell/snaps/Working_with_Tabular_Data__Data_Science_for_SAFS_2018-11-06_11-40-09.png)


---

![agg](http://gannet.fish.washington.edu/seashell/snaps/Working_with_Tabular_Data__Data_Science_for_SAFS_2018-11-06_11-41-02.png)

---

![joins](http://gannet.fish.washington.edu/seashell/snaps/Working_with_Tabular_Data__Data_Science_for_SAFS_2018-11-06_11-41-43.png)

---


![pipes](http://gannet.fish.washington.edu/seashell/snaps/Working_with_Tabular_Data__Data_Science_for_SAFS_2018-11-06_11-43-21.png)

---

## ggplot

---

## Project structure

![pro](http://gannet.fish.washington.edu/seashell/snaps/Project_Structure__Data_Science_for_SAFS_2018-11-06_11-58-11.png)


---



![rm](http://gannet.fish.washington.edu/seashell/snaps/Project_Structure__Data_Science_for_SAFS_2018-11-06_11-59-21.png)




---

![more](http://gannet.fish.washington.edu/seashell/snaps/Project_Structure__Data_Science_for_SAFS_2018-11-06_12-00-00.png)

---

![str](http://gannet.fish.washington.edu/seashell/snaps/Project_Structure__Data_Science_for_SAFS_2018-11-06_12-00-31.png)

---

## Version control

---

## knitr / R Markdown


---

## tidyr

![data](http://gannet.fish.washington.edu/seashell/snaps/R_for_Data_Science_2018-11-06_12-03-54.png)


---

![cheat](http://gannet.fish.washington.edu/seashell/snaps/data-wrangling-cheatsheet_2018-11-06_12-05-43.png)

https://www.rstudio.com/wp-content/uploads/2015/02/data-wrangling-cheatsheet.pdf
---


## scripting : find & xargs

```
%%bash
find /Volumes/Serine/wd/18-04-27/zr2096_*R1* \
| xargs basename -s _s1_R1_val_1.fq.gz | xargs -I{} /Applications/bioinfo/Bismark_v0.19.0/bismark \
--path_to_bowtie /Applications/bioinfo/bowtie2-2.3.4.1-macos-x86_64 \
--genome /Volumes/Serine/wd/18-03-15/genome \
--score_min L,0,-1.2 \
-p 4 \
--non_directional \
-1 /Volumes/Serine/wd/18-04-27/{}_s1_R1_val_1.fq.gz \
-2 /Volumes/Serine/wd/18-04-27/{}_s1_R2_val_2.fq.gz \
2> bismark.err
```
---
