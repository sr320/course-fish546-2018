class: center, middle

# FISH 546 
## Bioinformatics for Environmental Sciences

https://github.com/sr320/course-fish546-2016/wiki

##genefish.info

Steven Roberts
@sr320

---

## Reminders

- We will not going through manuals 

- 



---

class: center, middle


# RNA-Seq


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

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Screenshot_10_24_16__8_12_AM_1DBE5C48.png" alt="Screenshot_10_24_16__8_12_AM_1DBE5C48.png"/>

### Example running DESeq2 

<https://github.com/sr320/eimd-sswd/blob/master/eimd_analysis.ipynb>



---
### @hputnam example

<https://github.com/hputnam/Montipora_Spawn_Timing/blob/master/notebooks/Mcap_Spawn_analysis_script.md> 

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Montipora_Spawn_Timing_Mcap_Spawn_analysis_script_md_at_master_·_hputnam_Montipora_Spawn_Timing_1DBEC543.png" alt="Montipora_Spawn_Timing_Mcap_Spawn_analysis_script_md_at_master_·_hputnam_Montipora_Spawn_Timing_1DBEC543.png"/>

---

# With Genome...

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/TopHat_1DBE5B6E.png" alt="TopHat_1DBE5B6E.png"/>


---

## Example

Within Cyverse
<https://github.com/sr320/course-fish546-2015/blob/master/notebooks/Sam_RNA-seq.ipynb>

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Screenshot_10_24_16__8_10_AM_1DBE5C07.png" alt="Screenshot_10_24_16__8_10_AM_1DBE5C07.png"/>


---

class: center, middle


# Understanding Meaning

---

class: center, middle

You have a list of _important_ genes. Now what?

---

class: center, middle

## Wait I still only have a bunch of Uniprot codes!!

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


class: center, middle

## I can see where I am going but how do I get there...

---

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/SQLShare_1DC23CC6.png" alt="SQLShare_1DC23CC6.png"/>

---

![upload](https://drops.azureedge.net/drops/files/acc_524195/tz8q?rscd=inline%3B%20filename%3DScreen%2520Capture%2520on%25202016-10-27%2520at%252006-50-14.gif&rsct=image%2Fgif&se=2016-10-27T14%3A20%3A29Z&sig=og3tX%2BjsmBvL7nL1QuQSgN5oYoi%2BRC57CfM12nmaMmM%3D&sp=r&sr=b&st=2016-10-27T13%3A20%3A29Z&sv=2013-08-15)

---
Could upload anything....

![rasta](https://drops.azureedge.net/drops/files/acc_524195/QgDs?rscd=inline%3B%20filename%3DScreen%2520Capture%2520on%25202016-10-27%2520at%252006-48-58.gif&rsct=image%2Fgif&se=2016-10-27T14%3A21%3A54Z&sig=dMyzNjr9gmZol9yPpialmpJsvg6HsRYKyoq2UoFqvD8%3D&sp=r&sr=b&st=2016-10-27T13%3A21%3A54Z&sv=2013-08-15)

---

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/SQLShare_-_View_Query_1DC23EA1.png" alt="SQLShare_-_View_Query_1DC23EA1.png"/>

---

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/SQLShare_-_View_Query_1DC23ED5.png" alt="SQLShare_-_View_Query_1DC23ED5.png"/>

---

![select](https://drops.azureedge.net/drops/files/acc_524195/ByyU?rscd=inline%3B%20filename%3DScreen%2520Capture%2520on%25202016-10-27%2520at%252006-57-35.gif&rsct=image%2Fgif&se=2016-10-27T14%3A28%3A02Z&sig=lxdDEbo2ozc3il8ZY%2Fl4EkMLfFzve2ltEh83H0mBa6c%3D&sp=r&sr=b&st=2016-10-27T13%3A28%3A02Z&sv=2013-08-15)

---

![join](https://drops.azureedge.net/drops/files/acc_524195/tDM4?rscd=inline%3B%20filename%3DScreen%2520Capture%2520on%25202016-10-27%2520at%252007-08-13.gif&rsct=image%2Fgif&se=2016-10-27T14%3A38%3A34Z&sig=I7j21BQywFSghMN%2F3sRq6BgA2Sb1Np3mHk9Vwol2Igk%3D&sp=r&sr=b&st=2016-10-27T13%3A38%3A34Z&sv=2013-08-15)

---

You can just paste...

```sql
SELECT * FROM [roberts.sbr@gmail.com].[Geoduck-tranv3-blastx_sprot_1.sorted]blast
  left join
  [roberts.sbr@gmail.com].[uniprot-all0916]uni
on
blast.Column3 = uni.Column1
```


---

## Imagine you could just get a short list?

---

<https://youtu.be/D2XjF2xqbF4>


<img src="http://eagle.fish.washington.edu/cnidarian/skitch/CICESE__blast-sqlshare-excel_-_YouTube_🔊_1DC242CC.png" alt="CICESE__blast-sqlshare-excel_-_YouTube_🔊_1DC242CC.png"/>


---

<https://www.youtube.com/watch?v=5pvl-RBq0_A>

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/CICESE__Steven_does_SQLShare_-_YouTube_🔊_1DC2438E.png" alt="CICESE__Steven_does_SQLShare_-_YouTube_🔊_1DC2438E.png"/>



---

Live Demo - No Way!

---





