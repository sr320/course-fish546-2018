class: center, middle

# FISH 546
## Bioinformatics for Environmental Sciences

https://github.com/sr320/course-fish546-2018/wiki

Week 2

Steven Roberts
@sr320

---
class: center, middle

this week
# Jupyter & Annotation

---

class: center, middle

In *Jupyter* you need to add `!` before the command.

---
# Unix Review
last week reading / activity

- What do you think about `bash`?

--

- Redirecting Standard Out to File     
`cat tb1-protein.fasta tga1-protein.fasta > zea-proteins.fasta`

--

- Redirecting Standard Error    
`ls -l tb1.fasta leafy1.fasta > listing.txt 2> listing.stderr`

--


- Pipes    
```
grep -v "^>" tb1.fasta | \
grep --color -i "[^ATCG]"
    CCCCAAAGACGGACCAATCCAGCAGCTTCTACTGCTAYCCATGCTCCCCTCCCTTCGCCGCCGCCGACGC
```    


---


## Project Documentation

-  Document your methods and workflows

--

- Document the origin of all data in your project directory

--

- Document when you downloaded data

--

- Record data version information

--

- Describe how you downloaded the data

--

- Document the versions of the software that you ran


---

class: center, middle

#Read

---
## Common Bioinformatics Program

Blast
