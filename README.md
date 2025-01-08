## GRACE: Generative Renaissance in Artificial Computational Enzyme Design
![ACS-SB-GRACE-TOC](https://github.com/user-attachments/assets/ff7cdd66-0bf5-4918-a503-d5db264c8765)
link to our paper:  
https://pubs.acs.org/doi/full/10.1021/acssynbio.4c00624

### Abstract
Designing de novo enzymes is complex and challenging, especially to maintain the activity. This research focused on motif design to identify the crucial domain in the enzyme and uncovered the protein structure by molecular docking. Therefore, we developed a Generative Redesign in Artificial Computational Enzymology (GRACE), which is an automated workflow for reformation and creation of the de novo enzymes for the first time. GRACE integrated RFdiffusion for structure generation, ProteinMPNN for sequence interpretation, CLEAN for enzyme classification, and followed by solubility analysis and molecular dynamic simulation. As a result, we selected two gene sequences associated with carbonic anhydrase from among 10,000 protein candidates. Experimental validation confirmed that these two novel enzymes, i.e., dCA12_2 and dCA23_1, exhibited favorable solubility, promising substrate-active site interactions, and achieved activity of 400 WAU/mL. This workflow has the potential to greatly streamline experimental efforts in enzyme engineering and unlock new avenues for rational protein design.
This is the automated workflow of translational design for de novo enzyme generation

### Dependency Installation Guideline
In this workflow, several models and conda environments are integrated, please download the following models and set up the corresponding conda environment: 
1. [RFdiffusion](https://github.com/RosettaCommons/RFdiffusion)
2. [ProteinMPNN](https://github.com/dauparas/ProteinMPNN)
3. [CLEAN](https://github.com/tttianhao/CLEAN)
4. [SoDoPe](https://github.com/Gardner-BinfLab/SoDoPE_paper_2020/tree/master/SWI)
5. [NetSolP](https://services.healthtech.dtu.dk/services/NetSolP-1.0/)
6. [GraphSol](https://github.com/jcchan23/GraphSol)

Note: After testing GraphSol, we found that there is **no need** to set protein sequence of 80 amino acid letters within one row. Besides, **this setting will cause the error in SPOT-Contact-Local**, which serves as the feature map generator in GraphSol.  

### Usage
To execute the *de novo* enzyme workflow:
```Bash
chmod +x Automated_script.sh
./Automated_script.sh
```
### Citation
If you find our work useful for your research, please cite us as:  
Hu, R. E., Yu, C. H., & Ng, I. S. (2024). GRACE: Generative Redesign in Artificial Computational Enzymology. ACS Synthetic Biology, 13(12), 4154-4164.
