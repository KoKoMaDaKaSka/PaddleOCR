
# 简介
PaddleOCR旨在打造一套丰富、领先、且实用的文字检测、识别模型/工具库，助力使用者训练出更好的模型，并应用落地。


## 文档教程
- [快速安装](./doc/installation.md)
- [文本识别模型训练/评估/预测](./doc/detection.md)
- [文本预测模型训练/评估/预测](./doc/recognition.md)

## 特性：
- 超轻量级模型
    - (检测模型4.1M + 识别模型4.5M = 8.6M)
- 支持竖排文字
    - (单模型同时支持横排和竖排文字识别)
- 支持长文本识别
- 支持中英文数字组合识别
- 提供训练代码
- 支持模型部署

## 文本检测算法:

PaddleOCR开源的文本检测算法列表：
- [EAST](https://arxiv.org/abs/1704.03155)
- [DB](https://arxiv.org/abs/1911.08947)
- [SAST](https://arxiv.org/abs/1908.05498)

算法效果：
|模型|骨干网络|数据集|Hmean|
|-|-|-|-|
|EAST|ResNet50_vd|ICDAR2015|85.85%|
|EAST|MobileNetV3|ICDAR2015|79.08%|
|DB|ResNet50_vd|ICDAR2015|83.30%|
|DB|MobileNetV3|ICDAR2015|73.00%|

PaddleOCR文本检测算法的训练与使用请参考[文档](./doc/detection.md)。

## 文本识别算法:

PaddleOCR开源的文本识别算法列表：
- (CRNN)[https://arxiv.org/abs/1507.05717]
- [Rosetta](https://arxiv.org/abs/1910.05085)
- [STAR-Net](http://www.bmva.org/bmvc/2016/papers/paper043/index.html)
- [RARE](https://arxiv.org/abs/1603.03915v1)
- [SRN]((https://arxiv.org/abs/2003.12294))(百度自研)

算法效果如下表所示，精度指标是在IIIT, SVT, IC03, IC13, IC15, SVTP, CUTE数据集上的评测结果的平均值。

|模型|骨干网络|ACC|
|-|-|-|
|Rosetta|Resnet34_vd|80.24%|
|Rosetta|MobileNetV3|78.16%|
|CRNN|Resnet34_vd|82.20%|
|CRNN|MobileNetV3|79.37%|
|STAR-Net|Resnet34_vd|83.93%|
|STAR-Net|MobileNetV3|81.56%|
|RARE|Resnet34_vd|84.90%|
|RARE|MobileNetV3|83.32%|

PaddleOCR文本识别算法的训练与使用请参考[文档](./doc/recognition.md)。

## 端到端算法
PaddleOCR即将开源百度自研端对端OCR模型[End2End-PSL](https://arxiv.org/abs/1909.07808)，敬请关注。
- End2End-PSL (comming soon)



# 参考文献
```
EAST:
@inproceedings{zhou2017east,
  title={EAST: an efficient and accurate scene text detector},
  author={Zhou, Xinyu and Yao, Cong and Wen, He and Wang, Yuzhi and Zhou, Shuchang and He, Weiran and Liang, Jiajun},
  booktitle={Proceedings of the IEEE conference on Computer Vision and Pattern Recognition},
  pages={5551--5560},
  year={2017}
}

DB:
@article{liao2019real,
  title={Real-time Scene Text Detection with Differentiable Binarization},
  author={Liao, Minghui and Wan, Zhaoyi and Yao, Cong and Chen, Kai and Bai, Xiang},
  journal={arXiv preprint arXiv:1911.08947},
  year={2019}
}

DTRB:
@inproceedings{baek2019wrong,
  title={What is wrong with scene text recognition model comparisons? dataset and model analysis},
  author={Baek, Jeonghun and Kim, Geewook and Lee, Junyeop and Park, Sungrae and Han, Dongyoon and Yun, Sangdoo and Oh, Seong Joon and Lee, Hwalsuk},
  booktitle={Proceedings of the IEEE International Conference on Computer Vision},
  pages={4715--4723},
  year={2019}
}

SAST:
@inproceedings{wang2019single,
  title={A Single-Shot Arbitrarily-Shaped Text Detector based on Context Attended Multi-Task Learning},
  author={Wang, Pengfei and Zhang, Chengquan and Qi, Fei and Huang, Zuming and En, Mengyi and Han, Junyu and Liu, Jingtuo and Ding, Errui and Shi, Guangming},
  booktitle={Proceedings of the 27th ACM International Conference on Multimedia},
  pages={1277--1285},
  year={2019}
}

SRN:
@article{yu2020towards,
  title={Towards Accurate Scene Text Recognition with Semantic Reasoning Networks},
  author={Yu, Deli and Li, Xuan and Zhang, Chengquan and Han, Junyu and Liu, Jingtuo and Ding, Errui},
  journal={arXiv preprint arXiv:2003.12294},
  year={2020}
}

end2end-psl:
@inproceedings{sun2019chinese,
  title={Chinese Street View Text: Large-scale Chinese Text Reading with Partially Supervised Learning},
  author={Sun, Yipeng and Liu, Jiaming and Liu, Wei and Han, Junyu and Ding, Errui and Liu, Jingtuo},
  booktitle={Proceedings of the IEEE International Conference on Computer Vision},
  pages={9086--9095},
  year={2019}
}
```
