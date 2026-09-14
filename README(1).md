# Sparse Attention from Scratch

## Overview
This project implements sparse attention from scratch in PyTorch.

Implemented:
- Dense attention (manual matmul + mask + softmax)
- Sliding Window Sparse Attention
- Block Sparse Attention
- NaN handling for fully masked queries
- Correctness harness
- Benchmarking against dense attention

## Files

- Task1.ipynb : Main implementation
- correctness_harness.py : Correctness tests
- benchmark.py : Runtime and memory benchmarks
- WRITEUP.md : Analysis and observations

## Requirements

Python 3.10+

Install dependencies:

pip install torch numpy matplotlib

## Running the notebook

Open Task1.ipynb in Google Colab and run all cells.

## Correctness Harness

Run:

python correctness_harness.py

Expected output:

PASS

if sparse attention matches dense attention within tolerance.

## Benchmark

Run:

python benchmark.py

The script reports:
- Execution time
- Peak memory
- Sequence length scaling

## Implemented Sparsity Patterns

### Sliding Window
Each token attends only to nearby tokens inside a fixed window.

### Block Sparse
Attention is restricted to predefined blocks.

## NaN Handling

When a query has no valid attention positions, softmax(-inf,...,-inf) produces NaN.

This implementation detects such cases and replaces the output with zeros.

## Author

Vraj Badami
BITS PilaniS