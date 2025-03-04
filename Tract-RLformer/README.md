# Tract-RLformer

> Accepted conference paper at **ICPR** 2024 (27th International Conference on Pattern Recognition)

**Abstract**

Tractography is a crucial process to map neuron pathways using Diffusion MRI scans, and is crucial for understanding brain connectivity, and for Neurosurgical planning
Tractography faces challenges due to its complexity and susceptibility to false positives, misrepresenting vital pathways. 
We propose Tract-RLFormer, a network utilizing both supervised and reinforcement learning, in a two-stage policy refinement process that markedly
improves the accuracy and generalizability across various data-sets. By
employing a tract-specific approach, our network directly delineates the
tracts of interest, bypassing the traditional segmentation process. 
Through rigorous validation on datasets such as **TractoInferno**, **HCP**, and **ISMRM2015**, our methodology demonstrates a leap forward in tractography,
showcasing its ability to accurately map the brain’s white matter tracts.

[Github](https://www.github.com/aj-30/Tract-RLformer) | [arxiv](https://arxiv.org/pdf/2411.05757)

Please cite our work!! 

```bibtex

@inproceedings{joshi2024tract,
  title={Tract-RLFormer: A Tract-Specific RL Policy Based Decoder-Only Transformer Network},
  author={Joshi, Ankita and Sharma, Ashutosh and Goel, Anoushkrit and Jha, Ranjeet Ranjan and Ahuja, Chirag Kamal and Bhavsar, Arnav and Nigam, Aditya},
  booktitle={International Conference on Pattern Recognition},
  pages={258--275},
  year={2024},
  organization={Springer}
}
```