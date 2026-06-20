# Multi-Agent Reinforcement Learning Simulation

Q-learning implementation for Forager Agents in a stochastic grid environment — 
comparing single-agent vs. multi-agent and independent vs. shared Q-table strategies.

## Overview
Agents navigate a 10×10 grid with obstacles and renewable food resources, learning 
optimal foraging strategies via tabular Q-learning with epsilon-greedy exploration.

## Environment
- **Grid:** 10×10 with 5+ obstacles and 10 renewable food resources
- **Actions:** up, down, left, right
- **Rewards:** +10 food collected, -1 per step, -5 collision
- **Episodes:** 200 and 1,000 per experiment

## Q-Learning Parameters
| Parameter | Value | Justification |
|-----------|-------|---------------|
| Learning rate (α) | 0.15 | Stable yet responsive learning |
| Discount factor (γ) | 0.95 | Prioritises long-term rewards |
| Exploration rate (ε) | 0.20 | Persistent exploration in stochastic environment |

## Experiments
- **Single-agent:** 200 and 1,000 episodes — confirmed steady convergence toward near-optimal policy
- **Multi-agent (3 agents):** Independent Q-tables vs. shared Q-table across 200 and 1,000 episodes

## Key Findings
- Shared Q-table achieved faster convergence and higher food collection through accelerated knowledge sharing
- Independent Q-tables showed slower but more diverse learning as agents developed distinct policies
- Collision rates decreased over time in both setups — emergent implicit spatial coordination without explicit communication

## Files
- `Practical_assignment_Youssef_Zaky_202200208.ipynb` — full implementation
- `Practical_Assignment_Report.pdf` — project report
- `single_agent_200/1000.csv` — single-agent simulation results
- `multi_agent_independent/shared_200/1000_per_agent.csv` — multi-agent simulation results
