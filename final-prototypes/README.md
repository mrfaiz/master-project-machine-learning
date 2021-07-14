# Final Prototype of ML Master Project

# Project Goal and achievement
Initially our goal was to participate in the KDD Cup. The task of the KDD Cup was to build a model for Node Classification based on MAG240M-LSC (200 GB) Dataset. Due to hardware limitations and some issues in the Deep Graph Library, we forfeit the idea of participate in the KDD Cup. Although we would love to compete in the KDD Cup, we did not foresee the challenge of handling extremely large dataset.  

Then we shifted our focus on OGBN-MAG (1GB) dataset. The task was to predict the venue (conference or journal) of each paper, given its content, references, authors, and authors’ affiliations. Though this dataset was not quite as large as the previous one, but both dataset are closely resembled. We worked with RGCN and HAN model. Regarding RGCN, we concentrated with two varient a) Prefilling missing feature with zero value b) Featureless Embedding. We also did experiment with HAN model. However we also encountred the same difficulties regarding resources limitation and DGL issue like previous dataset. Our RGCN Model variant with Prefilling missing feature achieved 28% test accuracy.

Finally, we worked with ACM Dataset. The task was to predict the conference of a paper. Compared to two previous dataset, here we achieved fairly good results. We wrote two models, a) RGCN (Featureless embedding) b) HAN with 2 meta path. Both models achieved more than 85% test accuracy.  



# Contributions

## Faiz Ahmed

* Homogeneous graph and heterogeneous graph
* Graph neural network (GNN)
* Play with DGLGraph : Example link : https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/toy-codes-faiz/-/blob/master/zacharys-karate-club-with-dgl.ipynb

* Literature Research: Homo/Heterogeneous graph, Image Convolution and Graph Convolution, GNN, GCN, Message passing Framework, GAT. Git link for the presentation of initial literature study: https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/dgl-test/-/blob/master/presentation.pdf
* Implementation of Heterogeneous graph. https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/toy-codes-faiz/-/blob/master/zacharys-karate-club-with-dgl.ipynb
* Used some API's of DGL 
* Played with \textbf{MAG240M-LSC (200 GB)}. Tried to sub sample and process this dataset. But failed for infrastructure limitation. Some code links:
- https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/toy-codes-faiz/-/blob/master/MAG240MDataset.ipynb
- https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/toy-codes-faiz/-/blob/master/graph_subsampling.ipynb
- https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/toy-codes-faiz/-/blob/master/preprocess.py
- GAT implementation : https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/toy-codes-faiz/-/tree/master/gat
* Worked also with **OGBN-MAG (1GB) ** , but again RAM limitation

## Md Mashiur Rahman

* Prepare and train HeterogeneousRGCN Model for Node Classification on ACM Dataset with CSV file logger. 
[Link here.](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/final-prototypes/-/blob/master/Hetero_Graphs_Node_Classify_ACM.ipynb) 

* Combine RGCN (Prefilling missing feature with zero value) & HeteroRGCN (Featureless Embedding) models and Train both models for Node Classification on OGBN-MAG Dataset with CSV file logger. 
[Link here.](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/final-prototypes/-/blob/master/heterograph-node-classification-model.ipynb)


## Abdullah Al Amin

* Prepare and train HAN Model for Node Classification on ACM Dataset with CSV file logger as well as combine it with RGCN model. 
[Link here.](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/final-prototypes/-/blob/master/ACM_unified_v2.ipynb)

* RGCN model with prefilling values for missing features. [link here](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/final-prototypes/-/blob/master/heterograph%20node%20classification%20mag.ipynb)
* RGCN model with featureless embedding. [Link here](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/final-prototypes/-/blob/master/heterograph%20node%20classification%20mag%20with%20featureless%20embedding.ipynb)
* A naive apporach to graph subsampling.[Link here](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/final-prototypes/-/blob/master/graph%20subsampling.ipynb)


## Shaokat Hossain

* Preprocess OGBN-MAG dataset. [link here](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/final-prototypes/-/blob/master/ogbm-mag-data-preproecessing.ipynb)

* GAT(Optimized) implementation. [link here](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/dgl-practice/-/blob/master/GAT(Optimized).ipynb)
* GCN implementation. [link here](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/dgl-practice/-/blob/master/DGL%20Node%20classification%20.ipynb)


## Mithun Das

* I proposed these 3 dataset which I got finally in kaggle and 2 in OGB dataset itself to my team.It has almost same features but in every dataset we had different task to do. But finally we took \textbf{OGBN-MAG (1GB)} which has same feature as the \textbf{MAG240M-LSC (200 GB)} dataset.My proposed dataset are below:  
    1. ogbn-arxiv [here](https://www.kaggle.com/dataup1/ogbn-arxiv)
    2. ogbn-mag[here](https://www.kaggle.com/dataup1/ogbn-mag)
    3. ogbg-moltoxcast[here](https://www.kaggle.com/dataup1/ogbg-moltoxcast)
* DGL implementation [here](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/dgl-practice/-/blob/dgl-practice-md/DGL.ipynb)    
* preproecessing MAG try [here](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/dgl-practice/-/tree/dgl-practice-md/dataset/dataset/ogbn_mag/processed)
* Little ball of fur implementation: [here](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/dgl-practice/-/tree/dgl-practice-md) 
* Node classification on mag-checkpoints GCN [here](https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/dgl-practice/-/blob/dgl-practice-md/dataset/.ipynb_checkpoints/heterograph%20node%20classification%20mag-checkpoint.ipynb)
          
## Rishabh Lakra

* Extensive literature research on homogenous and heterogenous information networks, GNNs, R-GCNs, message passing framework and heterogenous GATs. A considerable part of it was achieved not just with the recommended papers, but with quite a few external resources as well. 

* Played around with heterographs and tried building a small scale movie recommendation model, with the aim that some of the characteristics can be translated to the  main HAN model, since movie data is also in the form of heterogenous graphs. 
[Link1](https://deeprs-tutorial.github.io/WWW_GNNs.pdf) 
[Link2](https://www.programmersought.com/article/94373949279/)

* Worked with a subset (2GB) of the MAG dataset, modified by Ankit Malhotra. Digged down deep on DGL documentation during this. [(https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/final-prototypes/-/blob/master/pre-processing.ipynb)]

## Ankit Malhotra

* Pre-Processing for OGBN-MAG (Adding reverse edges to the dataset) [(https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/final-prototypes/-/blob/master/main.ipynb)]

* HAN model implementation (Stochastic Training for OGBN-MAG Dataset). [(https://git.informatik.uni-kiel.de/ag-isdm/modules/ml-master-projects/kdd-cup2021/final-prototypes/-/blob/master/pre-processing.ipynb)]
