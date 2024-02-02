# Randomized-Anonymization

We proposed privacy-preserving methods for data sharing that satisfy both k-anonymity and ε-differential privacy.

The proposed methods are
k-RR (k-anonymization → randomized response), RR-k (randomized response → k-anonymization), and (ε, k)-Randomized Anonymization.

## Important Note

Step 1 in Algorithms 1 and 3 in [our paper](https://doi.org/10.5220/0011665600003414) (k-RR and Randomized Anonymization) need not truly satisfy $k$(or $k'$)-anonymity. Rather, it is essential that the partitioning is dataset-independent for satisfying differential privacy (and for Theorems 1 and 3). In our experiments, for the sake of simplicity, we apply a strict $k$-anonymization method for their Step 1, but in practice, a fixed partitioning method should be used, such that approximately $k$-anonymity is satisfied. (Please also see Errata below.) (A simplest partitioning would be to ${\it arbitrarily}$ fix the separation with reference to a partition that satisfies strict $k$-anonymity. Even when the fixed separation is published, it would be sufficient if the original dataset cannot be inferred.)

## Important future directions

・Developing (approximate) k-anonymization methods more suited for the integration with Randomized Response (especially for Algorithms 1 and 3). In particular, the method for calculating representative values should be carefully considered. (In our experiments, we ignore events in which the representative values vary between neighboring datasets.)

・Utilizing Optiimized Local Hashing (OLH) [[Wang et al., 2017](https://www.usenix.org/system/files/conference/usenixsecurity17/sec17-wang-tianhao.pdf)] instead of Randomized Response.

・Improving the handling of numeric (continuous value) data.

(・How should we determine appropriate values of ε and k for each medical information?)

## Note

For details of our mechanisms, please see our paper entitled "(ε, k)-Randomized Anonymization: ε-Differentially Private Data Sharing with k-Anonymity" (https://doi.org/10.5220/0011665600003414) presented at HEALTHINF 2023.

Errata:

・p.289. 3.2.1
  "When the following inequality holds: $ε ≥$" → "When the following inequality holds: $e^ε ≥$"  

・Algorithm 1, Step 1. "each cluster has" → "each cluster is expected to have"  
・Algorithm 3, Step 1. "each cluster has" → "each cluster is expected to have"   (Please also see Important Note above.)

### Contact
Akito Yamamoto

Division of Medical Data Informatics, Human Genome Center,

the Institute of Medical Science, the University of Tokyo

a-ymmt@ims.u-tokyo.ac.jp
