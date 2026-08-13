# LegalTech SLM — Contract Understanding & Clause Analysis

> A domain-specific Small Language Model (SLM) for structured legal contract analysis, built with Qwen3-1.7B, LoRA fine-tuning, CUAD, and ContractNLI.

> Honest status: the first fine-tuning experiment has not started yet, and no production or accuracy claims are being made yet.

---

## Project Status

**Current stage: Pre-training**

The complete data preparation and training pipeline has been prepared and validated.

The first fine-tuning experiment has **not started yet**.

### Progress

- [x] LegalTech problem research
- [x] Defined target use case
- [x] Selected Qwen3-1.7B
- [x] Selected CUAD dataset
- [x] Selected ContractNLI dataset
- [x] Prepared CUAD training examples
- [x] Prepared ContractNLI training examples
- [x] Balanced the training mixture
- [x] Combined datasets
- [x] Validated training sequence lengths
- [x] Validated JSON outputs
- [x] Validated dataset structure
- [x] Prepared LoRA adapter
- [x] Configured SFTTrainer
- [x] Configured training arguments
- [ ] Baseline evaluation
- [ ] First fine-tuning run
- [ ] Fine-tuned model evaluation
- [ ] Error / failure analysis
- [ ] Model iteration
- [ ] Inference benchmarking
- [ ] Deployment
- [ ] Monitoring
- [ ] Production-style evaluation

---

# 1. Why This Project?

Legal professionals spend significant amounts of time reading contracts and searching for specific clauses.

A commercial contract may contain dozens or hundreds of pages, while the information a legal professional needs may be limited to a few important clauses.

Examples include:

- Effective Date
- Expiration Date
- Governing Law
- License Grant
- Termination
- Liability Cap
- Anti-Assignment
- Change of Control
- IP Ownership
- Exclusivity
- Renewal Terms

The goal of this project is to build a **small, specialized language model** that can perform focused legal contract understanding tasks rather than trying to become a general-purpose chatbot.

The project focuses on two complementary capabilities:

1. **Contract clause extraction**
2. **Contractual statement reasoning**

---

# 2. Core Idea

The project combines two legal NLP datasets with different objectives.

```text
                    Legal Contract
                          |
             +------------+------------+
             |                         |
             v                         v
       CUAD Extraction          ContractNLI
             |                         |
             v                         v
    Find important clauses       Understand claims
             |                         |
             +------------+------------+
                          |
                          v
                LegalTech SLM
                 Qwen3-1.7B
```
