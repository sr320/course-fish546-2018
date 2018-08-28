class: center, middle

# FISH 546 
## Bioinformatics for Environmental Sciences

https://github.com/sr320/course-fish546-2016/wiki

##genefish.info

Steven Roberts
@sr320

---
class: center, middle
# Jupyter & Annotation
---
## New Format?
- General Announcements
- last class / week `fu`
- Instruction module 
- Work on projects
---
`issue # 16`


>I tried to make a file with Sublime 2 from the terminal using the CLI (command line interface) subl I was unsuccessful. I tried to make a symlink to subl using the instructions here but when I ran

`ln -s "/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl" ~/bin/subl`

>I just got a 'no such file or dir exists error'. I didn't try too hard though, so will make another attempt
---

>>tutorial was really mac based so it was a little difficult to get through on the windows operating system
---

class: center, middle

In *Jupyter* you need to add `!` before the command.

---
# Unix Review
last week reading

- Streams (not holding in memory)

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
## Instruction module

Blast

 
 