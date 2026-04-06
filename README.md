READ ME:
# TPC_RP (TypiClust) — CIFAR-10 Implementation
Implementation of the TPC_RP algorithm from:
*Active Learning on a Budget: Opposite Strategies Suit High and Low Budgets*
Hacohen, Dekel & Weinshall (ICML 2022)

## How to Run

### Step 1 — Pre-training (notebook1_simclr_pretrain.ipynb)
- Run on Kaggle with GPU enabled
- Trains SimCLR for 100 epochs on CIFAR-10
- Saves simclr_model.pt and embeddings.npy as a Kaggle Dataset

### Step 2 — TPC_RP Evaluation (notebook2_tpcrp_main.ipynb)
- Attach the dataset from Step 1 as input
- Runs TPC_RP query selection and all three evaluation frameworks
- Generates all plots and statistical analysis

## Reduced Hyperparameters
| Parameter | Paper | Mine |
|---|---|---|
| SimCLR epochs | 500 | 100 |
| Supervised epochs | 200 | 70 |
| SSL iterations | 400,000 | 30,000 |

Hyperparameters reduced due to computing power constraints. i do not have a gpu. 
