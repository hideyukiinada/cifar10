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
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), skip filter size=3, GAP, d10 + BN, Same conv padding | 2 | 64 | 0.7745 |72.94%| Linux | keras_9 ||
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), skip filter size=3, GAP, d10 + BN, Same conv padding | 100 | 64 | 0.0052 |86.19%| Linux | keras_11 | categorical accuracy during training: 0.9982 |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=9), skip filter size=3, GAP, d10 + BN, Same conv padding | 100 | 64 | 0.0066 |87.13%| Linux | keras_12 |  |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), skip filter size=1, GAP, d10 + BN, Same conv padding | 100 | 64 | 0.0059 |86.84%| Linux | keras_13 |  |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), leakyReLU, skip filter size=1, GAP, d10 + BN, Same conv padding | 100 | 64 | 0.0087 |84.38%| Linux | keras_14 |  |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), skip filter size=1, GAP, d10 + BN, Same conv padding | 100 | 128 | 0.0013 |86.70%| Linux | keras_15 | categorical_accuracy: 0.9996 |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), skip filter size=1, GAP, d10 + BN, Same conv padding, input centered at 0 | 100 | 128 | 0.0029 |85.61%| Linux | keras_16 | categorical_accuracy: 0.9990 |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), skip filter size=1, GAP, d10 + BN, Same conv padding, image augmentation | 2 | 128 | 0.8758 |40.34%| Linux | keras_17 | categorical_accuracy: 0.6917 |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), skip filter size=1, GAP, d10 + BN, Same conv padding, image augmentation | 10 | 128 | 0.3345 |55.13%| Linux | keras_18 | categorical_accuracy: 0.8835 |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), skip filter size=1, GAP, d10 + BN, Same conv padding, image augmentation (no feature centering/std) | 2 | 128 | 0.9000 |57.99%| Linux | keras_19 | categorical_accuracy: 0.6814  |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), skip filter size=1, GAP, d10 + BN, Same conv padding, image augmentation (no feature centering/std) | 10 | 128 | 0.3404 |75.70%| Linux | keras_20 | categorical_accuracy: 0.8831 |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=2), skip filter size=1, GAP, d10 + BN, Same conv padding, image augmentation (no feature centering/std) | 100 | 128 | 0.0212 |91.18%| Linux | keras_21 | categorical_accuracy: 0.9926 |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=18), skip filter size=1, GAP, d10 + BN, Same conv padding, image augmentation (no feature centering/std) | 100 | 128 | 0.0236 |91.57%| Linux | keras_22 | categorical_accuracy: 0.9923  |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=18), skip filter size=1, GAP, d10 + BN, Same conv padding, image augmentation (no feature centering/std) | 200 | 64 | 0.0111 |90.45%| Linux | keras_23 | categorical_accuracy: 0.9966  |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=20), skip filter size=1, GAP, d10 + BN, Same conv padding, image augmentation (no feature centering/std) | 100 | 64 | 0.0501  |91.06%| Linux | keras_24 | categorical_accuracy: 0.9830  |
|k3f64, (resnet f64 block x n + f128 block x n + f256 block x n) (n=10), skip filter size=1, GAP, d10 + BN, Same conv padding, image augmentation (no feature centering/std) | 100 | 128 | 0.0320  |91.93%| Linux | keras_25 | categorical_accuracy: 0.9890  |
|k3f64, (resnet f64 3l-block x n + f128 3l-block x n + f256 3l-block x n) (n=2), skip filter size=1, GAP, d10 + BN, Same conv padding, image augmentation (no feature centering/std) | 2 | 128 | 0.9970 | 55.46%| Linux | keras_26 | categorical_accuracy: 0.6464|
|k3f64, (resnet f64 3l-block x n + f128 3l-block x n + f256 3l-block x n) (n=2), skip filter size=1, GAP, d10 + BN, Same conv padding, image augmentation (no feature centering/std) | 10 | 128 | 0.4199 | 74.51%| Linux | keras_27 | categorical_accuracy: 0.8554|

 k: Kernel size
 f: Number of filters
 d: Dense unit size
 BN: Batch norm added
 GAP: Global Average Pooling

## Machines used
* Mac (OS:10.13.5, RAM: 16 GB, CPU: 2.6 GHz Intel Core i5, Python: 3.6.7) 