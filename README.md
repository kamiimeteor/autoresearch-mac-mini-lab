# Autoresearch Mac Mini Lab

Personal research log of running Karpathy-style autonomous AI research loops on Apple Silicon (M4 Mac mini).

This repository documents experiments using the MLX port of autoresearch to explore:

- Model structure search
- Step-efficiency optimisation under fixed training budget
- Hardware-specific training behaviour on unified memory systems
- Self-improving training workflows driven by evaluator metrics

## Hardware

- Machine: Apple Mac mini (M4)
- Memory: 32GB unified memory
- Framework: Apple MLX
- Training budget per experiment: ~5 minutes

## Research Method

Each experiment follows a strict autoresearch loop:

1. Modify `train.py`
2. Run fixed-time training experiment
3. Evaluate validation metric (`val_bpb`)
4. Keep change if metric improves
5. Revert if performance degrades

## Current Best Result

- Model: 12-layer Transformer
- Hidden dimension: 768
- MLP hidden size: 1280
- Best `val_bpb`: **2.216**

## Motivation

This lab explores how smaller, faster-training models can outperform larger ones under fixed wall-clock constraints, especially on Apple Silicon hardware.

The long-term goal is to understand and build self-improving AI systems that can autonomously explore optimisation strategies.

## Notes

Results are hardware-specific and may not transfer directly to larger GPU systems.

More experiment logs and insights will be added over time.
