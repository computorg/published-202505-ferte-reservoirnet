# Precomputed Datasets

This directory contains precomputed datasets to avoid network download issues in CI environments.

## Japanese Vowels Datasets

- `japanese_vowels.rds`: Standard Japanese vowels dataset
- `japanese_vowels_repeat.rds`: Japanese vowels dataset with `repeat_targets=TRUE`

### Regenerating the datasets

If you need to regenerate these datasets, run:

```r
library(reservoirnet)

# Standard dataset
japanese_vowels <- generate_data(dataset = "japanese_vowels")[[1]]
saveRDS(japanese_vowels, "data/japanese_vowels.rds")

# Dataset with repeat_targets=TRUE
japanese_vowels_repeat <- generate_data(dataset = "japanese_vowels", repeat_targets=TRUE)
saveRDS(japanese_vowels_repeat, "data/japanese_vowels_repeat.rds")
```

## Other Datasets

- `df_obfuscated_epidemio.rds`: Obfuscated epidemiological data
- `precomputed_results.rds`: Precomputed analysis results
