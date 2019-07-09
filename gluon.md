# d2l-zh
```
https://github.com/d2l-ai/d2l-zh
http://zh.d2l.ai/chapter_prerequisite/install.html
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple

```
remote

```sh
nvidia-smi
nvcc -V
sudo pgyvpn
ssh zhangchi@172.22.129.124

mkdir d2l-zh && cd d2l-zh
curl https://zh.d2l.ai/d2l-zh-1.0.zip -o d2l-zh.zip
unzip d2l-zh.zip && rm d2l-zh.zip
conda env create -f environment.yml
# conda env update -f environment.yml
conda activate gluon
set MXNET_GLUON_REPO=https://apache-mxnet.s3.cn-north-1.amazonaws.com.cn/ jupyter notebook --ip 172.22.129.124

```
## GPU

```bash
nvcc -V # cuda 9.1 准备升级成10.0
nvidia-smi
dpkg -l | grep -i nvidia
sudo apt-get remove --purge '^nvidia-.*'
sudo apt autoremove
sudo apt-get install ubuntu-desktop
echo 'nouveau' | sudo tee -a /etc/modules
sudo rm /etc/X11/xorg.conf
sudo reboot

sudo apt-get --purge remove  cuda  


# 430
wget http://cn.download.nvidia.com/XFree86/Linux-x86_64/430.26/NVIDIA-Linux-x86_64-430.26.run
sudo sh NVIDIA-Linux-x86_64-430.26.run

# cuda 10
nohup wget https://developer.nvidia.com/compute/cuda/10.0/Prod/local_installers/cuda_10.0.130_410.48_linux &
wget http://developer.download.nvidia.com/compute/cuda/10.0/Prod/patches/1/cuda_10.0.130.1_linux.run
sudo sh cuda_10.0.130_410.48_linux
sudo sh cuda_10.0.130.1_linux.run
# ubuntu-drivers devices
# sudo ubuntu-drivers autoinstall # sudo apt install nvidia-driver-410/ 430

```