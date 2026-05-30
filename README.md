# Anglova_cyborg
# Anglova CybORG

Project page for the **Anglova CybORG** multi-agent cyber-physical defense simulation.

## Overview

Anglova CybORG is a cyber-physical defense simulator built on the CybORG framework. The project investigates how scalable Blue defender teams (1, 2, 4, 8, 16 defenders) perform against 1-4 Red attackers across three collision modes, with a focus on collision degradation effects and defense performance scaling.

The simulation supports three collision modes:
- **spread** — Red attackers distribute targets across available Blue defenders
- **all_to_1** — All Red attackers converge on a single Blue defender
- **pairwise** — Red attackers engage Blue defenders in one-to-one pairs

## Defender-Attacker Combinations

| Defenders | Attackers | Total Scenarios |
|-----------|-----------|-----------------|
| 1D | 1A, 2A, 3A, 4A | 4 |
| 2D | 1A, 2A, 3A, 4A | 4 |
| 4D | 1A, 2A, 3A, 4A | 4 |
| 8D | 1A, 2A, 3A, 4A | 4 |
| 16D | 1A, 2A, 3A, 4A | 4 |

**Total: 20 unique D:A ratio scenarios**

## Key Features

- **Scalable Defender Teams:** 1, 2, 4, 8, 16 Blue defenders against 1-4 Red attackers
- **D:A Ratio Analysis:** Performance across 20 unique defender-to-attacker combinations
- **Collision Degradation:** Models performance decay when multiple Red agents target the same Blue agent
- **Attack Log Analysis:** Comprehensive logging of attack events and outcomes
- **CSV Data Export:** Scenario results exported for further analysis and visualization

## Simulation Architecture

| Component | Description |
|-----------|-------------|
| Red Agents | 1-4 attackers targeting Blue infrastructure |
| Blue Agents | 1/2/4/8/16 defenders protecting convoy assets |
| Collision Modes | spread / all_to_1 / pairwise |
| Degradation Model | Performance penalty for target overlap |

## Results & Graphs

### Defense Survival Rate by D:A Ratio

![Defense Survival Rate](graphs/defense_survival_da_ratio.png)

*Figure 1: Blue defender survival rate across all 20 D:A combinations. Survival improves with higher D:A ratios, but diminishing returns appear beyond 4D:1A. The all_to_1 mode shows the steepest degradation at low D:A ratios.*

### Attack Success Rate by D:A Ratio

![Attack Success Rate](graphs/attack_success_da_ratio.png)

*Figure 2: Red attacker success rate across all 20 D:A combinations. Success drops sharply as defender count increases, with 16D configurations showing near-zero success in spread mode.*

### Collision Degradation by Attacker Count

![Collision Degradation](graphs/collision_degradation_attackers.png)

*Figure 3: Performance degradation as a function of simultaneous Red attackers targeting the same Blue defender. Degradation intensifies with 3A and 4A in all_to_1 mode, showing non-linear decay curves.*

### D:A Scaling Efficiency

![Scaling Efficiency](graphs/scaling_efficiency.png)

*Figure 4: Marginal defensive gain per additional defender. Efficiency peaks at 4D for 1-2A scenarios, with 8D and 16D showing reduced marginal returns against 3-4A.*

### Scenario Timeline — 4D:4A All-to-1

![Scenario Timeline](graphs/timeline_4d4a_allto1.png)

*Figure 5: Event timeline for 4D:4A in all_to_1 mode. All four Red attackers converge on one Blue defender, causing rapid degradation while other three defenders remain idle.*

### Scenario Timeline — 16D:4A Spread

![Scenario Timeline](graphs/timeline_16d4a_spread.png)

*Figure 6: Event timeline for 16D:4A in spread mode. Four Red attackers distribute across sixteen defenders, resulting in minimal per-defender pressure and high survival rates.*

### Heatmap — Survival Rate (D × A)

![Survival Heatmap](graphs/survival_heatmap_da.png)

*Figure 7: Heatmap of defender survival rates across all D:A combinations. Darker cells indicate higher survival. The 16D column shows consistently high survival regardless of attacker count.*

### Heatmap — Attack Success (D × A)

![Attack Success Heatmap](graphs/attack_success_heatmap_da.png)

*Figure 8: Heatmap of Red attack success rates across all D:A combinations. Success concentrated in low-D high-A regions, particularly 1D:4A and 2D:4A.*

### Collision Mode Comparison — 4D:4A

![Collision Mode Comparison](graphs/collision_comparison_4d4a.png)

*Figure 9: Side-by-side comparison of spread, all_to_1, and pairwise modes for 4D:4A. All_to_1 produces the most asymmetric outcome with one defender overwhelmed while others survive.*

### Time-to-Compromise by D:A Ratio

![Time to Compromise](graphs/time_to_compromise.png)

*Figure 10: Average time until first Blue defender compromise. Higher D:A ratios extend time-to-compromise, with 16D configurations showing 3-5x longer resilience than 1D.*

## Resources

- [Project Report](report.pdf)
- [Presentation Slides](slides.pdf)
- [Supplementary Materials](supplementary/)
- [Code & Experiments](code/)

## Website

Visit the project page: [https://yourusername.github.io/Anglova_cyborg/](https://fasnanadeera.github.io/Anglova_cyborg/)

## Citation
