# Bivalvia TEs
Collection of manually curated LINEs, SINEs and DDE/D-related consensus sequences extracted from bivalve genomes.

### Format:

```<TE CLASS/SUPERFAMILY>_<SPECIES NAME>_<PROGRESSIVE NUMBER>_cons#<RepeatMasker classification>```  
*e.g:* LINE_A.i.concentricus_9_cons#LINE/CR1-Zenon

### Consensus sequences construction workflow (LINEs and DDE/D transposons):  
1. RepeatMasker annotation of TE using species-specific automatically generated library.  
2. Extension, Extraction and transaltion of all annotated insertions (min ORF length = 300 aa).  
3. Selection of all ORFs with a significant hmmscan hit (e-value < 0.05) against LINE-specific RVT HMM profiles or against DDE/D-related HMM profiles (specific for each DDE/D superfamily, as described in [Yuan and Wessler, (2011](https://www.pnas.org/doi/10.1073/pnas.1104208108))).  
4. Clustering of all ORF nucleotide sequecens following the 80-80 rule (CD-HIT).  
5. Identification of clusters with at least 5 members (for LINEs we also required that at least one sequence posses both RVT and EN domains on the same ORF) 
6. Back blastn of each rapresentative sequence against the genome (min 70% identity and coverage), extension and extraction of all hits.  
7. Consensus construction using EMBOSS *cons* (plurality of 3) followed by manual curation and validation.  
8. Merging all libraries and reduce redundancy (CD-HIT; 80-80 rule)

## Consensus sequences construction workflow (SINEs):  
For SINEs elements we selected 12 species for in-depth SINEs annotation using SINE_Scan. SINEs candidates resulting from RepeatModeler and SINE_Scan were merged and subjected to a "Blast-Extend-Extract" process to identify boundaries of the elements and confirm the presence of a 3' tRNA-related head, a conserved domain and a 5' tail.

### Accession numbers/sources of genome assemblies:  

- *Potamilus streckersoni*  GCA_016746295.1 (NCBI).  
- *Megalonaias nervosa* GCA_016617855.1 (NCBI).  
- *Solen grandis*  GCA_021229015.1 (NCBI).  
- *Sinonovacula constricta*  GCA_007844125.1 (NCBI).  
- *Dreissena rostriformis* https://phaidra.univie.ac.at/view/o:980132  
- *Archivesica marissinica*  GCA_014843695.1 (NCBI).  
- *Cyclina sinensis* GCA_012932295.1 (NCBI).  
- *Mercenaria mercenaria*  GCA_014805675.1  (NCBI).  
- *Ruditapes philippinarum* GCA_026571515.1 (NCBI).  
- *Anadara kagoshimensis* GCA_021292105.1 (NCBI).  
- *Scapharca broughtonii* http://dx.doi.org/10.5524/100607  
- *Tegillarca granosa*  GCA_013375625.1 (NCBI).  
- *Myzuhopecten yessoensis*  GCF_002113885.1 (NCBI).  
- *Chlamys farreri* http://mgbase.qnlm.ac/home  
- *Pecten maximus*  GCF_902652985.1 (NCBI).  
- *Argopecten irradians concentricus*  https://datadryad.org/stash/dataset/doi:10.5061/dryad.hdr7sqvdr  
- *Argopecten purpuratus* http://mgbase.qnlm.ac/home  
- *Pinctada fucata* http://gigadb.org/dataset/100240  
- *Saccostrea glomerata* http://soft.bioinfo-minzhao.org/srog  
- *Crassostrea virginica*  GCF_002022765.2 (NCBI).  
- *Crassostrea ariakensis* GCA_020567875.1 (NCBI).  
- *Crassostrea gigas*  GCF_902806645.1 (NCBI).  
- *Mytilus coruscus* GCA_017311375.1 (NCBI).  
- *Mytilus edulis* GCA_019925275.1 (NCBI).  
- *Limnoperna fortunei*  http://gigadb.org/dataset/100386  
- *Modiolus philippinarum* https://datadryad.org/stash/dataset/doi:10.5061/dryad.h9942  
- *Bathymodiolus platifrons* https://datadryad.org/stash/dataset/doi:10.5061/dryad.h9942  

**IMPORTANT**
The RepeatMasker formatted-style classification for DDE/D and SINEs was automatically generated using RepeatClassifier from the RepeatModeler package and can therefore be innacurate. If you have any correction to suggest please contact jacopo.martelossi2@unibo.it

