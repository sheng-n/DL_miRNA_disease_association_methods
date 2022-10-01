# A survey of deep learning and graph neural network for predicting miRNA-disease associations: databases, computational methods, challenges and future directions
![GitHub stars](https://img.shields.io/github/stars/sheng-n/DL_GNN_miRNA_disease_methods?color=red) ![GitHub forks](https://img.shields.io/github/forks/sheng-n/DL_GNN_miRNA_disease_methods?color=green&label=Fork) ![visitors](https://visitor-badge.glitch.me/badge?page_id=sheng-n.DL_GNN_miRNA_disease_methods)

## What is miRNA?
RNA can be divided into two categories based on its coding function: (1) RNAs with coding potential, and (2) RNAs without coding potential, also known as non-coding RNA (ncRNA), which includes microRNAs (miRNA), snoRNAs, circRNAs and lncRNAs. Long non-coding RNAs (lncRNAs) are a major class of important ncRNAs with the lengths more than 200 nucleotides. An increasing number of lncRNA have been found to be abnormally expressed in human diseases, and play a critical role in tumor development.

## Table of Contents
* [Overview](#Overview) 
* [Data resources](#Data-resources) 
  - [miRNA-disease association data resources](#miRNA-disease-association-data-resources)
  - [miRNA-related data resourcess](#miRNA-related-data-resources)
  - [Disease-related data resources](#Disease-related-data-resources)
* [Classical deep learning models for predicting MDAs](#Classical-deep-learning-models-for-predicting-MDAs) 
  - [Autoencoder](#Autoencoder)
  - [Multi-layer perceptron](#Multi-layer-perceptron)
  - [Convolutional neural network](#Convolutional-neural-network)
* [Graph neural network-based methods for predicting MDAs](#Graph-neural-network-based-methods-for-predicting-MDAs) 
  - [Graph convolutional network](#Graph-convolutional-network)
  - [Graph attention network](#Graph-attention-network)
  - [Graph autoencoder](#Graph-autoencoder)
* [Other deep learning methonds](#Other-deep-learning-methonds) 

## Overview
* We collect miRNA- and disease-related databases for MDA prediction, including miRNA-disease association databases, miRNA-related databases, and disease-related databases. 
* We provide the first a comprehensive overview of 45 MDA prediction models based on deep learning and graph neural networks. We classify the two types of models in detail, deep learning models such as autoencoder, multi-layer perceptron, convolutional neural network, variational autoencoder, gated recurrent unit, and generative adversarial network; graph neural network models such as graph convolutional network, graph attention network, graph autoencoder, as shown below figure 1.
![image](https://user-images.githubusercontent.com/95516781/193400787-c4ec3f72-5939-4f2c-8c6c-fe410cc0730d.png)

Fig 1: Deep learning and Graph neural network computational methods for MDA prediction. 

## Data resources
### miRNA-disease association data resources
| Database  | Description  | URL | 
|:------------------:|:-----:|:---------------: |
|HMDD v3.2 | Documents 19,166 lncRNAs, 529 diseases and 10,564 association in Homo sapiens, Mus musculus, Rattus norvegicus and Gallus gallus  | http://www.cuilab.cn/hmdd|
|dbDEMC 3.0    |Collects 2,659 lncRNAs, 216 cancers and 9,254 associations in human     |https://www.biosino.org/dbDEMC|
|miR2Disease    |Collects 2,659 lncRNAs, 216 cancers and 9,254 associations in human     |http://www.mir2disease.org/|
|miRCancer   |Collects 2,659 lncRNAs, 216 cancers and 9,254 associations in human     |http://mircancer.ecu.edu/ |
|miRwayD   |Collects 2,659 lncRNAs, 216 cancers and 9,254 associations in human     |http://www.mirway.iitkgp.ac.in/ |
|MNDR v4.0           |Records 39,880 lncRNA, over 1,600 diseases and 295,834 associations in 11 mammals |http://www.rnadisease.org/ |

### miRNA-related data resources
| Database  | Description  | URL | 
|:------------------:|:-----:|:---------------: |
|miRbase v22  | An archive of functional genomics datas  | https://www.mirbase.org/
|mirTarbase    |Records the comprehensive knowledge database of ncRNA from 39 speciesn |https://miRTarBase.cuhk.edu.cn/ |
|miRWalk |Documents ncRNA sequences for 296 species  |http://mirwalk.umm.uni-heidelberg.de/|
|starbase (ENCORI)   |Collects sequence, structure, function and phenotype information of experimentally validated lncRNAs|https://starbase.sysu.edu.cn/|
|lncRNASNP2|Records lncRNA-miRNA, miRNA-mRNA, ncRNA-RNA interactions information| http://bioinfo.life.hust.edu.cn/lncRNASNP|
|miREnvironment    |Documents the regulatory interactions between ncRNAs and other biomolecules|http://www.cuilab.cn/miren|


### Disease-related data resources
| Database  | Description  | URL | 
|:------------------:|:-----:|:---------------: |
|MeSH  | The DO semantically integrates disease and medical vocabularies  | http://www.nlm.nih.gov/ |
|HPO     |A comprehensive logical standard for describing and computationally analyzing phenotypic abnormalities found in human diseases |https://hpo.jax.org/app/ |
|OMIM  |Describes genes with known sequence and phenotypes   |http://www.ncbi.nlm.nih.gov/omim  |
|DisGeNet   |Collects 30,170 diseases, 21,671 genes and 1124,942 associations|https://www.disgenet.org/|
|LncRNADisease|Records 893 diseases, 1,206 miRNAs and 35,547 associations in human| http://www.rnanut.net/lncrnadisease/|

## Classical deep learning models for predicting MDAs
### Autoencoder
1. **[DeepMDA]** Fu L, Peng Q. A deep ensemble model to predict miRNA-disease association, Scientific Reports 2017;7(1):14482. [**[Download]**](https://www.nature.com/articles/s41598-017-15235-6 "Click") [**[Code]**](https://github.com/sperfu/DeepMDA "Click") 

2. **[DRMLDA]** Chen X, Gong Y, Zhang D-H et al. DRMDA: deep representations-based miRNA–disease association prediction, Journal of Cellular and Molecular Medicine 2018;22(1):472-485. [**[Download]**](https://onlinelibrary.wiley.com/doi/full/10.1111/jcmm.13336 "Click")

3. **[MLMDA]** Zheng K, You Z-H, Wang L et al. MLMDA: a machine learning approach to predict and validate MicroRNA–disease associations by integrating of heterogenous information sources, Journal of Translational Medicine 2019;17(1):260. [**[Download]**](https://translational-medicine.biomedcentral.com/articles/10.1186/s12967-019-2009-x "Click") 

4. **[DFELMDA]** Liu W, Lin H, Huang L et al. Identification of miRNA–disease associations via deep forest ensemble learning based on autoencoder, Briefings in Bioinformatics 2022;23(3). [**[Download]**](https://academic.oup.com/bib/article-abstract/23/3/bbac104/6553934?login=false "Click") [**[Code]**](https://github.com/Zj-Teng/DFELMDA "Click") 

5. **[MDA-CF]** Dai Q, Chu Y, Li Z et al. MDA-CF: Predicting MiRNA-Disease associations based on a cascade forest model by fusing multi-source information, Computers in Biology and Medicine 2021;136:104706. [**[Download]**](https://www.sciencedirect.com/science/article/pii/S001048252100500X "Click") [**[Code]**](https://github.com/a1622108/MDA-CF "Click") 

6. **[PMDFI]** Tang M, Liu C, Liu D et al. PMDFI: Predicting miRNA–Disease Associations Based on High-Order Feature Interaction, Frontiers in genetics 2021;12. [**[Download]**](https://www.frontiersin.org/articles/10.3389/fgene.2021.656107/full "Click") 

7. **[MSCNE]** Han G, Kuang Z, Deng L. MSCNE:Predict miRNA-Disease Associations Using Neural Network based on Multi-source Biological Information, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021:1-1. [**[Download]**](https://ieeexplore.ieee.org/document/9519511 "Click")

8. **[SMALF]** Liu D, Huang Y, Nie W et al. SMALF: miRNA-disease associations prediction based on stacked autoencoder and XGBoost, BMC Bioinformatics 2021;22(1):219. [**[Download]**](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-021-04135-2 "Click") [**[Code]**](https://github.com/dayunliu/SMALF "Click") 

9. **[MDA-CNN]** Peng J, Hui W, Li Q et al. A learning-based framework for miRNA-disease association identification using neural networks, Bioinformatics 2019;35(21):4364-4371. [**[Download]**](https://academic.oup.com/bioinformatics/article/35/21/4364/5448859?login=false "Click") [**[Code]**](https://github.com/
Issingjessica/MDA-CNN "Click") 

10. **[AEMDA]** Ji C, Gao Z, Ma X et al. AEMDA: inferring miRNA–disease associations based on deep autoencoder, Bioinformatics 2020;37(1):66-72. [**[Download]**](https://github.com/CunmeiJi/AEMDA "Click") [**[Code]**](https://github.com/CSUBioGroup/SDLDA "Click") 

11. **[iMDA-BN]** Zheng K, You Z-H, Wang L et al. iMDA-BN: Identification of miRNA-disease associations based on the biological network and graph embedding algorithm, Computational and Structural Biotechnology Journal 2020;18:2391-2400. [**[Download]**](https://www.sciencedirect.com/science/article/pii/S2001037020303767 "Click")

12. **[DANE-MDA]** 	Ji B-Y, You Z-H, Wang Y et al. DANE-MDA: Predicting microRNA-disease associations via deep attributed network embedding, iScience 2021;24(6):102455. [**[Download]**](https://www.sciencedirect.com/science/article/pii/S2589004221004235 "Click") [**[Code]**](https://github.com/jiboya123/DANE-MDA "Click") 

13. **[DBNMDA]** Chen X, Li T-H, Zhao Y et al. Deep-belief network for predicting potential miRNA-disease associations, Briefings in Bioinformatics 2020;22(3). [**[Download]**](https://academic.oup.com/bib/article-abstract/22/3/bbaa186/5898648?login=false "Click") 

14. **[SAEMD]** Wang C-C, Li T-H, Huang L et al. Prediction of potential miRNA–disease associations based on stacked autoencoder, Briefings in Bioinformatics 2022;23(2). [**[Download]**](https://academic.oup.com/bib/article-abstract/23/2/bbac021/6529883?login=false "Click") [**[Code]**](https://github.com/xpnbs/SAEMDA "Click") 

15. **[DBMDA]** Zheng K, You Z-H, Wang L et al. DBMDA: A Unified Embedding for Sequence-Based miRNA Similarity Measure with Applications to Predict and Validate miRNA-Disease Associations, Molecular Therapy - Nucleic Acids 2020;19:602-611. [**[Download]**](https://www.sciencedirect.com/science/article/pii/S2162253119304056 "Click") 

16. **[VAEMDA]** Zhang L, Chen X, Yin J. Prediction of Potential miRNA–Disease Associations Through a Novel Unsupervised Deep Learning Framework with Variational Autoencoder, Cells 2019;8(9):1040. [**[Download]**](https://www.mdpi.com/2073-4409/8/9/1040 "Click") 

17. **[SVAEMDA]** Ji C, Wang Y, Gao Z et al. A Semi-Supervised Learning Method for MiRNA-Disease Association Prediction Based on Variational Autoencoder, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2022;19(4):2049-2059. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9381658 "Click") 

### Multi-layer perceptron
1. **[EPMDA]** Dong Y, Sun Y, Qin C et al. EPMDA: Edge Perturbation Based Method for miRNA-Disease Association Prediction, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2020;17(6):2170-2175. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/8827911 "Click") 

2. **[MLRDFM]** Ding Y, Lei X, Liao B et al. MLRDFM: a multi-view Laplacian regularized DeepFM model for predicting miRNA-disease associations, Briefings in Bioinformatics 2022;23(3). [**[Download]**](https://academic.oup.com/bib/article-abstract/23/3/bbac079/6552270?login=false "Click") [**[Code]**](https://github.com/XYDBCS/MLRDFM "Click") 

### Convolutional neural network 
1. **[CNNDMP]** Xuan P, Dong Y, Guo Y et al. Dual Convolutional Neural Network Based Method for Predicting Disease-Related miRNAs, International journal of molecular sciences 2018;19(12):3732. [**[Download]**](https://www.mdpi.com/1422-0067/19/12/3732 "Click") 

2. **[CNNMDA]** Xuan P, Sun H, Wang X et al. Inferring the Disease-Associated miRNAs Based on Network Representation Learning and Convolutional Neural Networks, International journal of molecular sciences 2019;20(15):3648. [**[Download]**](https://www.mdpi.com/1422-0067/20/15/3648 "Click") 

3. **[DNRLCNN]** Zhong J, Zhou W, Kang J et al. DNRLCNN: A CNN Framework for Identifying MiRNA–Disease Associations Using Latent Feature Matrix Extraction with Positive Samples, Interdisciplinary Sciences: Computational Life Sciences 2022;14(2):607-622. [**[Download]**](https://link.springer.com/article/10.1007/s12539-022-00509-z "Click") 

## Graph neural models for predicting MDAs 
### graph convolutional network
1. **[HGCNMDA(1)]** Li C, Liu H, Hu Q et al. A Novel Computational Model for Predicting microRNA–Disease Associations Based on Heterogeneous Graph Convolutional Networks, Cells 2019;8(9):977. [**[Download]**](https://www.mdpi.com/2073-4409/8/9/977 "Click") 

2. **[Zhu’s method]** Zhu R, Ji C, Wang Y et al. Heterogeneous graph convolutional networks and matrix completion for miRNA-disease association prediction, Frontiers in bioengineering and biotechnology 2020;8:901. [**[Download]**](https://www.frontiersin.org/articles/10.3389/fbioe.2020.00901/full "Click") 

3. **[NIMCGCN]** Li J, Zhang S, Liu T et al. Neural inductive matrix completion with graph convolutional networks for miRNA-disease association prediction, Bioinformatics 2020;36(8):2538-2546. [**[Download]**]https://academic.oup.com/bioinformatics/article/36/8/2538/5697092 "Click") [**[Code]**](https://github.com/ljatynu/NIMCGCN/ "Click")

4. **[FCGCNMDA]** Li J, Li Z, Nie R et al. FCGCNMDA: predicting miRNA-disease associations by applying fully connected graph convolutional networks, Molecular Genetics and Genomics 2020;295(5):1197-1209. [**[Download]**](https://link.springer.com/article/10.1007/s00438-020-01693-7 "Click")

5. **[MMGCN]** Tang X, Luo J, Shen C et al. Multi-view Multichannel Attention Graph Convolutional Network for miRNA–disease association prediction, Briefings in Bioinformatics 2021;22(6). [**[Download]**](https://academic.oup.com/bib/article-abstract/22/6/bbab174/6271996 "Click") [**[Code]**](https://github.com/Txinru/MMGCN "Click")

6. **[GSCENet]** Li Z, Jiang K, Qin S et al. GCSENet: A GCN, CNN and SENet ensemble model for microRNA-disease association prediction, PLOS Computational Biology 2021;17(6):e1009048. [**[Download]**](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1009048 "Click") [**[Code]**](https://github.com/Appleabc123/GCSENet "Click")

7. **[MVIFMDA]** Xie X, Wang Y, Sheng N et al. Predicting miRNA-disease associations based on multi-view information fusion, Frontiers in genetics 2022;13. [**[Download]**](https://www.frontiersin.org/articles/10.3389/fgene.2022.979815/full "Click") 

8. **[MDA-GCNFTD]** Chu Y, Wang X, Dai Q et al. MDA-GCNFTG: identifying miRNA-disease associations based on graph convolutional networks via graph sampling through the feature and topology graph, Briefings in Bioinformatics 2021;22(6). [**[Download]**](https://academic.oup.com/bib/article-abstract/22/6/bbab165/6261915 "Click") [**[Code]**](https://github.com/a96123155/MDA-GCNFTG "Click")

9. **[MINIMDA]** Lou Z, Cheng Z, Li H et al. Predicting miRNA–disease associations via learning multimodal networks and fusing mixed neighborhood information, Briefings in Bioinformatics 2022. [**[Download]**](https://github.com/chengxu123/MINIMDA "Click") [**[Code]**](https://github.com/Txinru/MMGCN "Click")

10. **[HGCNMDA(2)]** Peng W, Che Z, Dai W et al. Predicting miRNA-disease associations from miRNA-gene-disease heterogeneous network with multi-relational graph convolutional network model, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2022:1-12. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9813368 "Click") [**[Code]**](https://github.com/weiba/HGCNMDA "Click")

11. **[MuCoMid]** Dong TN, Mucke S, Khosla M. MuCoMiD: A Multitask graph Convolutional Learning Framework for miRNA-Disease Association Prediction, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2022:1-1. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9779549 "Click") [**[Code]**](https://git.l3s.uni-hannover.de/dong/cmtt "Click")

12. **[SGNNMD]** Zhang G, Li M, Deng H et al. SGNNMD: signed graph neural network for predicting deregulation types of miRNA-disease associations, Briefings in Bioinformatics 2021;23(1). [**[Download]**](https://academic.oup.com/bib/article-abstract/23/1/bbab464/6455665 "Click") [**[Code]**](https://github.com/bubblecode/SGNNMD "Click")

### graph attention network
1. **[HGATMDA]** Ji C, Wang Y, Ni J et al. Predicting miRNA-Disease Associations Based on Heterogeneous Graph Attention Networks, Frontiers in genetics 2021;12. [**[Download]**](chrome-extension://cdonnmffkdaoajfknoeeecmchibpmkmg/assets/pdf/web/viewer.html?file=https%3A%2F%2Ffjfsdata01prod.blob.core.windows.net%2Farticles%2Ffiles%2F727744%2Fpubmed-zip%2F.versions%2F1%2F.package-entries%2Ffgene-12-727744%2Ffgene-12-727744.pdf%3Fsv%3D2018-03-28%26sr%3Db%26sig%3DTtrU2rU%252BOHDjdsgM6n2OL4ASfiupSmZRiCzuMkafpWc%253D%26se%3D2022-10-01T08%253A20%253A23Z%26sp%3Dr%26rscd%3Dattachment%253B%2520filename%252A%253DUTF-8%2527%2527fgene-12-727744.pdf "Click")

2. **[GRPAMDA]** Zhong T, Li Z, You Z-H et al. Predicting miRNA–disease associations based on graph random propagation network and attention network, Briefings in Bioinformatics 2022;23(2). [**[Download]**](https://academic.oup.com/bib/article-abstract/23/2/bbab589/6515233 "Click") [**[Code]**](https://github.com/ZTangBo/GRPAMDA "Click")

3. **[HGANMDA]** Li Z, Zhong T, Huang D et al. Hierarchical graph attention network for miRNA-disease association prediction, Molecular Therapy 2022;30(4):1775-1786. [**[Download]**](https://www.sciencedirect.com/science/article/pii/S1525001622000806 "Click") [**[Code]**](https://github.com/ZTangBo/HGANMDA "Click")

4. **[MDPBMP]** Yu L, Zheng Y, Gao L. MiRNA–disease association prediction based on meta-paths, Briefings in Bioinformatics 2022;23(2). [**[Download]**](https://academic.oup.com/bib/article-abstract/23/2/bbab571/6501422 "Click") [**[Code]**](https://github.com/LiangYu-Xidian/MDPBMP "Click")

### graph autoencoder
1. **[GCAEMDA]** Li L, Wang Y-T, Ji C-M et al. GCAEMDA: Predicting miRNA-disease associations via graph convolutional autoencoder, PLOS Computational Biology 2021;17(12):e1009655. [**[Download]**](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1009655 "Click") [**[Code]**](https://github.com/zhanglabNKU/VGAELDA "Click")

2. **[NIMGSA]** Jin C, Shi Z, Lin K et al. Predicting miRNA-Disease Association Based on Neural Inductive Matrix Completion with Graph Autoencoders and Self-Attention Mechanism, Biomolecules 2022;12(1):64. [**[Download]**](https://www.mdpi.com/2218-273X/12/1/64 "Click") [**[Code]**](https://github.com/zhanglabNKU/NIMGSA "Click")

3. **[GAEMDA]** Li Z, Li J, Nie R et al. A graph auto-encoder model for miRNA-disease associations prediction, Briefings in Bioinformatics 2020;22(4). [**[Download]**](https://academic.oup.com/bib/article-abstract/22/4/bbaa240/5929824 "Click") [**[Code]**](https://github.com/chimianbuhetang/GAEMDA "Click")

4. **[AGAEMD]** Zhang H, Fang J, Sun Y et al. Predicting miRNA-disease associations via node-level attention graph auto-encoder, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2022:1-1. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9767602 "Click") [**[Code]**](https://github.com/Zhhuizhe/AGAEMD "Click")

5. **[VGAE-MDA]** Ding Y, Tian L-P, Lei X et al. Variational graph auto-encoders for miRNA-disease association prediction, Methods 2021;192:25-34. [**[Download]**](https://www.sciencedirect.com/science/article/pii/S104620232030164X "Click")

6. **[VGAMF]** Shi Z, Zhang H, Jin C et al. Ding Y, Lei X, Liao B et al. Predicting miRNA-Disease Associations Based On Multi-View Variational Graph Auto-Encoder With Matrix Factorization, IEEE Journal of Biomedical and Health Informatics 2022;26(1):446-457. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9451570 "Click") [**[Code]**](https://github.com/XYDBCS/VGAMF "Click")

## Other deep learning methonds
1. **[CEMDA]** Liu B, Zhu X, Zhang L et al. Combined embedding model for MiRNA-disease association prediction, BMC Bioinformatics 2021;22(1):161. [**[Download]**](https://link.springer.com/article/10.1186/s12859-021-04273-7 "Click") [**[Code]**](https://github.com/liubailong/CEMDA "Click")

2. **[GMDA]** Xuan P, Wang D, Cui H et al. Integration of pairwise neighbor topologies and miRNA family and cluster attributes for miRNA–disease association prediction, Briefings in Bioinformatics 2021;23(1). [**[Download]**](https://academic.oup.com/bib/article-abstract/23/1/bbab428/6385813?login=false "Click")

## Welcome to contribute

```
@article{DL_MDA,
  title={A survey of deep learning for predicting miRNA-disease associations: databases, computational methods, challenges, and future directions},
  author={Nan Sheng, Xuping Xie, Lan Huang, Shuangquan Zhang, Ling Gao and Yan Wang},
  journal={Genomics, Proteomics & Bioinformatics (Awaiting submissions)},
  year={2022},
  publisher={ELSEVIER}
}
```

If you would like to help contribute this list, please feel free to contact me by email:

* Email: shengnan21@mails.jlu.edu.cn
