## Improving Transformer’s Resilience to Transient Hardware Faults

**Duration:** Oct 2024 – May 2025

* **Literature Review**

  * Conducted a thorough literature review focusing on enhancing fault tolerance of Transformer-based Large Language Models (LLMs) against transient hardware faults (e.g., bit-flips, transmission errors, arithmetic faults).

* **Architecture-Level Improvements**

  * Proposed novel architecture-level improvements involving targeted modifications such as weight redundancy, self-attention mechanism optimization, pruning strategies, and adversarial training combined with simulated hardware faults.

* **Robustness Regularization**

  * Developed and optimized a robustness regularization technique integrated into Transformer training:

    * Addressed robustness penalty scaling by implementing layer-wise normalization.
    * Mitigated gradient instability through gradient clipping before optimization.
    * Adopted a warm-up strategy to gradually introduce robustness regularization, significantly stabilizing training.

* **Training Efficiency Optimization**

  * Enhanced training efficiency through optimized TensorFlow data pipelines:

    * Implemented caching, prefetching, and mixed-precision training.
    * Minimized runtime overhead by reducing frequent `.numpy()` calls and relocating non-essential data processing outside training loops.
    * Adjusted batch sizes to balance computational efficiency and hardware constraints.

* **Fault Injection Framework**

  * Integrated a comprehensive fault injection framework capable of simulating transient hardware faults, performing robustness assessments, and computing critical metrics (Silent Data Corruption (SDC) rates, crash rates).
  * Conducted targeted fault injection experiments primarily on the first Transformer layer, chosen for its significant impact on model output and relatively low computational overhead.

* **Robustness Improvement Outcomes**

  * Reduced the SDC rate from approximately 80% to 74% without compromising model accuracy.
  * Significantly limited post-fault injection loss degradation (originally increasing from 0.08 to 0.20, improved to approximately 0.10).

* **Visualization and Interface**

  * Enabled real-time performance visualization and provided translation interfaces, facilitating external validation and usability testing.

* **Project Limitations**

  * Acknowledged constraints due to limited hardware and computational resources, utilizing approximately 1% of the full dataset with limited training epochs.
