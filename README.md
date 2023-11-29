## Glimpse
This is the description of the data sets.

## The sources of the raw proteomic data sets
We collected the global proteomic data sets of 12 cancer types from the National Cancer Institute’s Proteomic Data Commons (PDC) [<sup>1</sup>](#1). Among these, there are ten cancer cohorts from Clinical Proteomic Tumor Analysis Consortium (CPTAC) program, including Lung Squamous Cell Carcinoma (LSCC)[<sup>2</sup>](#2), Pancreatic Ductal Adenocarcinoma (PDAC)[<sup>3</sup>](#3), Glioblastoma (GBM)[<sup>4</sup>](#4), Ovarian Serous Cystadenocarcinoma (OV)[<sup>5</sup>](#5), Lung Adenocarcinoma (LUAD)[<sup>6</sup>](#6), Head and Neck Squamous Cell Carcinoma (HNSCC)[<sup>7</sup>](#7), Uterine Corpus Endometrial Carcinoma (UCEC)[<sup>8</sup>](#8), Breast Invasive Carcinoma (BRCA)[<sup>9</sup>](#9), Clear Cell Renal Cell Carcinoma (CCRCC)[<sup>10</sup>](#10), and Colon Adenocarcinoma (COAD)[<sup>11</sup>](#11). The other two cancer cohorts, Hepatitis B virus (HBV)-related Hepatocellular Carcinoma (HCC)[<sup>12</sup>](#12) and Early Onset Gastric Cancer (EOGC)[<sup>13</sup>](#13), are from International Cancer Proteogenome Consortium (ICPC). Tumor samples and paired normal adjacent tissue (NAT) were collected in ten cancer cohorts, while the normal samples of Ovarian Serous Cystadenocarcinoma (OV) and Glioblastoma (GBM) cohorts are not paired with tumor samples ([see table below](#tab1)).

<span id="tab1">![Table](/Table1.png)</span>

## Data preprocessing
The datasets we collected from the above studies have been normalised and the methodology can be found in the references given at the end of the 'README' as well as in the description of the corresponding studies provided by PDC. Given the nature of mass spectrometry, it is common to encounter a significant proportion of missing values in the generated data, which will affect downstream analyses. Therefore, proteins with missing expression values in over 50% of the samples were disregarded. For the remaining proteins that still had missing values within the samples, DreamAI was used to fill in the gaps. It is a robust imputation algorithm specifically tailored for proteomics data using crowd learning, consisting of an ensemble of six distinct imputation methods. For more detailed information of the datasets, you can refer to the link.

## Dataset composition
The datasets consist of 12 folders, each representing one cancer type of data. Except for EOGC, each cancer type contains proteomics profiles for normal and tumour samples separately. Each row represents a protein and each column represents a sample.The original study of EOGC did not provide proteomics profiles for normal and tumour samples separately, so the dataset only has the log2-fold-change between paired tumor and adjacent normal tissues.


## References
1. <span id="1">Thangudu RR, Rudnick PA, Holck M, Singhal D, MacCoss MJ, Edwards NJ, et al. Abstract LB-242: Proteomic Data Commons: A resource for proteogenomic analysis. Cancer Res. 2020;80(16_Supplement):LB-242.</span>
 
2. <span id="2">Satpathy S, Krug K, Beltran PMJ, Savage SR, Petralia F, Kumar-Sinha C, et al. A proteogenomic portrait of lung squamous cell carcinoma. Cell. 2021;184(16):4348–71.</span>
3. <span id="3">Cao L, Huang C, Zhou DC, Hu Y, Lih TM, Savage SR, et al. Proteogenomic characterization of pancreatic ductal adenocarcinoma. Cell. 2021;184(19):5031–52.</span>
4.  <span id="4">Wang LB, Karpova A, Gritsenko MA, Kyle JE, Cao S, Li Y, et al. Proteogenomic and metabolomic characterization of human glioblastoma. Cancer Cell. 2021;39(4):509–28.</span>
5. <span id="5">Hu Y, Pan J, Shah P, Ao M, Thomas SN, Liu Y, et al. Integrated proteomic and glycoproteomic characterization of human high-grade serous ovarian carcinoma. Cell Rep. 2020;33(3):108276.</span>
6. <span id="6">Gillette MA, Satpathy S, Cao S, Dhanasekaran SM, Vasaikar SV, Krug K, et al. Proteogenomic characterization reveals therapeutic vulnerabilities in lung adenocarcinoma. Cell. 2020;182(1):200–25.</span>
7.  <span id="7">Huang C, Chen L, Savage SR, Eguez RV, Dou Y, Li Y, et al. Proteogenomic insights into the biology and treatment of HPV-negative head and neck squamous cell carcinoma. Cancer Cell. 2021;39(3):361–79.</span>
8.  <span id="8">Dou Y, Kawaler EA, Zhou DC, Gritsenko MA, Huang C, Blumenberg L, et al. Proteogenomic characterization of endometrial carcinoma. Cell. 2020;180(4):729–48.</span>
9. <span id="9">Krug K, Jaehnig EJ, Satpathy S, Blumenberg L, Karpova A, Anurag M, et al. Proteogenomic landscape of breast cancer tumorigenesis and targeted therapy. Cell. 2020;183(5):1436–56.</span>
10. <span id="10">Clark DJ, Dhanasekaran SM, Petralia F, Pan J, Song X, Hu Y, et al. Integrated proteogenomic characterization of clear cell renal cell carcinoma. Cell. 2019;179(4):964–83.</span>
11. <span id="11">Vasaikar S, Huang C, Wang X, Petyuk VA, Savage SR, Wen B, et al. Proteogenomic analysis of human colon cancer reveals new therapeutic opportunities. Cell. 2019;177(4):1035–49.</span>
12. <span id="12">Gao Q, Zhu H, Dong L, Shi W, Chen R, Song Z, et al. Integrated proteogenomic characterization of HBV-related hepatocellular carcinoma. Cell. 2019;179(2):561–77.</span>
13. <span id="13">Mun DG, Bhin J, Kim S, Kim H, Jung JH, Jung Y, et al. Proteogenomic characterization of human early-onset gastric cancer. Cancer Cell. 2019;35(1):111–24.</span>
