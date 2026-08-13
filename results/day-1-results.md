# Day 1 Results — LegalTech SLM

**Date:** 2026-08-13  
**Model:** Qwen3-1.7B  
**Project:** LegalTech SLM — Contract Understanding & Clause Analysis  
**Status:** Pre-training complete

---

## Objective

Prepare and validate the complete training pipeline before starting the first
fine-tuning experiment.

The model combines two tasks:

- **CUAD** → Contract clause extraction
- **ContractNLI** → Contractual reasoning

The goal is to build a small legal-domain model capable of producing
structured JSON with relevant evidence.

---

## Dataset Preparation

### CUAD

Original CUAD dataset:

- 22,450 examples
- 408 contracts
- 41 clause categories
- 11,180 examples with answer spans
- 11,270 examples without answer spans

For the first experiment, 15 clause types were selected.

The V1 CUAD dataset contains:

| Split | Examples |
|---|---:|
| Train | 2,940 |
| Validation | 331 |
| Test | 353 |

### ContractNLI

ContractNLI contains:

| Split | Examples |
|---|---:|
| Train | 7,191 |
| Validation | 1,037 |
| Test | 2,091 |

The document splits were verified to prevent overlap:

```text
Train ∩ Validation: 0
Train ∩ Test: 0
Validation ∩ Test: 0
```