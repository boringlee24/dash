# DASH

DASH performs deep learning training job scheduling on heterogeneous GPU types in a cluster

## Hardware setup

16 NVIDIA TESLA K80 GPUs

8 NVIDIA TESLA V100 GPUs

## Software environment

* Python 3.6
* Tensorflow 1.14
* CUDA 10.0

## Benchmarking training models and dataset

1. DenseNet: [link](https://keras.io/api/applications/densenet/)
2. ResNet: [link](https://keras.io/api/applications/resnet/)
3. VGG: [link](https://keras.io/api/applications/vgg/)
4. MobileNet: [link](https://keras.io/api/applications/mobilenet/)
5. MnasNet: [link](https://keras.io/api/applications/nasnet/)

CIFAR10 dataset: [link](https://keras.io/api/datasets/cifar10/)

## Start DASH

Go to directory ```final/final4_new/```.

First allocate an external node (or scheduler node) for tcp client

On each node with the GPUs, start the tcp server by
```shell
python gpu_server.py args
```

Go to the external node, start DASH scheduling on the benchmark
```shell
python main.py args
```
