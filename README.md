# README 




# Project Name

By [Stavros Kalaouzis](https://github.com/skalaouzis).

Paper: [name, name, name., "paper name", resource:number (2016)](http://www.google.com).

## Information

bla bla

0. The experiments have been conducted with the beta-20 version of [MatConvNet](https://github.com/vlfeat/matconvnet), which is included in the current project.

0. In this version of  [MatConvNet](https://github.com/vlfeat/matconvnet), *the momentum is stored* at the end of every epoch.

0. The code has been evaluated on CIFAR-10 and CIFAR-100 for depth 164. 

0. Sample architecture for a resnet created with a `depth` of 38 can be [found here](https://github.com/bazilas/matconvnet-ResNet/blob/master/sample-resnet-depth38.pdf).

## Usage

0. Compile [MatConvNet](https://github.com/vlfeat/matconvnet) from the *matconvnet* folder.
0. Execute the cnn_cifar() from the *cifar* folder (the parametrization follows below).
0. To train *CIFAR-10* with the *ResNet-164*, execute:
    ```

    cnn_cifar('modelType', 'res', 'depth', 164, 'GPU', 1, 'batchSize', 128,'momentum', 0.95, 'weightDecay', 0.0001, 'Nclass', 10, 'learningRate', [0.01*ones(1,3) 0.1*ones(1,80) 0.01*ones(1,10) 0.001*ones(1,30)])
    
    ```
0. To train *CIFAR-100* with the *ResNet-164*, execute:
    ```
    
    cnn_cifar('modelType', 'res', 'depth', 164, 'GPU', 1, 'batchSize', 128,'momentum', 0.95, 'weightDecay', 0.0005, 'Nclass', 100, 'learningRate', [0.01*ones(1,3) 0.1*ones(1,70) 0.01*ones(1,20) 0.001*ones(1,30)])
    
    ```

0.  Explanation for some parameters:
	1. *modelType* (only residual model available, set value to: *res*)
	2. *depth* (nework depth)
	3. *GPU* (index for the GPU to be employed, set it to *[ ]* for CPU training) 
	4. *Nclass* (10 for CIFAR-10 and 100 for CIFAR-100)

0. The ResNet implementation is in the file */cifar/cnn_resnet_preact.m*

## Experiments

Bla bla

|  Dataset  |  Result |
|:---------:|:-------:|
| name.     |  5.98%  |
| name      | 24.07%  |

1.  CIFAR-10 error plot:
![cifar10](https://github.com/bazilas/matconvnet-ResNet/blob/master/cifar10.png "CIFAR-10")
2.  CIFAR-100 Error Plot:
![cifar100](https://github.com/bazilas/matconvnet-ResNet/blob/master/cifar100.png "CIFAR-100")







A template of README best practices to make your README simple to understand and easy to use. 

## Installation

Download to your project directory, add `README.md`, and commit:

```sh
curl -LO http://git.io/Xy0Chg
git add README.md
git commit -m "Use README Boilerplate"
```

## Usage

Replace the contents of `README.md` with your project's:

* Name
* Description
* Installation instructions
* Usage instructions
* Support instructions
* Contributing instructions

Feel free to remove any sections that aren't applicable to your project.

## Support

Please [open an issue](https://github.com/fraction/readme-boilerplate/issues/new) for support.

## Contributing

Please contribute using [Github Flow](https://guides.github.com/introduction/flow/). Create a branch, add commits, and [open a pull request](https://github.com/fraction/readme-boilerplate/compare/).
