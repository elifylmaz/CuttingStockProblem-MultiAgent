# Multi-Agent Cutting Stock Problem Solver

## Overview

This project analyzes multi-agent configurations to solve the **Cutting Stock Problem (CSP)** with a stock length of `101` units and piece lengths of `[11, 17, 23]`. The goal is to **minimize waste** (unused stock length) and **reduce cutting costs** by minimizing the number of pieces, while optimizing **computational efficiency** (runtime and loop count). 

The project tests various:
- **Agent counts**: 3 and 6
- **Algorithms**: Simulated Annealing (SA), Hill Climbing (HC), Genetic Algorithm (GA), and combinations
- **Approaches**: Collaborative and Hyper-heuristic

An additional interactive code allows users to specify **custom stock lengths**, **piece lengths**, **agent counts**, **algorithms**, and **approaches**.

---

## Features

- 🔁 **Flexible Configurations**  
  Test 3 or 6 agents with SA, HC, GA, or their combinations in Collaborative or Hyper-heuristic approaches.

- 🎯 **Optimization Goals**  
  Minimize waste and piece count to reduce cutting costs, with metrics for runtime and loop count.

- 🧪 **Interactive Experiments**  
  Run custom experiments with user-defined inputs (e.g., stock lengths of `176` or `250`, piece lengths like `[12, 23]` or `[15, 23]`).

- 📊 **Comprehensive Analysis**  
  Evaluate 28 predefined experiments and user-driven tests for performance insights.

---

## Experiment Summary

The project conducted **28 experiments** with a stock length of `101` units and piece lengths `[11, 17, 23]`. 

### 🔥 Best Configuration (Exp ID 23)

- **Setup**: 6 agents, Hill Climbing, Hyper-heuristic  
- **Result**: Zero waste, 7 pieces, 0.0002s runtime, 13 loops  
- **Why Best**: Achieves zero waste with minimal pieces and the fastest runtime, optimizing both cost and efficiency.

---

## Observations

- ✅ Most configurations (**27/28**) achieved **zero waste**, with **7 pieces**, showing consistency in minimizing piece count.
- ❌ **Exp ID 9** (3 agents, HC, Hyper-heuristic) was **suboptimal** (2 units waste) as Hill Climbing only explored nearby solutions.
- 📈 **6 agents** generally outperformed 3 agents  
  (e.g., **Exp ID 23** vs. **Exp ID 2**: `0.0002s`, 13 loops vs. `0.0006s`, 26 loops).
- ⚡ **Hill Climbing** was fastest, while **GA** had higher runtimes  
  (e.g., **Exp ID 17**: `0.6095s`).
- 🔄 **Hyper-heuristic** was efficient but risked suboptimal results, unlike the **reliable but costlier Collaborative approach**.

---

## Additional Experiments

- **Stock Length: 176**, **Piece Lengths: [12, 23]**  
  → 3 agents, GA, Collaborative  
  → ✅ Zero waste, 11 pieces, `0.1556s`

- **Stock Length: 250**, **Piece Lengths: [15, 23]**  
  → 8 agents, SA + HC + GA, Hyper-heuristic  
  → ✅ Zero waste, 14 pieces, `0.0354s`

