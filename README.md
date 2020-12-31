# CAP-Context-Aware-Pruning-for-Semantic-Segmentation

The official repository for paper ''CAP: Context-Aware Pruning for Semantic Segmentation" [paper](https://openaccess.thecvf.com/content/WACV2021/papers/He_CAP_Context-Aware_Pruning_for_Semantic_Segmentation_WACV_2021_paper.pdf)


Results Overviews on Cityscapes:
|          Methods         |      mIoU(%)    |  #Params(M)(%&darr;) |   #FLOPs(G)(%&darr;)  | 
|:-:|:-:|:-:|:-:|
| PSPNet-101-Unpruned      |      78.40      |        70.44    |   556.04    |
| PSPNet-101-FPGM          |      74.84      |  36.09(48.76%&darr;) | 280.68(49.61%&darr;)  |
| PSPNet-101-NS            |      75.70      |  48.47(31.19%&darr;) | 368.03(33.93%&darr;)  |
| PSPNet-101-BN-Scale      |      74.88      |  48.81(30.71%&darr;) | 370.49(33.49%&darr;) |
| **PSPNet-101-Ours-60%**      |      **77.82**     |  **47.84(32.08%&darr;)** | **363.21(34.80%&darr;)**  |
| **PSPNet-101-Ours-70%**      |      **75.27**      |  **39.74(43.58%&darr;)** | **296.25(46.82%&darr;)**  |
|                         |                   |               |              |
| PSPNet-50-Unpruned      |      76.99      |        51.45    |  403.00    |
| PSPNet-50-FPGM          |      74.59      |  27.06(47.40%&darr;) | 207.31(48.56%&darr;)  |
| PSPNet-50-NS            |      73.57      |  23.61(54.11%&darr;) | 199.78(50.43%&darr;)  |
| PSPNet-50-BN-Scale      |      73.85      |  **23.59(54.15%&darr;)** | **199.43(50.51%&darr;)** |
| **PSPNet-50-Ours-60%**      |      **75.59**     |  27.31(46.92%&darr;) | 233.67(42.02%&darr;)  |
| **PSPNet-50-Ours-70%**      |      73.94      |  23.78(53.78%&darr;) | 203.19(49.58%&darr;)  |
|                         |                   |               |              |
| ICNet-Unpruned      |      64.59      |        12.21    |  40.13    |
| ICNet-FPGM          |      62.00      |  6.45(47.18%&darr;) | 22.96(42.79%&darr;)  |
| ICNet-NS            |      60.02      |  6.90(43.49%&darr;) | 22.75(43.31%&darr;)  |
| ICNet-BN-Scale      |      59.68      |  6.96(43.00%&darr;) | 22.82(43.13%&darr;) |
| **ICNet-Ours-60%**      |      **62.38**     |  **5.56(54.46%&darr;)** | **21.16(47.27%&darr;)**  |
|                         |                   |               |              |
| SegNet-Unpruned      |      56.10      |        29.45    |  326.59    |
| SegNet-FPGM          |      51.60      |  15.63(46.92%&darr;) | 100.51(69.22%&darr;)  |
| SegNet-NS            |      56.85      |  11.85(59.76%&darr;) | 188.16(42.39%&darr;)  |
| SegNet-BN-Scale      |      59.95      |  11.92(59.52%&darr;) | **150.47(53.93%&darr;)** |
| **SegNet-Ours-20%**      |      **61.16**     |  **10.76(63.46%&darr;)** | 178.23(45.43%&darr;)  |

Results Overviews on Camvid:
|          Methods         |      mIoU(%)    |  #Params(M)(%&darr;) |   #FLOPs(G)(%&darr;)  | 
|:-:|:-:|:-:|:-:|
| SegNet-Unpruned      |      55.60      |        29.45    |   106.73    |
| SegNet-FPGM          |      52.54      |   15.63(46.92%&darr;) | 32.95(69.13%&darr;)  |
| SegNet-NS            |      54.78      |   12.25(58.40%&darr;) | 47.81(55.20%&darr;)  |
| SegNet-BN-Scale      |      55.73      |   12.50(57.39%&darr;) | 44.54(58.27%&darr;) |
| **SegNet-Ours-20%**      |      **57.12**     |  11.47(61.05%&darr;) |  53.14(50.21%&darr;)  |
| **SegNet-Ours-30%**      |      56.37     |  **6.03(79.52%&darr;)** | **30.01(71.88%&darr;)**  |


