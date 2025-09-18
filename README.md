# chess_inspired_human_ai_text_distinction

## Overview

This repository contains the data, code, and supplementary materials supporting *Beyond Checkmate: Exploring the Creative Chokepoints in AI Text* (**EMNLP'25 Main Conference**). The project investigates structural and stylistic differences between human-written and AI-generated texts, focusing on the “tripartite” structure of texts (Introduction, Body, Conclusion) and drawing an analogy with chess phases (Opening, Middlegame, Endgame).

Key aims:

- Determine which part (segment) of a text—intro, body, conclusion—is most informative for AI detection.  
- Use length-controlled experiments to reduce confounding by segment length.  
- Use move-pattern analysis in chess games to further validate findings about variability and optimality across game phases.

---
## Repository Structure
### Data Preparation

1. **Text Data**  
   - The `datasets/` folder includes cleaned versions of news (Ghostbuster/Reuters), essays (Persuade), emails (Enron subset).  
   - Preprocessed versions (segmented into intro/body/conclusion, tokenized, etc.) are also stored or generated via scripts in `code/segmentation/`.

2. **Chess Data**  
   - Chess datasets (move logs, Elo ratings) are stored under `chess_datasets/`.  
   - Scripted processing (e.g., computing optimal moves via Stockfish, computing SAN move-pattern overlap) lives in `code/chess_analysis/`.

### Running Experiments

- **Detection experiments**: Use code in `code/detection/` to run classifiers on specific segments or voting strategies.  
- **Length-controlled settings**: Subdirectories or params for settings C1 (equal segments), C2 (subsampled body), etc.  
- **Chess-phase analysis**: Use `code/chess_analysis/` to reproduce results showing overlap, % optimal moves by Elo and by game phase.

### Outputs & Figures

Figures and tables referenced in the paper are reproducible; plotting code is included. You can generate:

- F1-scores per segment & detector  
- Segmentation similarity metrics  
- Chess move-pattern overlaps & optimal move curves  

---

## Selected Findings

- Body / middle segments (or “voting” across segments) tend to yield the highest F1 for AI text detection, even under strict length control.  
- In chess, middlegame exhibits lower overlap in unique move-patterns compared to opening or endgame, corroborating the claim that “creative chokepoints” lie in middle phases.  
- Elo rating positively correlates with % of optimal moves; but this rate increases more steeply for AI players, especially in endgame vs middlegame relative to human players.

---

## Citation

If you use this work, please cite:
```bibtex
@article{tripto2025beyond,
  title={Beyond checkmate: exploring the creative chokepoints in AI text},
  author={Tripto, Nafis Irtiza and Venkatraman, Saranya and Nahar, Mahjabin and Lee, Dongwon},
  journal={arXiv preprint arXiv:2501.19301},
  year={2025}
}
```
