# mcmc_decryption

This project applies a Markov Chain Monte Carlo (MCMC) algorithm to decode a monoalphabetic substitution cipher. It was completed for IEMS 315: Stochastic Models (Fall 2024) at Northwestern University.

## Objective

To decipher a coded message by probabilistically searching for the best character-to-character translation using stochastic sampling.

## Method

- Proposed new translation functions by swapping characters in the key.
- Evaluated candidate solutions using bigram frequencies from Jane Austen's corpus.
- Used Metropolis-Hastings acceptance to iteratively converge toward a high-likelihood decoding.

## Output

After 20,000 iterations, the algorithm recovered a coherent English translation of the encoded message — a passage from *Romeo and Juliet*.  
The decoded result includes minor errors (e.g., "loke" instead of "love") due to local optima in the sampling space.

## Files

- `mcmc_decoder.py` – Implements proposal, scoring, and the MCMC algorithm loop.
- `ciphertext.txt` – Encoded message (if publicly shareable).
- `M_matrix.csv` – Character bigram frequency matrix used to score translations.
- `Project_Report.pdf` – Full write-up with background, methods, and results.

## Report

For a full explanation of the algorithm and results, see [`Project_Report.pdf`](./Project_Report.pdf).

## Reproducibility

This project was completed as part of IEMS 315: Stochastic Models at Northwestern University.

Due to course policy, the original data files (`code.txt` and `austenCount.txt`) are not included in this repository.  
To run the notebook, you will need:

- An encoded message to decode (plaintext `.txt`)
- A bigram frequency matrix or scoring function 
