# CAP-Context-Aware-Pruning-for-Semantic-Segmentation

[![996.ICU](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu) ![GitHub](https://img.shields.io/github/license/erichhhhho/CAP-Context-Aware-Pruning-for-Semantic-Segmentation.svg) ![](https://img.shields.io/badge/dynamic/json?color=000000&label=GitHub&query=%24.data.totalSubs&suffix=followers&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dgithub%26queryKey%3Derichhhhho)

The official repository for paper ''CAP: Context-Aware Pruning for Semantic Segmentation" by [Wei He](https://github.com/erichhhhho), Meiqing Wu, [Mingfu Liang](https://wuyujack.github.io/), [Siew-Kei Lam](https://siewkeilam.github.io/ei-research-group/contact.html). School of Computer Science and Engineering, Nanyang Technological University.
<br>[[paper]](https://openaccess.thecvf.com/content/WACV2021/papers/He_CAP_Context-Aware_Pruning_for_Semantic_Segmentation_WACV_2021_paper.pdf) [[supplementary]](https://openaccess.thecvf.com/content/WACV2021/supplemental/He_CAP_Context-Aware_Pruning_WACV_2021_supplemental.pdf) [[video]](https://www.youtube.com/watch?v=fKvswyyxkuw&t=5s) [[underline]](https://underline.io/lecture/8730-510---cap-context-aware-pruning-for-semantic-segmentation) 
## Abstract
Network pruning for deep convolutional neural networks (CNNs) has recently achieved notable research progress on image-level classification. However, most existing pruning methods are not catered to or evaluated on semantic segmentation networks. In this paper, we advocate the importance of contextual information during channel pruning for semantic segmentation networks by presenting a novel Context-aware Pruning framework. Concretely, we formulate the embedded contextual information by leveraging the layer-wise channels interdependency via the Context-aware Guiding Module (CAGM) and introduce the Context-aware Guided Sparsification (CAGS) to adaptively identify the informative channels on the cumbersome model by inducing channel-wise sparsity on the scaling factors in batch normalization (BN) layers. The resulting pruned models require significantly lesser operations for inference while maintaining comparable performance to (at times outperforming) the original models. We evaluated our framework on widely-used benchmarks and showed its effectiveness on both large and lightweight models. On Cityscapes dataset, our framework reduces the number of parameters by 32%, 47%, 54%, and 63%, on PSPNet101, PSPNet50, ICNet, and SegNet, respectively, while preserving the performance.

<p align="center">
  <img src="https://github.com/erichhhhho/CAP-Context-Aware-Pruning-for-Semantic-Segmentation/blob/main/CAG(Base).png" width = "630" height = "340">
</p>

<p align="center">
  <img src="https://github.com/erichhhhho/CAP-Context-Aware-Pruning-for-Semantic-Segmentation/blob/main/CAG(PPM).png" width = "630" height = "340">
</p>

## Requirement
* Python 3.6.4 and [PyTorch 0.4.1](http://pytorch.org/)

## Results
Results Overviews on Cityscapes:
|          Methods         |      mIoU(%)    |  #Params(M)(%&darr;) |   #FLOPs(G)(%&darr;)  | 
|:-:|:-:|:-:|:-:|
| PSPNet-101-Unpruned      |      78.40      |        70.44    |   556.04    |
| [PSPNet-101-FPGM](https://www.cityscapes-dataset.com/anonymous-results/?id=27515b64297787f0b3d927de6461b0aaf9fd7438171a30133672ac07150d6960)         |      74.84      |  36.09(48.76%&darr;) | 280.68(49.61%&darr;)  |
| [PSPNet-101-NS](https://www.cityscapes-dataset.com/anonymous-results/?id=db189ec0c5f213d26ee0ecaaa8504b2c5cc56bfde597c5be867dd3102a319b06)            |      75.70      |  48.47(31.19%&darr;) | 368.03(33.93%&darr;)  |
| [PSPNet-101-BN-Scale](https://www.cityscapes-dataset.com/anonymous-results/?id=93df0c9677854e784c0626ebe14764d739e83f3fb7a4cedcde5f8d65bbe5a7f5)      |      74.88      |  48.81(30.71%&darr;) | 370.49(33.49%&darr;) |
| [**PSPNet-101-Ours-60%**](https://www.cityscapes-dataset.com/anonymous-results/?id=ef41363b3017122964012f6f9e092ac4408fa15100faa2734c2b29c71bca44f0)      |      **77.82**     |  **47.84(32.08%&darr;)** | **363.21(34.80%&darr;)**  |
| [**PSPNet-101-Ours-70%**](https://www.cityscapes-dataset.com/anonymous-results/?id=39771db3aec6d4b278de1ddb788fd79a7d0105e31b7c91557ee57c2cf5050eff)      |      **75.27**      |  **39.74(43.58%&darr;)** | **296.25(46.82%&darr;)**  |
|                         |                   |               |              |
| [PSPNet-50-Unpruned](https://www.cityscapes-dataset.com/anonymous-results/?id=3ac0ae788e1503987ed88b11ad84938dc9aa2b23b0930e88eb9134fcd72d4ead)      |      76.99      |        51.45    |  403.00    |
| [PSPNet-50-FPGM](https://www.cityscapes-dataset.com/anonymous-results/?id=4b58532e1e350ae450051ae2a37e7b2139de37b385f867b7f28ccdfb8b9b5596)          |      74.59      |  27.06(47.40%&darr;) | 207.31(48.56%&darr;)  |
| [PSPNet-50-NS](https://www.cityscapes-dataset.com/anonymous-results/?id=e9fc4f4575abf22204146e7266940f79da226f236d09956f19795ea707d20bb0)            |      73.57      |  23.61(54.11%&darr;) | 199.78(50.43%&darr;)  |
| [PSPNet-50-BN-Scale](https://www.cityscapes-dataset.com/anonymous-results/?id=3a38de8aa38130b2766259fdcbe91a569595142fa636bf6ceb22ea181107d938)      |      73.85      |  **23.59(54.15%&darr;)** | **199.43(50.51%&darr;)** |
| [**PSPNet-50-Ours-60%**](https://www.cityscapes-dataset.com/anonymous-results/?id=4aa50dae2b87134983242fec4bf0b6f94d97f9b6215c16888cd3894311c87fd3)      |      **75.59**     |  27.31(46.92%&darr;) | 233.67(42.02%&darr;)  |
| [**PSPNet-50-Ours-70%**](https://www.cityscapes-dataset.com/anonymous-results/?id=0e9f79ed64a66e535a52e0ef8fc94a1b5d0a6944d4788be9b51902e0fe64660a)      |      73.94      |  23.78(53.78%&darr;) | 203.19(49.58%&darr;)  |
|                         |                   |               |              |
| [ICNet-Unpruned](https://www.cityscapes-dataset.com/anonymous-results/?id=f151111a5955f1f81ac40afb83d7f94c738b3fcd685997103b3feb3689be633e)      |      64.59      |        12.21    |  40.13    |
| [ICNet-FPGM](https://www.cityscapes-dataset.com/anonymous-results/?id=470f748e24e6cd285d474eddc5863edcc2302a7402aef588155b5b865ba1736a)          |      62.00      |  6.45(47.18%&darr;) | 22.96(42.79%&darr;)  |
| [ICNet-NS](https://www.cityscapes-dataset.com/anonymous-results/?id=469c15a3a018e852c3feba4f96312c83533ec30e1af8c2a34736bfde675a963d)            |      60.02      |  6.90(43.49%&darr;) | 22.75(43.31%&darr;)  |
| [ICNet-BN-Scale](https://www.cityscapes-dataset.com/anonymous-results/?id=325df8867f134550bb4842e4a0873c24928352489169f43b19e49b8cba5f6776)      |      59.68      |  6.96(43.00%&darr;) | 22.82(43.13%&darr;) |
| [**ICNet-Ours-60%**](https://www.cityscapes-dataset.com/anonymous-results/?id=c2cb5914a309a4ca41350459471f66173714d6eff0bbb1a623c02cd27da675ed)      |      **62.38**     |  **5.56(54.46%&darr;)** | **21.16(47.27%&darr;)**  |
|                         |                   |               |              |
| SegNet-Unpruned      |      56.10      |        29.45    |  326.59    |
| [SegNet-FPGM](https://www.cityscapes-dataset.com/anonymous-results/?id=5edc3d5fd293ae7231636867880ffabb42d631ecbc44093fbcf8c2cccea804ae)          |      51.60      |  15.63(46.92%&darr;) | 100.51(69.22%&darr;)  |
| [SegNet-NS](https://www.cityscapes-dataset.com/anonymous-results/?id=aaac27587147394582bc2bd766de4f431eaa14c3cde03cfeff194ec8ce145a30)            |      56.85      |  11.85(59.76%&darr;) | 188.16(42.39%&darr;)  |
| [SegNet-BN-Scale](https://www.cityscapes-dataset.com/anonymous-results/?id=01e0779ab87011540a7e4305842c765b5974d0f9b591721b45b8873734604fb4)      |      59.95      |  11.92(59.52%&darr;) | **150.47(53.93%&darr;)** |
| [**SegNet-Ours-20%**](https://www.cityscapes-dataset.com/anonymous-results/?id=e90072c504efacbaf31ac75716cbe71d51e15c76f99f93524c31b9826418b705)      |      **61.16**     |  **10.76(63.46%&darr;)** | 178.23(45.43%&darr;)  |

Results Overviews on Camvid:
|          Methods         |      mIoU(%)    |  #Params(M)(%&darr;) |   #FLOPs(G)(%&darr;)  | 
|:-:|:-:|:-:|:-:|
| SegNet-Unpruned      |      55.60      |        29.45    |   106.73    |
| SegNet-FPGM          |      52.54      |   15.63(46.92%&darr;) | 32.95(69.13%&darr;)  |
| SegNet-NS            |      54.78      |   12.25(58.40%&darr;) | 47.81(55.20%&darr;)  |
| SegNet-BN-Scale      |      55.73      |   12.50(57.39%&darr;) | 44.54(58.27%&darr;) |
| **SegNet-Ours-20%**      |      **57.12**     |  11.47(61.05%&darr;) |  53.14(50.21%&darr;)  |
| **SegNet-Ours-30%**      |      56.37     |  **6.03(79.52%&darr;)** | **30.01(71.88%&darr;)**  |


## Citation
If you find this project is useful for your research, please cite:
```
@InProceedings{He_2021_WACV,
    author    = {He, Wei and Wu, Meiqing and Liang, Mingfu and Lam, Siew-Kei},
    title     = {CAP: Context-Aware Pruning for Semantic Segmentation},
    booktitle = {Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)},
    month     = {January},
    year      = {2021},
    pages     = {960-969}
}
```
