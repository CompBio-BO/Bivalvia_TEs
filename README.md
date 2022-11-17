# Bivalvia_LINEs
Collection of manually curated LINE consensus sequences extracted from bivalve genomes

### Format:

```<SPECIES NAME>_<PROGRESSIVE NUMBER>_cons_<AUT|RVT>#<RepeatMasker classification> <LINE CLADE> <ALIGNMENT SIZE>```  
*e.g:* A.i.concentricus_9_cons_AUT#LINE/CR1-Zenon CR1 7

AUT=Consensus sequences with both Reverse Transcriptase (RVT) and Endonuclease domain (EN) (NB: They can be in different ORFs).  
RVT=Consensus sequences missing the EN domain.  
ALIGNMENT SIZE=Number of sequences used to generate the consensus sequences.  

Consensus sequences construction workflow:  
1. RepeatMasker annotation of TE using an automatically generated library (with RepeatModeler).  
2. Extension, Extraction and transaltion of all annotated insertions (min ORF length = 300 aa).  
3. Selection of all ORFs with a significant hmmscan hit (e-value < 0.05) against LINE-specific RVT HMM profiles.  
4. Clustering of all ORF nucleotide sequecens following the 80-80 rule.  
5. Identification of clusters with at least 5 members and one of them showing both RVT and EN domains on the same ORF.  
6. Back blastn of each rapresentative sequence against the genome (min 70% identity and coverage), extension and extraction of all hits.  
7. Consensus construction using EMBOSS cons (plurality of 3) and manual validation and curation.  


Species and accession/source of genome assembly:
