# <p align=center>`Histopathology Datasets for Machine Learning`</p>

This is a list of histopathology datasets made public for classification, segmentation, regression and/or registration tasks.

If you find any mistakes, you know of other datasets that are not listed here or anything else, please write an issue.

I hope this list will help some of you.

# Overview
- [Ressources](#ressources)
- [References](#references)

# Ressources

Please find in the table below some link and information about histopathology dataset that are publicly available.

Dataset name | Organs | Staining | Link | Size | Data | Supervised | Task | WSI/Patch | Other (Magnification, Scanner) | year
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |---
ACDC-LungHP [1a], [1b] | Lung | H&E | [link data](https://acdc-lunghp.grand-challenge.org/), [link paper](https://ieeexplore.ieee.org/document/9265237) | Train: 150, Test: 50 | images + xml | yes | seg + classi | wsi | | 2019
ACROBAT 2022 | Breast | IHC + H&E | [link data](https://acrobat.grand-challenge.org/), [link paper](https://openreview.net/pdf?id=5TTocO2VI3r) | Train: 750 train; Valid: 100; Test: 300 | images (1 H&E match to 1-4 IHC) + landmarks | | registration | wsi | 40x - Hamamatsu | 2022
ADP [2] | multiple | multiple (most H&E) | [link data](https://www.dsp.utoronto.ca/projects/ADP/), [link github](https://github.com/mahdihosseini/ADP), [link paper](https://openaccess.thecvf.com/content_CVPR_2019/papers/Hosseini_Atlas_of_Digital_Pathology_A_Generalized_Hierarchical_Histological_Tissue_Type-Annotated_CVPR_2019_paper.pdf) | Train: 14.134, Valid: 1767, Test: 1767 (100 wsi) | images + 57 hierarchical HTTs (histological tissue type) |  | multi-label (3) classification (hierarchy) | patch (1088x1088) | 40x - Huron TissueScope LE1.2 WSI | 2019
ANHIR [3] | different (Lung, Kidney, Colon, Gastric, Breast)| different | [link data](https://anhir.grand-challenge.org/), [link paper](https://ieeexplore.ieee.org/document/9058666) | 50+ sets| image + landmarks |  | registration | patch (15k x 15k to 50k x 50k) | 40x, 20x, 10x, different scanner | 2019
ARCH [4] | different | different | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/arch), [link paper](https://openaccess.thecvf.com/content/CVPR2021/html/Gamper_Multiple_Instance_Captioning_Learning_Representations_From_Histopathology_Textbooks_and_Articles_CVPR_2021_paper.html) | 4270 | images + caption |  | learn representation from text + image | patch | multiple | 2020
BACH - ICIA2018 [5] | Breast | H&E | [link data](https://iciar2018-challenge.grand-challenge.org/Dataset/), [link paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841518307941) | 400 | images (4 classes: normal 100, benign: 100, in situ carcinoma: 100, invasive carcinoma: 100) + 20 unlabeled + 10 labeled WSI (10 patients) | yes and no | classi + seg| Patch (classi, 2048x1536) + WSI (seg) | Leica SCN400 | 2018
BCNB [6] | Breast | | [link data](https://bcnb.grand-challenge.org/), [link paper](https://www.frontiersin.org/articles/10.3389/fonc.2021.759007/full) | 1058 (train 0.6, valid 0.2, test 0.2) | images + roi annotated + patient record | | | wsi | | 2021
BCSS [7] | Breast | H&E | [link data](https://bcsegmentation.grand-challenge.org/), [link paper](https://academic.oup.com/bioinformatics/article/35/18/3461/5307750) | 151 wsi, 20.000 patch| patch + segmentation mask | yes | semantic seg | patch | (TCGA) | 2019
BreakHis [8] | Breast |	H&E	| [link data](https://web.inf.ufpr.br/vri/databases/breast-cancer-histopathological-database-breakhis/), [link paper](https://www.inf.ufpr.br/lesoliveira/download/TBME-00608-2015-R2-preprint.pdf) |	7.909 (2480 benign, 5429 malignant)	| images + binary label + tumor type (8) (different magnifications: 40x, 100x, 200x, 400x) |	yes |	classi |	Patch (700x460) | 40x, 100x, 200x, 400x | 2016
BreCaHAD [9] | Breast | H&E | [link data](https://figshare.com/articles/dataset/BreCaHAD_A_Dataset_for_Breast_Cancer_Histopathological_Annotation_and_Diagnosis/7379186) [link paper](https://bmcresnotes.biomedcentral.com/articles/10.1186/s13104-019-4121-7) | 162 | images + centroid with label | yes | classi (6: mitosis, apoptosis, tumor nuclei, non-tumor nuclei, tubule, non-tubule) | patch (1360x1024) | 40x - Zeiss | 2019
CAMELYON16 [10] | Lymph node | H&E | [link data](https://camelyon16.grand-challenge.org/), [link paper](https://jamanetwork.com/journals/jama/article-abstract/2665774) | Train: 270 (160 Normal, 110 with metastases); Test: 130 | images + binary masks | yes | classi + seg | WSI | slide level analysis | 2016
CAMELYON17 [11] | Lymph node | H&E | [link data](https://camelyon17.grand-challenge.org/), [link paper](https://ieeexplore.ieee.org/document/8447230) | Train: 500 (100 patients, 5 slides each); Test: 500 | images + binary masks | yes | classi + seg | WSI | patient level analysis | 2017
CAMELYON [12] | Breast (Lymph node) | H&E | [link paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6007545/) | 1399 wsi | | | | wsi | | 2017
Cellseg [13] |  |  | [link data](https://neurips22-cellseg.grand-challenge.org/) | | | | instance segmentation | | | 2022
CoNIC 2022 [14] | Colon | H&E | [link data](https://conic-challenge.grand-challenge.org/), [link github](https://github.com/TissueImageAnalytics/CoNIC), [link paper](https://arxiv.org/pdf/2111.14485.pdf) | 4981 patch with 431.913 nuclei of 6 types | image + instance seg mask + classi mask | yes | seg + classi + reg | patch (256x256) | 20x | 2022
CoNSeP - HoVer-Net [15] | Colorectal adenocarcinoma | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/hovernet/), [link paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841519301045?via%3Dihub) | Train: 27 images, Test: 14 images, 24.319 nuclei | images + nuclei (location + class) | yes | instance seg + classi (7: other, inflammatory, healthy epithelial, dysplastic/malignant epithelial, figroblast, muscle, endothelial) | patch (1000x1000) | 40x (UHCW) | 2019
CPM-15 [16] | (2) | H&E | [link data](https://drive.google.com/drive/folders/11ko-GcDsPpA9GBHuCtl_jNzWQl6qY_-I) | 15 (2905 nuclei) | images + nuclei seg + label | yes | seg + classi | patch (400x400, 600x1000) | 20x, 40x (TCGA) | 
CPM-17 [17] | (4) | H&E | [link data](https://drive.google.com/drive/folders/1sJ4nmkif6j4s2FOGj8j6i_Ye7z9w0TfA), [link paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6454006/) | Train: 32, test: 32 (7570 nuclei) | images + nuclei seg + label | yes | seg + classi | patch (500x500 to 600x600) | 20x, 40x (TCGA) | 2019
CRAG - MILD-Net [18] | Colon | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/mildnet/), [link paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841518306030?via%3Dihub) | Train: 173, Valid: 40 | image + segmentation | yes | instance seg | patch (around 1500x1500) | 20x | 2019
CRCHisto [19] | Colon | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/crchistolabelednucleihe/), [link paper](https://ieeexplore.ieee.org/document/7399414) | 100 images, 29.756 nuclei (10 wsi, 9 patients) | images + point nuclei class label | yes (22.444 nuclei) | seg + classi (epithelial, inflammatory, fibroblast, miscellaneous) | patch (500x500) | 20x - Omnyx VL120 (UHCW) | 2016
CRC-TP [20] | CRC | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/crc-tp), [link paper](https://www.sciencedirect.com/science/article/abs/pii/S136184152030061X?via%3Dihub) | 280k patches (from 20 wsi) | images + tissue phenotypes | yes | classi | patch |  | 2020
CryoNuSeg [21] | multiple (10: adrenal gland, larynx, lymph nodes, mediastinum, pancreas, pleura, skin, testes, thymus, and thyroid gland) | H&E | [link data](https://www.kaggle.com/datasets/ipateam/segmentation-of-nuclei-in-cryosectioned-he-images), [link github](https://github.com/masih4/CryoNuSeg), [link paper](https://www.sciencedirect.com/science/article/pii/S0010482521001438) | 8000 nuclei from 30 patches (from 30 wsi) | images + segmentation masks + binary labels | yes | nuclei segmentation | patch (512x512) | 40x (from TCGA) | 2021
DigestPath2019 - signet ring cell [22] | Gastric, Intestine | H&E | [link data](https://digestpath2019.grand-challenge.org/), [link paper](https://arxiv.org/pdf/1907.03954.pdf) | Train: 460, Test: 226 | images + cell bounding boxes | partly yes (Train: 77, test: 27) | cell detection | patch (avg 2kx2k) | 40x | 2019
DigestPath2019 - colonoscopy tissue segment [23] | Colon | H&E | [link data](https://digestpath2019.grand-challenge.org/), [link paper](https://arxiv.org/pdf/1907.03954.pdf) | Train: 660, Test: 212 | images + lesion annotation | seg + classi (benign vs malignant) | partly yes (train: 250, test: 90) | patch (avg 5kx5k) | 20x | 2019
GlaS [24] | Colorectal Cancer | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/glascontest/), [link paper](https://arxiv.org/pdf/1603.00275v2.pdf) | 165 | Train: 85 (37 benign, 48 malignant); Test: 80 (37 benign, 43 malignant) | yes | classi + seg | Patch (diff sizes - few hundred px) | 20x - Zeiss MIRAX MIDI | 2015
Gleason_CNN [25] | Prostate | H&E | [link data](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/OCYCMP), [link github](https://github.com/eiriniar/gleason_CNN), [link paper](https://www.nature.com/articles/s41598-018-30535-1) | 5 tissue microarrays (200-300 spots) | images + patch and pixel annotation | yes | classi | 40x - NanoZoomer-XR Digital slide scanner, Hamamatsu | 2018
Gelasca et al. [26] | Breast | H&E | [link data](https://bioimage.ucsb.edu/research/bio-segmentation) | 50 | images (malignant/benignant, 1.895 nuclei) + masks | yes | classi + seg | Patch (896x768; 768x512) | |
HEROHE - ECDP2020 [27a], [27b] | Breast | H&E | [link data](https://ecdp2020.grand-challenge.org/Home/), [link paper](https://arxiv.org/ftp/arxiv/papers/2111/2111.04738.pdf) | Train: 359 (positive: 144, negatives: 215), Test: 150 (positive: 60, negative: 90) | images + binary label | yes | classi | wsi | 20x - 3D Histech Pannoramic 1000 | 2020
Janowczyk et al. [28] | Breast |  H&E | [link data](http://www.andrewjanowczyk.com/use-case-1-nuclei-segmentation/), [link github](https://github.com/choosehappy/public/tree/master/DL%20tutorial%20Code) | 143 | images (12.000 nuclei) + masks| yes | semantic seg | Patch (2000x2000) | 40x | 2015
Kather et al. [29] | Colon | H&E | [link data](https://zenodo.org/record/1214456#.Yt_SxN_RZhE), [link github](https://github.com/jnkather/deep-stroma-histology/tree/v0.2), [link paper](https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.1002730) | Train: 100k (86 wsi), Valid: 7180 (25 wsi) | image + label (9 tissue type) | yes | classi | patch (224x224) |  | 2018
Kather et al. [30] | Colon | H&E | [link data](https://zenodo.org/record/2530835#.Yt_ZdN_RZhE), [link data](https://zenodo.org/record/2530789#.Yt_Zc9_RZhE), [link data](https://zenodo.org/record/2532612#.Yt_Zdd_RZhE), [link github](https://github.com/jnkather/MSIfromHE), [link paper](https://www.nature.com/articles/s41591-019-0462-y#data-availability) |   |   | no/yes | seg (tumor detection) + classi (MSI detection) |   |  | 2019
Kumar [31] | different (8) | H&E | [link data](https://drive.google.com/drive/folders/1bI3RyshWej9c4YoRW-_q7lh7FOFDFUrJ), [link paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7872382) | Train: 16 (13.372 nuclei), test same organ (4.130 nuclei): 8, test diff organ (4.121 nuclei): 6 | images + nuclei seg + label | yes | seg + classi | patch (1000x1000) | 40x (TCGA) | 2017
Lizard [32] | Colon | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/lizard/), [link paper](https://arxiv.org/pdf/2108.11195.pdf) | 495.179 nuclei | images + instance seg mask | yes | seg | patch | 20x (DigestPath + CRAG + GlaS + PanNuke + CoNSeP + TCGA) | 2021
LYON19 [33] | Multiple (Breast, Colon, Protate) | IHC | [link data](https://lyon19.grand-challenge.org/), [link paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841519300829) | 441 ROIs |  |  |  | patch | | 2019
MIDOG 2021 [34] | Breast | H&E | [link data](https://imig.science/midog2021/the-dataset/), [link paper](https://arxiv.org/pdf/2204.03742.pdf) | 200 wsi: 50 wsi / scanners - 4 scanners | images + roi | | detection of mitotic figues | wsi | | 2021
MIDOG 2022 [35] | different (6 for train 10 for test) | H&E | [link data](https://midog2022.grand-challenge.org/) | Train: 405 cases, 9501 mitotic annotation | images + seg | yes | seg | Patch | | 2022
MoNuSAC 2020 [36] | different (Lung, Prostate, Kidney, Breast) | H&E | [link data](https://monusac-2020.grand-challenge.org/), [link paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9446924) | 31.411 nuclei from 209 images | images + mask | yes | instance seg + classi | patch (81x113 to 1422x2162) | 40x (TCGA) | 2020
MoNuSeg [37a], [37b] | different (7) | H&E | [link data](https://monuseg.grand-challenge.org/Data/), [link github](https://github.com/ruchikaverma-iitg/MoNuSeg), [link paper](https://ieeexplore.ieee.org/document/8880654) | Train: 30, Test: 14 | images (Train: 22.000 nuclei, Test: 7000) + masks| yes | instance seg | Patch (1000x1000) | 40x (from TCGA) | 2018
Naylor et al. [38] | Breast | H&E | [link data](https://zenodo.org/record/2579118#.Yt5FWt_RaUk), [link paper](https://ieeexplore.ieee.org/document/8438559) | 50 | images (4.022 nuclei, 11 patients) + masks | yes | seg | Patch (512x512) | 40x | 2018
NuCLS [39] | Breast | H&E | [link data](https://nucls.grand-challenge.org/), [link paper](https://arxiv.org/ftp/arxiv/papers/2102/2102.09099.pdf) | 220.000 nuclei from 3.944 roi from 125 patients | roi + bounding bx + classification | yes | nuclear detection + classi + seg | patch | (TCGA) | 2021
PAIP2019 [40] | Liver | H&E | [link data](https://paip2019.grand-challenge.org/), [link paper](https://www.sciencedirect.com/science/article/pii/S1361841520302188) | Train: 50, Valid: 10, Test: 40 | images + binary mask | yes | cancer seg | wsi | 20x - Aperio AT2 | 2019
PAIP2020 [41] | Colon | H&E | [link data](https://paip2020.grand-challenge.org/), [link github](https://github.com/wisepaip/paip2020) | Train: 47, Valid: 31, Test: 40 | images + binary mask | yes | cancer seg | wsi | 40x - Aperio AT2 | 2020
PAIP2021 [42] | Multiple (Colon, Prostate, Pancreas) | H&E | [link data](https://paip2021.grand-challenge.org/Rules/), [link paper](https://arxiv.org/ftp/arxiv/papers/2110/2110.12283.pdf) | Train: 150, Valid: 30, Test: 60 | wsi + xml gt | yes/no | semantic seg | wsi | 20x - Aperio AT2 | 2021
The PANDA challenge [43]  | Prostate | H&E | [link data](https://www.kaggle.com/c/prostate-cancer-grade-assessment/data), [link paper](https://www.nature.com/articles/s41591-021-01620-2) | Train: 10.616, Valid: 393, Internal test: 545, External test: 1071 | images + label | yes | classi | wsi | slide level analysis | 2020
PanNuke [44] | multiple (19) | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/pannuke), [link github](https://jgamper.github.io/PanNukeDataset/), [link paper](https://arxiv.org/pdf/2003.10778.pdf), [link paper](https://link.springer.com/chapter/10.1007/978-3-030-23937-4_2) | 189.744 nuclei (from >20k wsi) | images + nuclei (position + classi: neoplastic, connective, non-neoplastic epithelial, dead, inflammatory) | yes | instance seg + classi | patch | 40x | 2019
PatchCamelyon [45]	| Lymph node |	H&E |	[link data](https://patchcamelyon.grand-challenge.org/), [link github](https://github.com/basveeling/pcam) [link paper](https://arxiv.org/pdf/1806.03962.pdf)	| 327.680 |	images + binary label	| yes |	classi |	Patch (96x96) | 10x | 2018
SegPC-2021 [46] | Blood |  | [link data](https://segpc-2021.grand-challenge.org/), [link github](https://github.com/dsciitism/SegPC-2021), [link report](https://ieee-dataport.org/open-access/segpc-2021-segmentation-multiple-myeloma-plasma-cells-microscopic-images) | | | | | | | 2021
SPIE-AAPM_NCI BreastPathQ [47] | Breast | H&E | [link data](https://breastpathq.grand-challenge.org/), [link paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8107263/) | 2579 patch from 96 wsi (64 patients) | images + score | yes | regression | patches | 20x | 2019
TCGA [48] | Multiple | H&E | [link data](https://portal.gdc.cancer.gov/) | > 11k |  |  |  | WSI | 
TIGER [49] | Breast | H&E | [link data](https://tiger.grand-challenge.org/) | | | | | | | 2022
TNBC [50] | Breast | H&E | [link data](https://peterjacknaylor.github.io/data/), [link data](https://drive.google.com/drive/folders/1taB8boGyycjV4X1a2vCIAV9fwMxFSS41), [link paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8438559) | 50 images, 4022 cells (11 patients) | images + nuclei seg + label | yes | seg + classi | patch (512x512) | 40x - Philips Ultra Fast Scanner (Curie Inst.) | 2019
TUPAC16 [51] | Breast | H&E | [link data](https://tupac.grand-challenge.org/), [link paper](https://arxiv.org/ftp/arxiv/papers/1807/1807.08284.pdf) | 500 | images + label | yes (wsi level) | classi | WSI | 40x (from TCGA) | 2019
TUPAC16 - aux [52] | Breast - mitoses| H&E | [link data](https://tupac.grand-challenge.org/) | 73 | images + locations | yes | seg | patch | 40x (from TCGA) Leica SCN400 | 2019
WSSS4LUAD [53] | Lung | H&E | [link data](https://wsss4luad.grand-challenge.org/), [link paper](https://arxiv.org/pdf/2204.06455.pdf) | 87 (Train: 53, valid: 12, Test: 12) | Train: 10.091 patches, Valid: 40 patches, Test: 80 patches; image level for train, pixel level for test/valid | yes | tissue semantic seg | wsi | (67 GDPH, 20 TCGA) | 2021

# References
[1a] Li, Zhang, et al. "Computer-aided diagnosis of lung carcinoma using deep learning-a pilot study." arXiv preprint arXiv:1803.05471 (2018).

[1b] Li, Zhang, et al. "Deep learning methods for lung cancer segmentation in whole-slide histopathology images—the acdc@ lunghp challenge 2019." IEEE Journal of Biomedical and Health Informatics 25.2 (2020): 429-440.

[2] Hosseini, Mahdi S., et al. "Atlas of digital pathology: A generalized hierarchical histological tissue type-annotated database for deep learning." Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2019.

[3] Borovec, Jiří, et al. "ANHIR: automatic non-rigid histological image registration challenge." IEEE transactions on medical imaging 39.10 (2020): 3042-3052.

[4] Gamper, Jevgenij, and Nasir Rajpoot. "Multiple instance captioning: Learning representations from histopathology textbooks and articles." Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2021.

[5] Aresta, Guilherme, et al. "Bach: Grand challenge on breast cancer histology images." Medical image analysis 56 (2019): 122-139.

[6] Xu, Feng, et al. "Predicting axillary lymph node metastasis in early breast cancer using deep learning on primary tumor biopsy slides." Frontiers in oncology 11 (2021): 759007.

[7] Amgad, Mohamed, et al. "Structured crowdsourcing enables convolutional segmentation of histology images." Bioinformatics 35.18 (2019): 3461-3467.

[8] Spanhol, Fabio A., et al. "A dataset for breast cancer histopathological image classification." Ieee transactions on biomedical engineering 63.7 (2015): 1455-1462.

[9] Aksac, Alper, et al. "BreCaHAD: a dataset for breast cancer histopathological annotation and diagnosis." BMC research notes 12.1 (2019): 1-3.

[10] Bejnordi, Babak Ehteshami, et al. "Diagnostic assessment of deep learning algorithms for detection of lymph node metastases in women with breast cancer." Jama 318.22 (2017): 2199-2210.

[11] Bandi, Peter, et al. "From detection of individual metastases to classification of lymph node status at the patient level: the camelyon17 challenge." IEEE transactions on medical imaging 38.2 (2018): 550-560.

[12] Litjens, Geert, et al. "1399 H&E-stained sentinel lymph node sections of breast cancer patients: the CAMELYON dataset." GigaScience 7.6 (2018): giy065.

[13]

[14] Graham, Simon, et al. "Conic: Colon nuclei identification and counting challenge 2022." arXiv preprint arXiv:2111.14485 (2021).

[15] Graham, Simon, et al. "Hover-net: Simultaneous segmentation and classification of nuclei in multi-tissue histology images." Medical Image Analysis 58 (2019): 101563.

[16] Vu, Quoc Dang, et al. "Methods for segmentation and classification of digital microscopy tissue images." Frontiers in bioengineering and biotechnology (2019): 53.

[17] Vu, Quoc Dang, et al. "Methods for segmentation and classification of digital microscopy tissue images." Frontiers in bioengineering and biotechnology (2019): 53.

[18] Graham, Simon, et al. "MILD-Net: Minimal information loss dilated network for gland instance segmentation in colon histology images." Medical image analysis 52 (2019): 199-211.

[19] Sirinukunwattana, Korsuk, et al. "Locality sensitive deep learning for detection and classification of nuclei in routine colon cancer histology images." IEEE transactions on medical imaging 35.5 (2016): 1196-1206.

[20] Javed, Sajid, et al. "Cellular community detection for tissue phenotyping in colorectal cancer histology images." Medical image analysis 63 (2020): 101696.

[21] Mahbod, Amirreza, et al. "CryoNuSeg: A dataset for nuclei instance segmentation of cryosectioned H&E-stained histological images." Computers in biology and medicine 132 (2021): 104349.

[22] Li, Jiahui, et al. "Signet ring cell detection with a semi-supervised learning framework." International conference on information processing in medical imaging. Springer, Cham, 2019.

[23] Li, Jiahui, et al. "Signet ring cell detection with a semi-supervised learning framework." International conference on information processing in medical imaging. Springer, Cham, 2019.

[24] Sirinukunwattana, Korsuk, et al. "Gland segmentation in colon histology images: The glas challenge contest." Medical image analysis 35 (2017): 489-502.

[25] Arvaniti, Eirini, et al. "Automated Gleason grading of prostate cancer tissue microarrays via deep learning." Scientific reports 8.1 (2018): 1-11.

[26]

[27a] Conde-Sousa, Eduardo, et al. "HEROHE Challenge: assessing HER2 status in breast cancer without immunohistochemistry or in situ hybridization." arXiv preprint arXiv:2111.04738 (2021).

[27b] La Barbera, David, et al. "Detection of her2 from haematoxylin-eosin slides through a cascade of deep learning classifiers via multi-instance learning." Journal of Imaging 6.9 (2020): 82.

[28]

[29] Kather, Jakob Nikolas, Halama, Niels, & Marx, Alexander. (2018). 100,000 histological images of human colorectal cancer and healthy tissue (v0.1) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.1214456

[30] Kather, Jakob Nikolas, et al. "Deep learning can predict microsatellite instability directly from histology in gastrointestinal cancer." Nature medicine 25.7 (2019): 1054-1056.

[31] Kumar, Neeraj, et al. "A dataset and a technique for generalized nuclear segmentation for computational pathology." IEEE transactions on medical imaging 36.7 (2017): 1550-1560.

[32] Graham, Simon, et al. "Lizard: a large-scale dataset for colonic nuclear instance segmentation and classification." Proceedings of the IEEE/CVF International Conference on Computer Vision. 2021.

[33] Swiderska-Chadaj, Zaneta, et al. "Learning to detect lymphocytes in immunohistochemistry with deep learning." Medical image analysis 58 (2019): 101547.

[34] Aubreville, Marc, et al. "Mitosis domain generalization in histopathology images--The MIDOG challenge." arXiv preprint arXiv:2204.03742 (2022).

[35]

[36] Verma, Ruchika, et al. "MoNuSAC2020: A multi-organ nuclei segmentation and classification challenge." IEEE Transactions on Medical Imaging 40.12 (2021): 3413-3423.

[37a] Kumar, Neeraj, et al. "A multi-organ nucleus segmentation challenge." IEEE transactions on medical imaging 39.5 (2019): 1380-1391.

[37b] Kumar, Neeraj, et al. "A dataset and a technique for generalized nuclear segmentation for computational pathology." IEEE transactions on medical imaging 36.7 (2017): 1550-1560.

[38]

[39]

[40]

[41]

[42]

[43]

[44]

[45]

[46]

[47]

[48]

[49]

[50]

[51]

[52]

[53]

# Author
Marie Duc - PhD Student

email: marie.duc@med.uni-tuebingen.de
