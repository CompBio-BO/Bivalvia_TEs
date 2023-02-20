# Bivalvia TEs
Collection of manually curated LINEs, SINEs and DDE/D-related consensus sequences extracted from bivalve genomes.

### Format:

```<TE CLASS/SUPERFAMILY>_<SPECIES NAME>_<PROGRESSIVE NUMBER>_cons#<RepeatMasker classification>```  
*e.g:* LINE_A.i.concentricus_9_cons#LINE/CR1-Zenon

### Consensus sequences construction workflow:  
1. RepeatMasker annotation of TE using an automatically generated library (with RepeatModeler).  
2. Extension, Extraction and transaltion of all annotated insertions (min ORF length = 300 aa).  
3. Selection of all ORFs with a significant hmmscan hit (e-value < 0.05) against LINE-specific RVT HMM profiles or against DDE/D-related HMM profiles (specific for each DDE/D superfamily, as described in [Yuan and Wessler, (2011](https://www.pnas.org/doi/10.1073/pnas.1104208108))).  
4. Clustering of all ORF nucleotide sequecens following the 80-80 rule (CD-HIT).  
5. Identification of clusters with at least 5 members (for LINEs we also required that at least one sequence posses both RVT and EN domains on the same ORF) 
6. Back blastn of each rapresentative sequence against the genome (min 70% identity and coverage), extension and extraction of all hits.  
7. Consensus construction using EMBOSS *cons* (plurality of 3) followed by manual curation and validation.  
8. Merging all libraries and reduce redundancy (CD-HIT; 80-80 rule)


### Accession numbers/sources of genome assemblies:  

- *Potamilus streckersoni*  GCA_016746295.1  
- *Megalonaias nervosa* GCA_016617855.1  
- *Solen grandis*  GCA_021229015.1  
- *Sinonovacula constricta*  GCA_007844125.1  
- *Dreissena rostriformis* https://phaidra.univie.ac.at/view/o:980132  
- *Archivesica marissinica*  GCA_014843695.1  
- *Cyclina sinensis* GCA_012932295.1  
- *Mercenaria mercenaria*  GCA_014805675.1  
- *Ruditapes philippinarum* 
- *Anadara kagoshimensis* GCA_021292105.1  
- *Scapharca broughtonii* http://dx.doi.org/10.5524/100607  
- *Tegillarca granosa*  GCA_013375625.1  
- *Myzuhopecten yessoensis*  GCF_002113885.1  
- *Chlamys farreri* http://mgbase.qnlm.ac/home  
- *Pecten maximus*  GCF_902652985.1  
- *Argopecten irradians concentricus*  https://datadryad.org/stash/dataset/doi:10.5061/dryad.hdr7sqvdr  
- *Argopecten purpuratus* http://mgbase.qnlm.ac/home  
- *Pinctada fucata* http://gigadb.org/dataset/100240  
- *Saccostrea glomerata* http://soft.bioinfo-minzhao.org/srog  
- *Crassostrea virginica*  GCF_002022765.2  
- *Crassostrea ariakensis* GCA_020567875.1  
- *Crassostrea gigas*  GCF_902806645.1  
- *Mytilus coruscus* GCA_017311375.1  
- *Mytilus edulis* GCA_019925275.1  
- *Limnoperna fortunei*  http://gigadb.org/dataset/100386  
- *Modiolus philippinarum* https://datadryad.org/stash/dataset/doi:10.5061/dryad.h9942  
- *Bathymodiolus platifrons* https://datadryad.org/stash/dataset/doi:10.5061/dryad.h9942  


