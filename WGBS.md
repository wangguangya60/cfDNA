WGBS

### What is methylation

- [ ] most common is 5mC

- [ ] affects 70-80% of CpGs in human genome

- [ ] high levels of 5mC in CpG-rich promotors is strongly associated with repression

- [ ] in CpG-poor regions, relationship is more complex

### tips

- [ ] Directional library and un-directional library

  https://www.biostars.org/p/15938/

### Software

- [ ] bismark

bismark以bowtie为基础。如下图所示，将所有参考基因组和read上的C变成T（另一条链G变成A），再来做比对，因为所有序列只剩下3个碱基故名“three letter”。

- [ ] bsmap

bsmap则以SOAP算法为基础。它不转换基因组序列，而是允许序列中的C和T比对到基因组上的C，但是C不能比对到T（如图示）。另外通过HASH table seeding的方法也使比对过程更快速。

- [ ] methypipe

与bismark类似，以SOAP算法为基础，搭配BSviewer 做可视化

### Analysis

- [ ] methylation level

- [ ] mC density

- [ ] CpG in different region (chrosome, gene body, promotors)

- [ ] DMRs

### Description of methylation

DNA methylation represents an annotation system for marking the genetic text, thus providing instruction as to how and when to read the information and control transcription. Unlike sequence information, which is inherited, methylation patterns are established in a programmed process that continues throughout development, thus setting up stable gene expression profiles. This DNA methylation paradigm is a key player in medicine. Some changes in methylation closely correlate with age providing a marker for biological ageing, and these same sites could also play a part in cancer. The genome continues to undergo programmed variation in methylation after birth in response to environmental inputs, serving as a memory device that could affect ageing and predisposition to various metabolic, autoimmune, and neurological diseases. Taking advantage of tissue-specific differences, methylation can be used to detect cell death and thereby monitor many common diseases with a simple cell-free circulating-DNA blood test.



### Questions

- [x] most of the cfDNA molecules in plasma originated from the hematopoietic system 
- [x] The difference between cells in different development stage; The difference between cell from human A and human B at the same development stage. Which one is more significant?  
- [x] Basic role of DNA methylation is to restrict accessibility. Although this role usually serves to inhibit the activity of transcription factors, in some instances it could serve to prevent the binding of repressors, thus, in effect, causing gene activation.
- [x] Methylation patterns derived from the gametes are erased before implantation of the embryo and a new profile of methylation is established. ---- Reprogramming
- [ ] during implantation, the entire genome become methylated apart from CpG islands that are recognized and protected from methylation. Some house-keeping like genes.
- [ ] How to detect absolute ctDNA levels from cfDNA. ddPCR ? 

This diagram shows how basal methylation is preserved after DNA replication

![](C:\Users\wangguangya\Desktop\WGBS\reprogramming.jpg)

- [x] Rather than being a strictly dynamic mechanism for regulating gene expression, DNA methylation states can serve as a long ­term memory of previous gene expression decisions that were mediated by transcriptional factors that might no longer be present in the cell

- [x] Aging

Some changes occur in all tissues, gen­erating a distinct pattern that increases in magnitude as a function of ageing. Indeed, by mea­suring the methylation status of a small fraction of these sites in blood cells, it is possible to derive an index value that quite accurately reflects the age of the individual.

- [x] The difference between NGS and ddPCR

NGS to carry out a wide screening of the possible circulating mutations associated with the tumor

the ddPCR used for the identification of specific tumor mutations.

- [ ] Usage of cfDNA

  analysis of ctDNA and liquid biopsy samples obtained during the treatment may give important information capable of monitoring the prognosis of patients, as well as identifying specific therapeutic protocols pursuing the principles of personalized medicine

- [ ] Key words

hematopoietic 血液的； epithelial 上皮的；TFBS 转录binding site； TSS 转录起始位点

CTCF 转录阻抑物，也被称为11锌指蛋白或CCCTC结合因子

- [ ] TFBSs within open chromtain

the presence of transcription factors (TFs) bound to the DNA prevents the enzyme from cleavage in an otherwise nucleosome-free region. This leaves small regions, referred to as footprints, where read coverage suddenly drops within peak regions of high coverage.

- [ ] Gene Expression Omnibus (GEO) 

accession GSE71378 

## Scripts for the study "Cell-free DNA Comprises an In Vivo Nucleosome Footprint that Informs Its Tissues-Of-Origin"

http://shendurelab.github.io/cfDNA/

- [ ] Resources

- [ ] Demo data

https://www.ebi.ac.uk/ena/data/view/PRJNA471637

https://www.ebi.ac.uk/ena/data/view/SRR2130005&display=html

https://www.ncbi.nlm.nih.gov/Traces/study/?acc=PRJNA471637&o=acc_s%3Aa

https://www.ncbi.nlm.nih.gov/Traces/study/?acc=PRJNA291063&o=avgspotlen_l%3Ad



## Key words

apoptosis  /   necrosis

circulating cell-free DNA /  tumor-derived cfDNA 

tumour-associated molecular characteristics

non-invasive prenatal testing (NIPT)  /  foetal chromosomal aneuploidies  /  foetally derived DNA 

plasma/serum

single nucleotide variation /  copy number aberration  /  methylomic change / gene expression change

amplicon-sequencing / capture sequencing /  UMI to overcome errors from PCR

- [ ] bisulfite sequencing

Plasma DNA consists of DNA molecules originating from different tissues/organs during cell death and apoptosis 

cfDNA methylome is compared to the methylation profiles of different tissues and the contributions of individual tissues to cfDNA can be deduced 

peak fragment size frequency at 166 bp, reminiscent of a chromatosomal structure (approximately 146 bp nucleosome approximately 20 bp linker), and a 10-bp periodicity in the **descending size range** (为什么只在峰的左侧存在波动，caused by nicks around nucleosome)



## Chromtain Degradation

- [ ] DNase I preferentially degrades protease-treated degenerated chromatin or naked DNA and **does not cleave intact chromatin**, DNase I and proteases probably further divide the nucleosome units into smaller cfDNA pieces 

- [ ] in necrosis, DNase1L3 was essential, DNase1L3 may also function in DNA fragmentation of nucleosomal units

- [ ] CAD-mediated apoptotic DNA degradation is mainly cell-autonomous DNA degradation, but **not required** for normal animal development, as other process can back up. DNA fragmentation in cell are not required for apoptosis. *but important for second apoptosis (after having been engulfed by phagocytes) and necrosis*.

- [ ] in apoptosis, activity of degrading chromatin to mononucleosomes:  **CAD <  DNase1L3** ; CAD was insufficient for degrading chromatin and required DNase1L3 to degrade it into mononucleosomes

- [ ] CAD cleaved chromatin but with low efficiency and resulted in multiple sizes of DNA fragments. However, DNase1L3 efficiently cleaved chromatin to mononucleosomal size 

- [ ] **Localization:**  CAD in cytoplasm and nuclei ;  DNase1L3 and DNase I are secreted proteins and exist in
  blood circulation.
  
- [ ] **DNase1** is expressed by nonhematopoietic tissues and preferentially cleaves protein-free DNA 

- [ ] **DNase1L3** is mainly secreted by immune cells such as macrophages and targets DNA-protein complexes, such as nucleosomes

- [ ] Both hepatocyte necrosis and apoptosis **induced** DNase1L3 and DNase I activities in sera  

- [ ] inflammation 

- [ ] The serum DNase I activity correlates with the development of autoimmune diseases such as systemic lupus erythematosus (SLE) 

- [ ] Dnase1L3-deficient mice develop anti-DNA IgG antibodies and progressive systemic lupus erythematosus (SLE)-like disease, and the short fragment cfDNA increase. when immune response was restricted, the level of short cfDNA drop. So the short fragment is induced by immune response

- [ ] Both DNase I and DNase c may serve to prevent the onset of SLE-like diseases by degrading dead cell chromatin

- [ ] **Do the short fragments tend to be mapped to some specific regions, like open chromatins, TFBS ? And are there some specific motifs at the end of short fragments?**

- [ ] The **10-bp periodicity** of plasma DNA length, which is frequently more pronounced in ctDNA than in normal cfDNA

  

## Tumor derived cfDNA fraction detection 

CancerDetector

ichorCNA (no normal sample needed)

https://github.com/broadinstitute/ichorCNA

mFast-SeqS

## WGS library construction (single strand / double strand)

- [ ] fetal-derived and tumor-derived cfDNA is comparatively shorter than maternal cfDNA
- [ ] Would single-stranded library purify fetal-derived and tumor-derived cfDNA ? 

- [ ] single-stranded library can enrich short fragments but the ratio of fetal-derived and tumor-derived molecules do not increase

Why do single-stranded cfDNA molecules exist ?  What kind of enzyme?

Do these cfDNA preferably map to specific regions?

Do these cfDNA ends has motifs different from double-stranded molecules?

Is the distribution of short and long fragments different, short tend to be in specific regions, and long tend to be other regions?

**What cause the 10bp periodicity ?**  

The nucleosome is a histone DNA complex that folds **147** basepair of DNA into 1.7 turns of a left-handed superhelix, helical periodicity (wavelength) is 10.4bp. so the enzyme cutting sites are those bases away from histones in a helix;    linker DNA: 20 ~ 60bp. 