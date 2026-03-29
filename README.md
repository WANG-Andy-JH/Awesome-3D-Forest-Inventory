# Awesome 3D Forest Inventory

Individual Tree Segmentation (ITS) on active LiDAR point cloud data.

## Table of Contents

- [Individual Tree Segmentation](#individual-tree-segmentation)
    - [Conventional Method](#conventional-method)
        - [Graph Based](#graph-based)
        - [Region-growing Based](#region-growing-based)
    - [Deeplearning Method](#deeplearning-method)
        - [Fully Supervised](#fully-supervised)
            - [Semantic-segmentation Based](#semantic-segmentation-based)
            - [Proposal Based](#proposal-based)
            - [Center-voting Based](#center-voting-based)
            - [Instance-mask Based](#instance-mask-based)
        - [Weakly Supervised](#weakly-supervised)
        - [Self Supervised](#self-supervised)
        - [Transfer Learning](#transfer-learning)
    - [Accuracy evaluation](#accuracy-evaluation)
        - [Point Accuracy](#point-accuracy)
        - [Boundary Accuracy](#boundary-accuracy)
- [Individual Tree Component Segmentation](#individual-tree-component-segmentation)
- [Individual Tree Parameter Estimation](#individual-tree-parameter-estimation)
- [Datasets](#datasets)
    - [ITS Datasets](#its-datasets)
    - [Synthetic](#synthetic)
        - [Modeling](#modeling)
        - [Simulation](#simulation)
- [Reviews](#reviews)
- [Comparative Study](#comparative-study)
- [Citation](#citation)
---


## Individual Tree Segmentation
### Conventional Method
#### Graph Based
Normalized cut, cut pursuit...

- ```2009``` &#9733; 3D segmentation of single trees exploiting full waveform LIDAR data ```ISPRS J```  [```paper```](https://www.sciencedirect.com/science/article/abs/pii/S0924271609000495)

- ```2015``` An efficient approach to 3D single tree-crown delineation in LiDAR data ```ISPRS J```  [```paper```](https://www.sciencedirect.com/science/article/pii/S0924271615001951)

- ```2016``` &#9733; Bottom-up delineation of individual trees from full-waveform airborne laser scans in a structurally complex eucalypt forest ```Remote Sensing of Environment``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0034425715301966#aep-article-footnote-id1)

- ```2020``` &#9733; Unsupervised semantic and instance segmentation of forest point clouds ```ISPRS J```  [```paper```](https://www.sciencedirect.com/science/article/pii/S0924271620301180?via%3Dihub)

- ```2022``` &#9733; 3D Graph-Based Individual-Tree Isolation (Treeiso) from Terrestrial Laser Scanning Point Clouds ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/14/23/6116) [```code```](https://github.com/truebelief/artemis_treeiso)


#### Region-growing Based
Processon CHM: Watershed (marker: local maxima, custom marker-control)
Bottom-up, local to global...
Clustering by seed points...

- ```2004``` &#9733; LIDAR-based geometric reconstruction of boreal type forest stands at single tree level for forest and wildland fire management ```Remote Sensing of Environment``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0034425704001464?via=ihub)

- ```2006``` &#9733; Isolating Individual Trees in a Savanna Woodland Using Small Footprint Lidar Data ``` Photogrammetric Engineering & Remote Sensing``` [```paper```](https://www.ingentaconnect.com/content/asprs/pers/2006/00000072/00000008/art00003)

- ```2010``` &#9733; Adaptive clustering of airborne LiDAR data to segment individual tree crowns in managed pine forests ```International Journal of Remote Sensing``` [```paper```](https://www.tandfonline.com/doi/full/10.1080/01431160902882561#abstract)

- ```2010``` Single tree detection in heterogeneous boreal forests using airborne laser scanning and area-based stem number estimates ```International Journal of Remote Sensing``` [```paper```](https://www.tandfonline.com/doi/full/10.1080/01431161.2012.657363#d1e251)

- ```2011``` Prior-knowledge-based single-tree extraction ```International Journal of Remote Sensing``` [```paper```](https://www.tandfonline.com/doi/full/10.1080/01431161.2010.494633)

- ```2012``` &#9733; A New Method for Segmenting Individual Trees from the Lidar Point Cloud ``` Photogrammetric Engineering & Remote Sensing``` [```paper```](https://www.ingentaconnect.com/content/asprs/pers/2012/00000078/00000001/art00006)

- ```2014``` &#9733; A bottom-up approach to segment individual deciduous trees using leaf-off lidar point cloud data ```ISPRS J``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0924271614000860?via%3Dihub)

- ```2014``` &#9733; An efficient, multi-layered crown delineation algorithm for mapping individual tree structure across multiple ecosystems ```Remote Sensing of Environment``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0034425714000984)

- ```2014``` A new procedure for identifying single trees in understory layer using discrete LiDAR data ```IGARSS``` [```paper```](https://ieeexplore.ieee.org/document/6946686)

- ```2014``` Impact of Tree-Oriented Growth Order in Marker-Controlled Region Growing for Individual Tree Crown Delineation Using Airborne Laser Scanner (ALS) Data ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/6/1/555)

- ```2014``` PTrees: A point-based approach to forest tree extraction from lidar data ```International Journal of Applied Earth Observation and Geoinformation``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0303243414001135)

- ```2015``` &#9733; A novel transferable individual tree crown delineation model based on Fishing Net Dragging and boundary classification ```ISPRS J``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0924271615002257?via%3Dihub)

- ```2015``` Agent-based region growing for individual tree crown delineation from airborne laser scanning (ALS) data ```International Journal of Remote Sensing``` [```paper```](https://www.tandfonline.com/doi/full/10.1080/01431161.2015.1030043#d1e185)

- ```2015``` Individual Tree Segmentation from LiDAR Point Clouds for Urban Forest Inventory ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/7/6/7892)

- ```2018``` Extracting individual trees from lidar point clouds using treeseg &#9733; ```Methods in Ecology and Evolution``` [```paper```](https://besjournals.onlinelibrary.wiley.com/doi/full/10.1111/2041-210X.13121) [```code```](https://github.com/apburt/treeseg)

- ```2022``` &#9733; Automatic tree crown segmentation using dense forest point clouds from Personal Laser Scanning (PLS) ```International Journal of Applied Earth Observation and Geoinformation``` [```paper```](https://www.sciencedirect.com/science/article/pii/S1569843222002138) [```code```](https://github.com/anditockner/treeX)

- ```2025``` &#9733; treeX: Unsupervised Tree Instance Segmentation in Dense Forest Point Clouds ```arxiv``` [```paper```](https://arxiv.org/abs/2509.03633) [```code```](https://github.com/ai4trees/pointtree)

### Deeplearning Method
#### Fully Supervised
##### Semantic-segmentation Based
Multiple tasks, main output of DL network are point-wise semantic labels.

- ```2021``` Individual Tree Crown Segmentation Directly from UAV-Borne LiDAR Data Using the PointNet of Deep Learning ```Forests``` [```paper```](https://www.mdpi.com/1999-4907/12/2/131) 

- ```2022``` A Two-Stage Approach for Individual Tree Segmentation From TLS Point Clouds ```IEEE``` [```paper```](https://ieeexplore.ieee.org/document/9913319)

- ```2024``` Supervised terrestrial to airborne laser scanner model calibration for 3D individual-tree attribute mapping using deep neural networks ```ISPRS J``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0924271624000558?via%3Dihub) [```code```](https://github.com/truebelief/artemis_treescaling/tree/main)

- ```2025``` Tree and shrub instance segmentation by boundary-aware ecological structural probability analysis ```Urban Forestry & Urban Greening``` [```paper```](https://www.sciencedirect.com/science/article/pii/S1618866725004571)

##### Proposal Based
Proposal based method is a Top-Down ***Bounding Box or Proposal first*** workflow. 

- ```2022``` Individual Tree Crown Segmentation and Crown Width Extraction From a Heightmap Derived From Aerial Laser Scanning Data Using a Deep Learning Framework ```Frontiers in Plant Science``` [```paper```](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2022.914974/full)

- ```2023``` Instance segmentation of individual tree crowns with YOLO v5: A comparison of approaches using the ForInstance benchmark LiDAR dataset ```ISPRS J``` [```paper```](https://www.sciencedirect.com/science/article/pii/S2667393223000169?via%3Dihub)

- ```2023``` Automatic Detection of Individual Trees in Forests Based on Airborne LiDAR Data with a Tree Region-Based Convolutional Neural Network (RCNN) ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/15/4/1024)

##### Center-voting Based
Center-voting method is a bottom-up workflow.
- ```2023``` &#9733; Towards accurate instance segmentation in large-scale LiDAR point clouds ```arxiv``` [```paper```](https://arxiv.org/abs/2307.02877) [```code```](https://github.com/prs-eth/PanopticSegForLargeScalePointCloud)

- ```2023``` Towards Intricate Stand Structure: A Novel Individual Tree Segmentation Method for ALS Point Cloud Based on Extreme Offset Deep Learning ```Applied Sciences``` [```paper```](https://www.mdpi.com/2076-3417/13/11/6853) [```data 1```](https://doi.pangaea.de/10.1594/PANGAEA.942856) [```data 2```](http://forsys.cfr.washington.edu/FUSION/fusion_overview.html) 

- ```2024``` &#9733; Automated forest inventory: Analysis of high-density airborne LiDAR point clouds with 3D deep learning ```Remote Sensing of Environment``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0034425724000890) [```code```](https://github.com/prs-eth/ForAINet)

- ```2024``` &#9733; SegmentAnyTree: A sensor and platform agnostic deep learning model for tree segmentation using laser scanning data ```Remote Sensing of Environment``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0034425724003936) [```code```](https://github.com/SmartForest-no/SegmentAnyTree)

- ```2024``` Towards general deep-learning-based tree instance segmentation models ```ICLR``` [```paper```](https://arxiv.org/pdf/2405.02061) [```data```](https://data.goettingen-research-online.de/dataset.xhtml?persistentId=doi:10.25625/QUTUWU)

- ```2024``` &#9733; TreeLearn: A deep learning method for segmenting individual trees from ground-based LiDAR forest point clouds ```Ecological Informatics``` [```paper```](https://www.sciencedirect.com/science/article/pii/S1574954124004308) [```data```](https://data.goettingen-research-online.de/dataset.xhtml?persistentId=doi:10.25625/VPMPID)

- ```2026``` A 3D point cloud instance segmentation network for extracting individual trees from complex forest scenes ```Computers and Electronics in Agriculture``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0168169925014395)

- ```2026``` ITS-Net: A platform and sensor agnostic 3D deep learning model for individual tree segmentation using aerial LiDAR data ```ISPRS J``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0924271625004587) [```data```](https://pan.baidu.com/s/1rJdpUeQqYR8A2gUbc8CxAA)

##### Instance-mask Based
- ```2022``` &#9733; Mask3D: Mask Transformer for 3D Semantic Instance Segmentation ```arxiv``` [```paper```](https://arxiv.org/abs/2210.03105) [```code```](https://github.com/JonasSchult/Mask3D)

- ```2024``` &#9733; OneFormer3D: One Transformer for Unified Point Cloud Segmentation ```CVPR``` [```paper```](https://openaccess.thecvf.com/content/CVPR2024/papers/Kolodiazhnyi_OneFormer3D_One_Transformer_for_Unified_Point_Cloud_Segmentation_CVPR_2024_paper.pdf) [```code```](https://github.com/filaPro/oneformer3d)

- ```2025``` &#9733; ForestFormer3D: A Unified Framework for End-to-End Segmentation of Forest LiDAR 3D Point Clouds ```arxiv``` [```paper```](https://arxiv.org/abs/2506.16991) [```code```](https://github.com/SmartForest-no/ForestFormer3D) [```data```](https://zenodo.org/records/16742708)

#### Weakly Supervised

--

#### Self Supervised
- ```2025``` &#9733; Label-Efficient 3D Forest Mapping: Self-Supervised and Transfer Learning for Individual, Structural, and Species Analysis ```arxiv``` [```paper```](https://arxiv.org/abs/2511.06331) [```code```](https://github.com/aldinorizaldy/TreeLite3D)

#### Transfer Learning
- ```2024``` &#9733; TreeLearn: A deep learning method for segmenting individual trees from ground-based LiDAR forest point clouds ```Ecological Informatics``` [```paper```](https://www.sciencedirect.com/science/article/pii/S1574954124004308) [```data```](https://data.goettingen-research-online.de/dataset.xhtml?persistentId=doi:10.25625/VPMPID)

- ```2025``` &#9733; Label-Efficient 3D Forest Mapping: Self-Supervised and Transfer Learning for Individual, Structural, and Species Analysis ```arxiv``` [```paper```](https://arxiv.org/abs/2511.06331) [```code```](https://github.com/aldinorizaldy/TreeLite3D)

### Accuracy Evaluation

Main objectives of ITS accuracy evaluation: (1) determine the accuracy of tree detection, including the number and location of trees (point accuracy); (2) determine the quality of tree crown delineation, i.e., the boundary of tree crowns (boundary accuracy).

For individual tree segmentation, the accuracy might include measures of commission (tree detected by algorithm does not exist on the ground) and omission (reference tree is not detected by the algorithm) errors.

1. GT data matching
2. Evaluation

**Evaluation based on instance detection:**
*   "How many trees did the algorithm identify?"
*   "Were there any omissions (missed detections) or false positives (over-detections)?"
    **Suitable application scenarios:** Forest resource inventory, tree counting.

**Evaluation based on point-level segmentation:**
*   "How accurate is the segmentation for each individual tree?"
*   "Are the crown boundaries clearly defined?"
    **Suitable application scenarios:** Canopy structure analysis, biomass estimation, radiative transfer modeling.

#### Point Accuracy
- ```Point-wise``` Intersection over union (IoU) metric based.
    - Index: $IoU$, $Precision$, $Recall$, $F1 Score$, $Coverage$
- ```Tree-instance-wise``` Tree position, height based.
    - Index: Tree instance level $Precision$, $Recall$, $F1 Score$
- ```Plot-level-instance``` The Number of instances.
    - Index: Plot level linear regression analysis of correlation.

#### Boundary Accuracy
- ```Polygon Wise``` The crown matched with the ground truth crown polygon.
    - Index: Tree instance $Precision$, $Recall$, $F1 Score$
- ```Tree Crown Wise``` Per crown root-mean-square error (RMSE) of crown width measurements.
    - Index: $RMSE$



## Individual Tree Component Segmentation
Segment tree stem, branch points.

- ```2015``` &#9733; Detection of fallen trees in ALS point clouds using a Normalized Cut approach trained by simulation ```ISPRS J``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0924271615000271)

- ```2018``` Filtering Stems and Branches from Terrestrial Laser Scanning Point Clouds Using Deep 3-D Fully Convolutional Networks ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/10/8/1215)

- ```2021``` Forest Structural Complexity Tool—An Open Source, Fully-Automated Tool for Measuring Forest Point Clouds ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/13/22/4677)

- ```2021``` Sensor Agnostic Semantic Segmentation of Structurally Diverse and Complex Forest Point Clouds Using Deep Learning ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/13/8/1413) [```data TLS```](http://www.auscover.org.au)

- ```2022``` Semantic segmentation of point cloud data using raw laser scanner measurements and deep neural networks ```ISPRS J```[```paper```](https://www.sciencedirect.com/science/article/pii/S2667393221000119?via%3Dihub)

- ```2023``` LWSNet: A Point-Based Segmentation Network for Leaf-Wood Separation of Individual Trees ```Forests``` [```paper```](https://www.mdpi.com/1999-4907/14/7/1303#Abstract)


## Individual Tree Parameter Estimation

- ```2003``` Measuring individual tree crown diameter with lidar and assessing its influence on estimating forest volume and biomass ```Canadian Journal of Remote Sensing``` [```paper```](https://www.tandfonline.com/doi/abs/10.5589/m03-027)

- ```2022``` Individual tree detection and estimation of stem attributes with mobile laser scanning along boreal forest roads ```ISPRS J``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0924271622000697?via%3Dihub)

- ```2023``` Tree Segmentation and Parameter Measurement from Point Clouds Using Deep and Handcrafted Features ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/15/4/1086)

## Datasets

### ITS Datasets

3D point cloud datasets for individual tree segmentation

- ```2022``` &#9733; Data for the NeonTreeEvaluation Benchmark ```zenodo``` [```data```](https://zenodo.org/records/5914554)

- ```2022``` &#9733; Individual tree point clouds and tree measurements from multi-platform laser scanning in German forests ```Earth System Science Data``` [```associated paper```](https://essd.copernicus.org/articles/14/2989/2022/essd-14-2989-2022.html) [```data```](https://doi.pangaea.de/10.1594/PANGAEA.942856)

- ```2022``` &#9733; LAUTx - Individual Tree Point Clouds from Austrian forest Inventory plots ```zenodo``` [```data```](https://zenodo.org/records/6560112)

- ```2022``` &#9733; Terrestrial laser scanning data Wytham Woods: individual trees and quantitative structure models (QSMs) ```zenodo``` [```data```](https://zenodo.org/records/7307956)

- ```2023``` &#9733; FOR-instance: a UAV laser scanning benchmark dataset for semantic and instance segmentation of individual trees ```zenodo``` [```data```](https://zenodo.org/records/8287792)

- ```2023``` &#9733; TreeLearn Dataset ```GRO.data``` [```data```](https://data.goettingen-research-online.de/dataset.xhtml?persistentId=doi:10.25625/VPMPID)

- ```2023``` &#9733; UAV laser scanning labelled las data over tropical moist forest classified as leaf or wood points ```zenodo``` [```data```](https://zenodo.org/records/8398853)

- ```2024``` &#9733; Extended version of WYTHAM and LAUTx ```GRO.data``` [```data```](https://data.goettingen-research-online.de/dataset.xhtml?persistentId=doi:10.25625/QUTUWU)

- ```2025``` A large dataset of labelled single tree point clouds, QSMs and tree graphs ```Nature  Scientific Data``` [```paper```](https://www.nature.com/articles/s41597-025-06421-7)

- ```2025``` &#9733; Benchmarking individual tree segmentation using multispectral airborne laser scanning data: the FGI-EMIT dataset ```arxiv``` [```associated paper```](https://arxiv.org/abs/2511.00653)

- ```2025``` &#9733; FOR-instanceV2 dataset and pre-trained model in paper entitled "ForestFormer3D: A Unified Framework for End-to-End Segmentation of Forest LiDAR 3D Point Clouds" ```zenodo``` [```data```](https://zenodo.org/records/16742708)

- ```2026``` &#9733; TLS forest instance segmentation benchmark ```zenodo``` [```associated paper```](https://www.sciencedirect.com/science/article/pii/S092427162500423X) [```data```](https://zenodo.org/records/14615493)

- ```2026``` WHU-STree: A multi-modal benchmark dataset for street tree inventory ```ISPRS J``` [```paper```](https://www.sciencedirect.com/science/article/pii/S0924271626000626?via%3Dihub) [```home```](https://github.com/WHU-USI3DV/WHU-STree/?tab=readme-ov-file)


### Synthetic
#### Modeling

- ```Product``` SpeedTree [```website```](https://unity.com/cn/products/speedtree)

- ```2010``` Speed Tree-Based Forest Simulation System ```IEEE``` [```paper```](https://ieeexplore.ieee.org/abstract/document/5631937)

#### Simulation

- ```2016``` HELIOS: A multi-purpose lidar simulation framework for research, planning and training of laser scanning operations with airborne, groundbased mobile and stationary platforms ```ISPRS Ann``` [```paper```](https://isprs-annals.copernicus.org/articles/III-3/161/2016/)

- ```2017``` DART: Recent Advances in Remote Sensing Data Modeling With Atmosphere, Polarization, and Chlorophyll Fluorescence ```IEEE``` [```paper```](https://ieeexplore.ieee.org/abstract/document/7900403)

## Reviews
- ```2011``` &#9733; A review of methods for automatic individual tree-crown detection and delineation from passive remote sensing ```International Journal of Remote Sensing``` [```paper```](https://www.tandfonline.com/doi/full/10.1080/01431161.2010.494184#d1e233)

- ```2016``` &#9733; Trends in Automatic Individual Tree Crown Detection and Delineation—Evolution of LiDAR Data ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/8/4/333)

- ```2023``` Latest Trends on Tree Classification and Segmentation Using UAV Data — A Review of Agroforestry Applications ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/15/9/2263)

- ```2024``` A Review of Semantic Segmentation and Instance Segmentation Techniques in Forestry Using LiDAR and Imagery Data ```Electronics```  [```paper```](https://www.mdpi.com/2079-9292/13/20/4139)

## Comparative Study

- ```2010``` ```Conventional ITS``` Comparative Analysis of Clustering-Based Approaches for 3-D Single Tree Detection Using Airborne Fullwave Lidar Data ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/2/4/968)

- ```2012``` &#9733; ```Conventional ITS``` An International Comparison of Individual Tree Detection and Extraction Using Airborne Laser Scanning ```Remote Sensing``` [```paper```](https://www.mdpi.com/2072-4292/4/4/950)

- ```2026``` &#9733; ```Comprehensive ITS``` Benchmarking tree instance segmentation of terrestrial laser scanning point clouds ```ISPRS J``` [```paper```](https://www.sciencedirect.com/science/article/pii/S092427162500423X) [```data```](https://zenodo.org/records/14615493)

## Citation

If this repository helps your research, please cite:

```bibtex
@misc{wang2026awesome3dforestinventory,
  title        = {Awesome 3D Forest Inventory},
  author       = {WANG-Andy-JH},
  year         = {2026},
  howpublished = {\url{https://github.com/WANG-Andy-JH/Awesome-3D-Forest-Inventory}},
  note         = {GitHub repository}
}
```

If you use specific methods, datasets, or codes listed above, please also cite the original papers.
