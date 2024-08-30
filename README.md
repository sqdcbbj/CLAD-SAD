# CLAD-SAD：A Contrastive Learning Based Apple Detection Algorithm For Sparsely Annotated Dataset
一种基于对比学习的稀疏标注苹果检测算法

## 实验结果
| 方法          | 模型类型 | AP<sub>0.50:0.95</sub> | AP<sub>0.5</sub> | AP<sub>0.75</sub> | AR   |
| ------------- | -------- | ----------------------- | ---------------- | ----------------- | ---- |
| Centernet  | 全监督   | 37.5                    | 64.3             | 38.3              | 47.2 |
| FCOS      | 全监督   | 40.3                    | 61.9             | 45.3              | 51.2 |
| Retinanet | 全监督   | 36.7                    | 60.1             | 40.0              | 46.3 |
| Faster R-CNN | 全监督 | 40.5                    | 66.4             | 46.0              | 47.8 |
| SIOD     | 稀疏监督 | 43.8                    | 69.5             | 47.1              | **51.3** |
| CLAD-SAD      | 稀疏监督 | **44.2**                | **71.0**         | **48.9**          | 50.9 |

## 训练
`cd run`
###
仅使用SPGLG模块

`sh sh plg_resdcn18_train.sh`

仅使用对比学习模块

`sh gcl_resdcn18_train.sh`

整体使用训练

`sh dminer_resdcn18_train.sh`

## 测试（注意修改文件中的模型加载地址）

`sh test_resdcn18.sh`

## 结果可视化

`sh visualize.sh`
