# Sex_Dosage_Sarcophilus_harrisii

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

<img width="1000" height="580" alt="chromosome_depth" src="https://github.com/user-attachments/assets/aee84c78-53d1-4f35-9e48-36d255c13241" />

Figure 8. The bar graph shows the relative sequencing depth of the six autosomes and two sex chromosomes (X and Y) of Sarcophilus harrisii. The six autosomal chromosomes (NC_045426.1–NC_045431.1) exhibit relatively consistent sequencing depth, with values close to 1.0, indicating that they have coverage comparable to the median autosomal depth. In contrast, the X chromosome (NC_045432.1) and Y chromosome (NC_045433.1) show noticeably lower relative depths of approximately 0.55 each. This means that both sex chromosomes have around 55% of the median autosomal coverage. The difference in bar heights suggests a reduced sequencing depth in the sex chromosomes compared with the autosomes, supporting an XY-like dosage pattern in the sample.

# PART E. Interpret your results

<img width="1598" height="863" alt="image" src="https://github.com/user-attachments/assets/7f08911d-a44c-4842-90ec-742f139bf294" />

Figure 10. NCBI BioSample record for the WGS sample of Sarcophilus harrisii (Tasmanian devil).

The figure presents the NCBI BioSample information associated with the whole-genome sequencing sample used in the sex-chromosome dosage analysis. It provides important sample metadata, including the organism, sample identifier, and recorded biological sex, if available. This information is important for comparing the sequencing-depth results with the reported sex of the sequenced individual. The metadata can help determine whether the XY-like dosage interpretation, based on the X:A ratio of 0.554 and Y:A ratio of 0.549, agrees with the recorded biological sex.

# QUESTIONS FOR THE REPORT

# Sex-Chromosome Inference in the Tasmanian Devil (*Sarcophilus harrisii*)

## 1. Species Selection and Evidence for the Sex-Determination System

The selected species is the Tasmanian devil (*Sarcophilus harrisii*), a marsupial mammal with a diploid XX/XY sex-determination system. Females possess two X chromosomes (XX), whereas males possess one X chromosome and one Y chromosome (XY).

Evidence supporting this system comes from the documented karyotype of the species, which has a diploid chromosome number of **2n = 14**, consisting of six pairs of autosomes and one pair of sex chromosomes.

The reference genome assembly **mSarHar1.11 (GCF_902635505.1)** provides the genomic sequences used to identify the autosomes and sex chromosomes for the sequencing-depth analysis.

## 2. Genome Assembly, WGS Run, and BioSample Information

The reference genome assembly used in this analysis is **mSarHar1.11 (GCF_902635505.1)**. Its associated assembly BioSample accession is **SAMEA6099886**.

However, the whole-genome sequencing (WGS) run accession and its corresponding BioSample accession have not yet been established from the available coverage and inference files.

| Information | Accession / Status |
|---|---|
| Species | *Sarcophilus harrisii* |
| Assembly name | mSarHar1.11 |
| Assembly accession | GCF_902635505.1 |
| Assembly BioSample | SAMEA6099886 |
| WGS run accession | Not yet established |
| WGS BioSample | Not yet established |
| Donor identity comparison | Undetermined |

The assembly BioSample and WGS BioSample must be compared to determine whether the reference genome and sequencing data originated from the same individual. Therefore, donor identity cannot currently be confirmed.

## 3. Chromosome Classification and Sequence Identification

Eight chromosome sequences were selected from the NCBI reference genome assembly for the sequencing-depth analysis. Six sequences represent the autosomes, while the remaining two represent the X and Y chromosomes.

The chromosome classification is summarized below.

| Chromosome Group | NCBI Accession | Classification |
|---|---|---|
| A1 | NC_045426.1 | Autosomal |
| A2 | NC_045427.1 | Autosomal |
| A3 | NC_045428.1 | Autosomal |
| A4 | NC_045429.1 | Autosomal |
| A5 | NC_045430.1 | Autosomal |
| A6 | NC_045431.1 | Autosomal |
| X | NC_045432.1 | X chromosome |
| Y | NC_045433.1 | Y chromosome |

The chromosome identities were verified using their corresponding assignments in the NCBI reference genome assembly **GCF_902635505.1**.

The six autosomal sequences were assigned to group A, while the X and Y chromosome sequences were classified separately. Mitochondrial DNA and unplaced scaffolds were excluded because they do not belong to the autosomal or sex-chromosome groups evaluated in this analysis.

The original chromosome accession names were retained to maintain consistency between the chromosome classification and sequencing-depth analysis.

## 4. Sequencing-Depth Results and Inferred Sex-Chromosome Complement

The median autosomal sequencing depth was calculated as **42.675×**. The relative sequencing depths of the X and Y chromosomes were evaluated by comparing their coverage against the median autosomal depth.

### Sequencing-Depth Summary

| Measurement | Result |
|---|---:|
| Median autosomal depth | 42.675× |
| X:A ratio | 0.554 |
| Y:A ratio | 0.549 |
| Inferred sex-chromosome complement | XY-like |

Both sex chromosomes exhibited approximately 55% of the median autosomal sequencing depth.

These results indicate reduced coverage relative to the autosomes, consistent with the expected dosage pattern of a male XY individual. The analysis script consequently classified the sample as **XY-like**.

However, sequencing-depth analysis alone cannot definitively establish the biological sex of the individual. The observed ratios provide evidence supporting an XY-like sex-chromosome complement rather than a confirmed biological-sex identification.

## 5. Comparison with the Recorded Sex of the WGS Donor

The sequencing-depth analysis produced an XY-like interpretation, supported by the X:A ratio of 0.554 and Y:A ratio of 0.549. These values are consistent with the expected chromosome dosage pattern of a male Tasmanian devil.

However, the recorded biological sex of the WGS donor has not yet been verified because the corresponding WGS BioSample information is unavailable in the supplied data. Therefore, a direct comparison between the inferred chromosome complement and the recorded sex cannot currently be established.

Several technical factors may also influence the observed sequencing-depth ratios, including:

- Sequencing-depth variation.
- Read-mapping bias.
- Repetitive genomic regions.
- Differences between the reference assembly and the sequenced individual.

Consequently, the result provides evidence supporting an XY-like chromosome complement, but it should be interpreted alongside the WGS BioSample metadata and other available biological information.

## 6. Why a Chromosome-Level Assembly Alone Is Insufficient for Reliable Read-Depth Sex Inference

A chromosome-level genome assembly provides information about chromosome organization, sequence identity, and chromosome structure. However, it does not directly reveal the number of chromosome copies present in a particular individual.

To infer sex-chromosome dosage, sequencing reads obtained from the biological sample must first be mapped against the reference genome. The resulting sequencing depth is then compared between the autosomes and sex chromosomes to determine their relative coverage.

Without sequencing reads, an X:A or Z:A ratio cannot be calculated because chromosome sequences and their lengths alone do not provide information about the actual sequencing coverage of an individual.

Furthermore, the reference assembly and sequencing sample may originate from different individuals. This makes it important to consider sample-specific biological differences when interpreting the results.

Therefore, a chromosome-level assembly serves as the reference for the analysis, while the sequencing data provide the evidence needed to infer the sex-chromosome complement.

---

## Overall Conclusion

The sequencing-depth analysis of *Sarcophilus harrisii* produced an XY-like sex-chromosome inference. The median autosomal sequencing depth was 42.675×, with an X:A ratio of 0.554 and a Y:A ratio of 0.549. These values indicate that both sex chromosomes exhibited approximately 55% of the median autosomal coverage, supporting an XY-like chromosome complement.

Nevertheless, the inference remains provisional because the WGS BioSample accession and recorded donor sex have not yet been verified. Confirming the relationship between the reference assembly and sequencing sample, together with examining the associated BioSample metadata, is necessary for a more reliable interpretation.

## References and Data Sources

- **NCBI Assembly:** GCF_902635505.1 — mSarHar1.11
- **Assembly BioSample:** SAMEA6099886
- **NCBI Reference Chromosomes:** NC_045426.1–NC_045433.1
- **Species:** *Sarcophilus harrisii* (Tasmanian devil)
