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
