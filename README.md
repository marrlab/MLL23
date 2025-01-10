# MLL23: A large publicly available single-cell peripheral blood dataset for domain generalized hematological disease diagnostics

## 1) Description:

The MLL23 dataset is a fully labeled peripheral blood single-cell dataset for detecting hematological diseases like acute myeloid leukemia. 
The data acquisition process was performed by the Munich Leukemia Laboratory. The resulting 41,906 images of single nucleated cells comprise 288 x 288 pixels and 25μm x 25μm, corresponding to a resolution of 11.52 pixels per μm. 
Next, five human expert examiners at the Munich Leukemia Laboratory annotated the images, assigning each single cell to one out of 18 classes. In the group of lymphoid cells, there are mature ‘typical' lymphocytes (number of single-cell images = 5,547) and atypical lymphocytes like plasma cells (1,792), large granular lymphocytes (1,849), reactive lymphocytes (33), hairy cells (3,266) and other neoplastic lymphocytes (180), as well as smudge cells (988). In comparison, the group of myeloid cells is divided into mature cells like band neutrophil granulocytes (716), segmented neutrophil granulocytes (7,187), eosinophil granulocytes (2,456), basophil granulocytes (634), monocytes (2512), and immature cells like myeloblasts (8,619), metamyelocytes (495), promyelocytes (752), myelocytes (752), and atypical promyelocytes (2,039). The cell types occur with specific frequencies in the peripheral blood in healthy and pathological patients. Due to that and the fact that the Munich Leukemia Laboratory focuses specifically on hematologic neoplasias, the dataset is naturally imbalanced with respect to the number of images per class, with, for example, over 8000 myeloblasts, but only 33 reactive lymphocytes.


## 2) Download:

The MLL23 dataset can be downloaded from Zenodo.
The main folder contains 18 subfolders named after the rescpective classes. In these the accordingly labeled images are stored as .tif files.

The file labels_MLL23.csv gives an overview of the class labels and number of images per class for the MLL23 dataset.

## 3) Dataset Harmonization

The jupyter notebook MLL-data-analysis.ipnyb helps in exploring the MLL23 dataset and harmonising it with two furter public peripheral blood single cell datasets for domain generalisation tasks.

For using the jupyter notebook make sure:
1. The packages listed in requirements.txt are installed in your environment
2. To download the Matek19 dataset from: https://doi.org/10.7937/tcia.2019.36f5o9ld
3. To download the Acevedo20 dataset from: https://doi.org/10.1016/j.dib.2020.105474

The notebook will give informations about each dataset and contains an approche to harmonise the class labels of the datasets for further domain generalization tasks.

For all three datasets an overwiew of the labels, harmonised labels and numbers of images for each label is given by: harmonised_labels.csv.

The file labels_unharmonised.csv shows the labels that could not be harmonised and that were therefore not used in domain generalization tasks.


## 4) Domain Generalization

For domain generalization the library https://github.com/marrlab/DomainLab by X. Sun et al. was used.   
