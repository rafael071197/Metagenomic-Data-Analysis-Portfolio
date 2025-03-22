# **Prokaryotic Evolutionary Dynamics in a SoCal Coastal Marine Ecosystem (January 2025 - June 2025)**

This project aims to investigate the evolutionary dynamics of prokaryotes in the coastal marine ecosystem of Southern California through various metagenomic and bioinformatic steps. The following steps outline the pipeline used for data generation, analysis, and variant identification.

---

### **Pipeline Overview:**

- [**Step 1: SPAdes-Based Metagenome Assembly Pipeline**](https://www.notion.so/Step-1-SPAdes-Based-Metagenome-Assembly-Pipeline-1bdc2e3c80168085a8a6d2603c1eddae?pvs=21)  
  Begin with assembling metagenomes using SPAdes, which provides high-quality assemblies for downstream analyses.

- [**Step 2: Merging All Assembled Contigs**](https://www.notion.so/Step-2-Merging-All-Assembled-Contigs-1bdc2e3c80168005a54eff2360b63b90?pvs=21)  
  After assembly, merge all contigs into a unified file for further processing and analysis.

- [**Step 3: Filtering Contigs by Length**](https://www.notion.so/Step-3-Filtering-Contigs-by-Length-1bdc2e3c801680068619fcd969f152b5?pvs=21)  
  Filter out contigs that do not meet the required length criteria, ensuring that only the most relevant contigs are included.

- [**Step 4: Coassembling Contigs with MEGAHIT**](https://www.notion.so/Step-4-Coassembling-Contigs-with-MEGAHIT-1bdc2e3c801680c2a80ce0581c5b24cb?pvs=21)  
  Perform co-assembly of contigs using MEGAHIT to improve the assembly by utilizing multiple datasets.

- [**Step 5: Read Mapping with BWA**](https://www.notion.so/Step-5-Read-Mapping-with-BWA-1bdc2e3c801680329526c693163fbf2d?pvs=21)  
  Map sequencing reads to the assembled contigs using BWA to determine the alignment of each read to the reference.

- [**Step 6: Variant Calling with bcftools**](https://www.notion.so/Step-6-Variant-Calling-with-bcftools-1bdc2e3c801680debc3cf0992991a7e1?pvs=21)  
  Call genetic variants using bcftools based on the mapped reads, identifying SNPs, indels, and other variants across the metagenomes.

- [**Step 7: Variant Optimization with MAPQ Filtering and Depth Coverage Filtering**](https://www.notion.so/Step-7-Variant-Optimization-with-MAPQ-Filtering-and-Depth-Coverage-Filtering-1bdc2e3c801680f58886ef79bfa61a7b?pvs=21)  
  Filter the variants based on MAPQ scores and depth coverage, ensuring high-quality variant calls for downstream analysis.

- [**Step 8: Variant Count per Contig**](https://www.notion.so/Step-8-Variant-Count-per-Contig-1bdc2e3c801680e3a24fc6838839e6f4?pvs=21)  
  Count the number of variants identified in each contig, which helps to quantify the genetic variation in the dataset.

- [**Step 9: Merging Variants Across Multiple CSV Files**](https://www.notion.so/Step-9-Merging-Variants-Across-Multiple-CSV-Files-1bdc2e3c8016804bbca2fcdf7a2397bc?pvs=21)  
  Merge variant data from different CSV files, ensuring the integration of all relevant variant information for each sample.

- [**Step 10: VCF Processing and Variant Extraction by Contig**](https://www.notion.so/Step-10-VCF-Processing-and-Variant-Extraction-by-Contig-1bdc2e3c801680db8f0dec7a79a3fca6?pvs=21)  
  Process VCF files and extract variants by contig, creating separate VCF files for each contig across multiple metagenome samples.

- [**Step 11: Common Variants Between a Reference Metagenome and Multiple Comparisons**](https://www.notion.so/Step-11-Common-Variants-Between-a-Reference-Metagenome-and-Multiple-Comparisons-1bec2e3c80168051b27af3f7165fe8d1?pvs=21)  
  Compare variants in a reference metagenome (SRR18278886) to variants in other metagenomes, identifying common variants across all samples.
