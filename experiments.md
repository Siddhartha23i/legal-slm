# Experiment #01

### Hypothesis

LoRA fine-tuning on CUAD + ContractNLI will improve
structured contract extraction and NLI performance.

### Configuration

- Model: Qwen3-1.7B
- LoRA rank: 16
- Learning rate: 2e-4
- Epochs: 1
- Effective batch size: 8
- Max sequence length: 4096

### Result

[results here]

### Observation

The model improved on clause extraction but struggled
with ContractNLI.

### Failure examples

[examples]

### Decision

Do not increase epochs yet.

Investigate class imbalance and task interference first.