# Accuracy chart

Dataset: CIFAR10

## Size of dataset

Type|Size|
|---|---|
|Training dataset| 50000|
|Test dataset| 10000|
|Total | 60000|

Image size: 32x32

|Type|Epoch|Batch size | Loss|Test Accuracy | Machine used | File name |Note|
|---|---|---|---|---|---|---|---|
|k3f8, k3f128, d128, d10, Valid conv padding | 2 | 64 | 1.0543 | 63.89% | Mac | keras_baseline ||
|k3f8, k3f128, d128, d10, Valid conv padding | 10 | 64 | 0.4196 | 69.21% | Mac | keras_2 ||
|k3f8, k3f128, d128, d10 + BN, Valid conv padding | 10 | 64 | 0.6458 |67.25%| Mac | keras_3 ||
|k3f64x3, k3f128x3, d128, d10 + BN, Valid conv padding | 10 | 64 | 0.1787 |76.84%| Mac | keras_4 ||
|k3f64x3, k3f128x3, d128, d10 + BN, Valid conv padding | 10 | 64 | 0.1864 |76.69%| Linux | keras_4 ||
|k3f64x3, k3f128x3, k3f256x3, d128, d10 + BN, Valid conv padding | 10 | 64 | 0.3073 |77.92%| Linux | keras_5 ||
|k3f64x3, k3f128x3, k3f256x3, d128, d10 + BN, Valid conv padding | 100 | 64 | 0.0168 |78.11%| Linux | keras_6 ||
|k3f64x3, k3f128x3, k3f256x3, GAP, d10 + BN, Valid conv padding | 10 | 64 | 0.2777 |78.54%| Linux | keras_7 |
|k3f64x3, k3f128x3, k3f256x3, GAP, d10 + BN, Valid conv padding | 200 | 64 | 0.0058|79.57%| Linux | keras_8 ||
|k3f64x3, k3f128x3, k3f256x3, GAP, d10 + BN, Same conv padding | 10 | 64 | 0.2647 |72.22%| Linux | keras_10 ||
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), GAP, d10 + BN, Same conv padding | 2 | 64 | 0.7745 |72.94%| Linux | keras_9 ||
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), GAP, d10 + BN, Same conv padding | 100 | 64 | 0.0052 |86.19%| Linux | keras_11 | categorical accuracy during training: 0.9982 |

 k: Kernel size
 f: Number of filters
 d: Dense unit size
 BN: Batch norm added
 GAP: Global Average Pooling

## Machines used
* Mac (OS:10.13.5, RAM: 16 GB, CPU: 2.6 GHz Intel Core i5, Python: 3.6.7) 