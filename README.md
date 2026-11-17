<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/46107644-b439-494c-8845-159a091b42b5" /># Sex_Dosage_Sarcophilus_harrisii

## Part A. Choose and Register Your Animal

| Field | Value |
|---|---|
| **Full Name** | FRANCIS KYLE A. OFICIAR |
| **Section** | B |
| **Animal Species** | *Sarcophilus harrisii* (Tasmanian devil) |
| **Assembly Accession** | GCF_902635505.1 |
| **Assembly Name** | mSarHar1.11 |
| **Assembly BioSample** | SAMEA6099886 |
| **Sex System (XY/ZW)** | XY |
| **WGS Run Accession** | Not yet verified |
| **WGS BioSample** | Not yet verified |
| **Same Donor?** | Not yet verified |
| **NCBI Genome Link** | [NCBI Genome](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_902635505.1/) |


# PART B. Retrieve data and map reads in Galaxy

<img width="1182" height="766" alt="image" src="https://github.com/user-attachments/assets/072bb63b-2358-48bc-bee7-0d04221fb096" />

**Figure 1.**

<img width="1600" height="779" alt="image" src="https://github.com/user-attachments/assets/208545b3-d999-425a-8657-ff65483e8af0" />

**Figure 2.** Reverse-read

<img width="1599" height="776" alt="image" src="https://github.com/user-attachments/assets/f6718786-2d58-4c56-a6d8-c448037dae01" />

**Figure 3.** Forward-read

<img width="1600" height="790" alt="image" src="https://github.com/user-attachments/assets/6bd39191-252b-441e-845c-e851fa47afe7" />

**Figure 4.** BWA-MEM2

<img width="1600" height="814" alt="image" src="https://github.com/user-attachments/assets/06949477-7899-4364-a1c1-37f88ffa1791" />

**Figure 5.** SAMtools

# PART C.

<img width="129" height="181" alt="image" src="https://github.com/user-attachments/assets/62e15032-c20c-4d69-bc06-4547b1e97a3d" />

The chromosome groups were selected based on the chromosome assignments provided in the NCBI reference genome assembly GCF_902635505.1 (mSarHar1.11) and the reference sequence names listed in the chromosome_coverage.tsv file. The six autosomes, represented by NC_045426.1 to NC_045431.1, were assigned to group A because they correspond to the identified non-sex chromosomes of the Tasmanian devil (Sarcophilus harrisii). Meanwhile, NC_045432.1 was assigned to group X because it represents the X chromosome, while NC_045433.1 was assigned to group Y because it represents the Y chromosome. This classification follows the XY sex-determination system of the species. Mitochondrial DNA and unplaced scaffolds were excluded because they do not belong to the identified autosomal or sex-chromosome groups. By using the exact reference sequence names, the classification also ensures consistency with the chromosome coverage data used in the analysis.

# Part D. Run the R analysis

<img width="1116" height="265" alt="image" src="https://github.com/user-attachments/assets/f76e496c-7a76-49a4-bd69-0de211a99281" />

Figure 6. Project folder for the R analysis in Part D. The *Sarcophilus harrisii*  folder holds the Galaxy output chromosome_coverage.tsv, the chromosome labels chromosome_groups.csv, the script sex_depth_analysis.R, and the results folder the script created.

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/2780e4b2-2b81-432c-b635-dedccfcef1ba" />

Figure 7. Autosomal and sex-chromosome depth analysis of Sarcophilus harrisii (Tasmanian devil).

R analysis of sex-chromosome dosage using sex_depth_analysis.R, chromosome_coverage.tsv, and chromosome_groups.csv based on the NCBI reference genome assembly GCF_902635505.1 (mSarHar1.11). The median autosomal depth was 42.675×. The X chromosome (NC_045432.1) had an X/A ratio of 0.554, while the Y chromosome (NC_045433.1) had a Y/A ratio of 0.549. Both sex chromosomes showed approximately 55% of the median autosomal sequencing depth, resulting in an XY-like dosage interpretation. This pattern supports the presence of an XY chromosome complement in the sequenced sample. However, sequencing depth alone cannot definitively establish biological sex because coverage variation, read-mapping biases, chromosome assembly quality, and differences between the genome assembly donor and WGS sample donor may influence the results. Therefore, the inferred result should also be compared with the sex information recorded in the WGS BioSample.

