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

-

---

class: center, middle


# R and xargs

Demo..


---


## Transcriptome Assembly

- All the genes (expressed)!

--

- Necessary for de novo (no genome) expression analysis

--

- Memory intensive

--

- Primary software - Trinity


---

## Trinity

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Home_·_trinityrnaseq_trinityrnaseq_Wiki_1DBE50A5.png" alt="Home_·_trinityrnaseq_trinityrnaseq_Wiki_1DBE50A5.png"/>


---


<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Accessing_Trinity_on_Publicly_Available_Compute_Resources_·_trinityrnaseq_trinityrnaseq_Wiki_1DBE5204.png" alt="Accessing_Trinity_on_Publicly_Available_Compute_Resources_·_trinityrnaseq_trinityrnaseq_Wiki_1DBE5204.png"/>

---

## Example code

```
Trinity.pl
--seqType fq
--JM 24G
--left /Volumes/web/cnidarian/Geo_Pool_F_GGCTAC_L006_R1_001_val_1.fq /Volumes/web/cnidarian/Geo_Pool_M_CTTGTA_L006_R1_001_val_1.fq
--right /Volumes/web/cnidarian/Geo_Pool_F_GGCTAC_L006_R2_001_val_2.fq /Volumes/web/cnidarian/Geo_Pool_M_CTTGTA_L006_R2_001_val_2.fq
--CPU 16
```

---

## Evaluating assembly

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Transrate_-_transcriptome_assembly_quality_analysis_1DBE53AF.png" alt="Transrate_-_transcriptome_assembly_quality_analysis_1DBE53AF.png"/>


---

## Overview

Transrate analyses a transcriptome assembly in three key ways:

--

- by inspecting the contig sequences

--

- by mapping reads to the contigs and inspecting the alignments

--

- by aligning the contigs against proteins or transcripts from a related species and inspecting the alignments

---

## Lots you can do "within Trinity"

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Trinity_Transcript_Quantification_·_trinityrnaseq_trinityrnaseq_Wiki_1DBE5496.png" alt="Trinity_Transcript_Quantification_·_trinityrnaseq_trinityrnaseq_Wiki_1DBE5496.png"/>


---

## Basic


### Get Counts - do stats



---

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Screenshot_10_24_16__8_19_AM_1DBE5DFC.png" alt="Screenshot_10_24_16__8_19_AM_1DBE5DFC.png"/>





---



# With Genome...

<img src="http://gannet.fish.washington.edu/seashell/snaps/HISAT_2018-10-21_13-50-45.png" alt="HISAT_2018"/>


---

## Hisat replaces Tophat

Within Cyverse
<https://github.com/sr320/course-fish546-2015/blob/master/notebooks/Sam_RNA-seq.ipynb>

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Screenshot_10_24_16__8_10_AM_1DBE5C07.png" alt="Screenshot_10_24_16__8_10_AM_1DBE5C07.png"/>

---
<img src="http://eagle.fish.washington.edu/cnidarian/skitch/eimd-sswd_eimd_analysis_ipynb_at_master_·_sr320_eimd-sswd_1DC23A83.png" alt="eimd-sswd_eimd_analysis_ipynb_at_master_·_sr320_eimd-sswd_1DC23A83.png"/>


---

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/001_1-Downloading-databases_1DC23B63.png" alt="001_1-Downloading-databases_1DC23B63.png"/>

---

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/001_1-Downloading-databases_1DC23B63.png" alt="001_1-Downloading-databases_1DC23B63.png"/>

---

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/001_1-Downloading-databases_1DC23B8E.png" alt="001_1-Downloading-databases_1DC23B8E.png"/>

---

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/001_1-Downloading-databases_1DC23BB7.png" alt="001_1-Downloading-databases_1DC23BB7.png"/>

---

### I want that!

```
http://www.uniprot.org/uniprot/?query=&fil=reviewed%3Ayes&columns=id%2Centry%20name%2Creviewed%2Cprotein%20names%2Cgenes%2Corganism%2Clength%2Cgo(biological%20process)%2Cgo-id%2Ccomment(PATHWAY)%2Cdatabase(UniPathway)%2Cdatabase(CDD)%2Cdatabase(Pfam)
```

---

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/001_1-Downloading-databases_1DC23BF1.png" alt="001_1-Downloading-databases_1DC23BF1.png"/>

---

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/001_1-Downloading-databases_1DC23C18.png" alt="001_1-Downloading-databases_1DC23C18.png"/>

---
