# MNIST-to-SVHN and SVHN-to-MNIST

PyTorch Implementation of [CycleGAN](https://arxiv.org/pdf/1703.10593.pdf) and [Semi-Supervised GAN](https://arxiv.org/abs/1606.01583) for Domain Transfer.

## Prerequites
* [Python 3.5](https://www.continuum.io/downloads)
* [PyTorch 0.1.12](http://pytorch.org/)

## Potential bugs

### The python code does not fully use the GPU when it is running,
### potential misoptimization with cuda() is suspected
### any help would be grateful
<br>

## Usage

### For Visual Studio
#### Clone the repository

https://visualstudio.github.com/
https://docs.microsoft.com/en-us/visualstudio/python/quickstart-03-python-in-visual-studio-project-from-repository?view=vs-2019
```
Click View -> Team Viewer and Connect to Github
Clone repository
```
#### Download svhm data
$C:\Users\User\source\repos\project_name\mnist-svhn-transfer\
create new folders mnist and svhn
```
http://ufldl.stanford.edu/housenumbers/train_32x32.mat
http://ufldl.stanford.edu/housenumbers/test_32x32.mat
http://ufldl.stanford.edu/housenumbers/extra_32x32.mat
```
and copy them to the svhn folder
#### Execute code
```
cd source/repos/project_name/mnist-svhn-transfer
python main.py --use_labels=False --use_reconst_loss=True
```

### For Linux or Mac users
#### Clone the repository

```bash
$ git clone https://github.com/yunjey/mnist-svhn-transfer.git
$ cd mnist-svhn-transfer/
```

#### Download the dataset
```bash
$ chmod +x download.sh
$ ./download.sh
```

#### Train the model

##### 1) CycleGAN
```bash
$ python main.py --use_labels=False --use_reconst_loss=True
```

##### 2) SGAN

```bash
$ python main.py --use_labels=True --use_reconst_loss=False
```
<br>

## Results

#### 1) CycleGAN (should be re-uploaded)

From SVHN to MNIST            |  From MNIST to SVHN
:-------------------------:|:-------------------------:
![alt text](gif/cycle-s-m.gif)  |  ![alt text](gif/cycle-m-s.gif)
![alt text](gif/cycle-s-m.png)  |  ![alt text](gif/cycle-m-s.png)

#### 2) SGAN
From SVHN to MNIST            |  From MNIST to SVHN
:-------------------------:|:-------------------------:
![alt text](gif/sgan-s-m.gif)  |  ![alt text](gif/sgan-m-s.gif)
![alt text](gif/sgan-s-m.png)  |  ![alt text](gif/sgan-m-s.png)



