# Stochastic Optimization for Asset Acquisition: The World Cup Album Case

## Introduction
Every four years, the release of the World Cup sticker album presents a classic mathematical challenge: **The Coupon Collector's Problem**. As the number of unique assets increases and market prices fluctuate, completing the collection individually becomes financially inefficient due to high collision probabilities (duplicates).

This project explores the mathematical viability, speed, and cost-efficiency of different acquisition strategies, moving from purely stochastic methods to distributed Peer-to-Peer (P2P) networks.

## Methodology & Evolution
To find the most viable path to completion, the research was divided into several simulation phases using **Monte Carlo** methods:

1.  **Baseline Analysis:** We simulated the standard acquisition path, proving that retail promotions offer negligible savings (less than 1%) when faced with the high variance of the final assets.
2.  **Marginal Cost Thresholds:** We identified that the cost of acquiring a new unique asset via random packs eventually exceeds the premium of buying it directly. We established an automated "Stop-Loss" logic.
3.  **Parametric Optimization:** Through iterative testing, we discovered the **75% Inflection Point**. Stopping random purchases at this stage and pivoting to the secondary market minimizes the total financial risk for an individual node.
4.  **P2P Network Effect:** We simulated a distributed network of 10 participants. By implementing a zero-marginal-cost exchange protocol for duplicates, we achieved a systemic cost reduction of over 34%.
5.  **Hybrid Scale Model:** The final model combines P2P networking with dynamic market tiering. By categorizing assets into Tiers (Legends, Rookies, and Commons), we created a high-fidelity simulation that mirrors real-world market scarcity.

## Key Findings: The Power of 10
The research concludes that the most efficient strategy is the **10-Node Collaborative Network**. 
* **Cost Efficiency:** While an individual might spend upwards of $21,000 MXN to finish via packs, a member of a 10-person P2P network reaches completion with an average of **$5,400 - $5,600 MXN**.
* **Risk Mitigation:** Collaboration acts as a natural buffer against "bad luck" in pack openings, tightening the standard deviation of the total cost and making the budget highly predictable.
* **Optimal Pivot:** For a 10-person group, the mathematical "Sweet Spot" to stop buying packs is **95%**. At this point, the group should buy the remaining specific stickers to close the collection.

## How to Run
This project is contained within a Jupyter Notebook. To replicate the simulations and generate the charts:

1.  Clone this repository.
2.  Install the required dependencies using pip:
    ```bash
    pip install -r requirements.txt
    ```
3.  Open and run `simulator_main.ipynb`.

## Tech Stack
* **Language:** Python
* **Parallelism:** Multiprocessing (CPU core distribution for massive simulations)
* **Libraries:** NumPy (Data handling), Matplotlib (Visualization)
