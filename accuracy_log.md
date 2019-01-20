# Accuracy chart

Dataset: CIFAR10

## Size of dataset

Type|Size|
|---|---|
|Training dataset| 50000|
|Test dataset| 10000|
|Total | 60000|

Image size: 32x32

|Type|Epoch|Batch size | Loss|Test Accuracy | Machine used | File name | 
|---|---|---|---|---|---|---|
|Original code | 2 | 64 | 1.0543 | 63.89% | Mac | keras_baseline |
|Original code + more epochs | 10 | 64 | 0.4196 | 69.21% | Mac | keras_2 |
|Batchnorm added | 10 | 64 | 0.6458 |67.25%| Mac | keras_3 |
 
## Machines used
* Mac (OS:10.13.5, RAM: 16 GB, CPU: 2.6 GHz Intel Core i5, Python: 3.6.7) 