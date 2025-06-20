<!-- DO NOT CHANGE MARKDOWN HEADERS. IF CHANGED, MODEL CARD MAY BE REJECTED BY A REVIEWER -->

<!-- `description.md` is required. -->

ATOMICA is a hierarchical geometric deep learning model trained on over 2.1 million molecular interaction interfaces. It represents interaction complexes using an all-atom graph structure, where nodes correspond to atoms or grouped chemical blocks, and edges reflect both intra- and intermolecular spatial relationships. The model uses SE(3)-equivariant message passing to ensure that learned embeddings are invariant to rotations and translations of molecular structures. The architecture produces embeddings at multiple scales—atom, block, and graph—that capture fine-grained structural detail and broader functional motifs. [Project Website](https://zitniklab.hms.harvard.edu/projects/ATOMICA/)

The model has been pretrained on 2,105,703 molecular interaction interfaces from the Protein Data Bank and Cambridge Structural Database, spanning multiple interaction types including protein-small molecule, protein-ion, small molecule-small molecule, protein-protein, protein-peptide, protein-RNA, protein-DNA, and nucleic acid-small molecule complexes. The pretraining strategy involves denoising transformations (rotation, translation, torsion) and masked block-type prediction, enabling the model to learn chemically grounded, transferable features. ATOMICA supports downstream tasks via plug-and-play adaptation with task-specific heads, including binding site prediction and protein interface fingerprinting. [Project Website](https://zitniklab.hms.harvard.edu/projects/ATOMICA/) | [GitHub](https://github.com/mims-harvard/ATOMICA/tree/main)



## Model Architecture
ATOMICA employs a hierarchical geometric deep learning architecture with the following key components:
- An all-atom graph representation of molecular complexes where nodes correspond to atoms or chemical blocks
- SE(3)-equivariant message passing to ensure rotational and translational invariance
- Multi-scale embeddings at atom, block, and graph levels
- Pretraining via denoising transformations and masked block-type prediction
