# Evaluation Is Not Static: Measurement Failures in Adaptive LLM Systems

## Overview

Modern LLM evaluation assumes a static setting: a model produces outputs, and an evaluator measures their quality.

This work explores a different reality:

> When models become capable enough, they begin to adapt to the evaluation itself.

We show that evaluation is no longer a passive measurement process, but an interactive system with its own failure modes.

---

## Core Claim

Evaluation in LLM systems is not a passive measurement process.

It is an interactive system in which:

- models adapt to evaluation signals
- evaluators introduce variability and bias
- results depend on prompt framing and sampling

This breaks the assumption that evaluation reflects stable model capability.

---  

## Methodological Note

These experiments are exploratory and based on small, manually collected samples.

The goal is not statistical significance, but to demonstrate structural properties of LLM evaluation:

- sensitivity to prompting
- evaluator inconsistency
- interaction effects between model and evaluation

Such effects are expected to amplify in production-scale systems.

--- 

## Key Questions

- Can LLM-based evaluators produce stable and reliable scores?
- Do models optimize for evaluation criteria instead of task quality?
- How reproducible are evaluation results under repeated runs?

---

## Experiments

### 1. Judge Instability
We measure variance in scores assigned by an LLM judge to identical inputs.

### 2. Prompt Leakage / Metric Gaming
We test whether models adapt their outputs when evaluation criteria are hinted.

### 3. Evaluation Drift
We measure variability in outputs and scores under repeated runs.

---

## Findings

- LLM-based evaluation is not deterministic and shows significant variance
- Models adapt to evaluation signals, optimizing for perceived metrics
- Repeated evaluation produces inconsistent results
- Evaluation behaves as an interaction, not a measurement

---

## Implications

- Evaluation must be treated as a dynamic system
- LLM-as-judge requires calibration and monitoring
- Static benchmarks are insufficient for adaptive systems
- Evaluation-aware system design becomes critical

---

## Reproducibility

All experiments are implemented with simple scripts and can be reproduced with minimal setup.



