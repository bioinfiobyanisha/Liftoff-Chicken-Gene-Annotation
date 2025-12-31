# 🧬 Liftoff-Chicken-Gene-Annotation

Gene annotation transfer from **Red Jungle Fowl** to **White Leghorn** chicken using **Liftoff**, performed at **chromosome-level** (Chromosome 1 / partial region).

---

## 📌 Project Overview

This project demonstrates a **step-by-step Liftoff workflow** to transfer gene annotations from a well-annotated reference genome (**Red Jungle Fowl**) to a target genome (**White Leghorn**).  
Due to large genome size, the analysis is restricted to **chromosome 1 or a small genomic region**, as recommended for testing and learning purposes.

---

## 🎯 Objectives

- Use Red Jungle Fowl as the **reference genome**
- Use White Leghorn as the **target genome**
- Extract **chromosome 1 / partial region**
- Perform **gene annotation transfer using Liftoff**
- Generate annotated **GTF output** for the target genome

---

## 🧰 Tools & Software Used

- **Liftoff**
- **samtools**
- **Linux (Ubuntu / WSL)**
- **NCBI Genome Datasets**
- **GitHub**

---

## 📂 Data Used

### Reference Genome
- Species: *Gallus gallus* (Red Jungle Fowl)
- Assembly: `GCF_000002315.6 (GRCg6a)`
- Files:
  - Genomic FASTA (`.fna`)
  - Annotation file (`.gtf` / `.gff`)

### Target Genome
- Species: *Gallus gallus* (White Leghorn)
- Assembly: `GCA_024652995.1`
2️⃣ Extract chromosome 1 from reference genome
samtools faidx GCF_000002315.6_GRCg6a_genomic.fna NC_006088.5 > RJF_chr1.fa

3️⃣ Extract chromosome 1 annotation from GTF
grep "NC_006088.5" genomic.gtf > RJF_chr1.gtf

 4️⃣ Extract chromosome 1 from White Leghorn genome
samtools faidx GCA_024652995.1_ASM2465299v1_genomic.fna CM045249.1 > WL_chr1.fa

5️⃣ Run Liftoff
liftoff \
  WL_chr1.fa \
  RJF_chr1.fa \
  -g RJF_chr1.gtf \
  -o WL_liftoff_chr1.gtf


📤 Output Files
	•	WL_liftoff_chr1.gtf → Liftoff-annotated genes on White Leghorn chromosome 1
	•	Log files showing mapping statistics and feature transfer



✅ Results
	•	Successful transfer of gene annotations from reference to target genome
	•	Chromosome-level annotation achieved
	•	Workflow validated on a reduced genomic region



📚 Conclusion

This project demonstrates the practical use of Liftoff for comparative genomics and gene annotation transfer between closely related species/breeds.
The workflow can be extended to whole genome annotation with sufficient computational resources.



👩‍🔬 Author

Anisha Vishwakarma
MSc Biotechnology | Bioinformatics Enthusiast
GitHub: https://github.com/bioinfiobyanisha
