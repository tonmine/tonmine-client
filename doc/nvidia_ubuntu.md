# Ubuntu Nvidia mining client installation

## 1. cuda environment deployment
> If your ubuntu does not have nvidia driver or cuda, you need to run cuda installation    
> [More information](https://developer.nvidia.com/cuda-downloads) about Nvidia dreiver and cuda.

**ubuntu 18.04 cuda installation**
```
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin
sudo mv cuda-ubuntu1804.pin /etc/apt/preferences.d/cuda-repository-pin-600
sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub
sudo add-apt-repository "deb https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/ /"
sudo apt-get update
sudo apt-get -y install cuda
```
> Need to reboot after installation `sudo reboot -f`

**ubuntu 20.04 cuda installation**
```
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-ubuntu2004.pin
sudo mv cuda-ubuntu2004.pin /etc/apt/preferences.d/cuda-repository-pin-600
sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/7fa2af80.pub
sudo add-apt-repository "deb https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/ /"
sudo apt-get update
sudo apt-get -y install cuda
```
> Need to reboot after installation `sudo reboot -f`

## 2. Install opencl environment
```
sudo apt-get update
sudo apt-get upgrade -y python3 python3-pip
sudo apt-get install -y opencl-headers ocl-icd-libopencl1 ocl-icd-opencl-dev clinfo
```

## 3. Download and install the mining client

**for ubuntu 18.04**
```
cd ~
sudo rm -r tonmine*
mkdir tonmine
cd tonmine
wget https://www.dropbox.com/s/2zd1kan056vr2oz/tonmine-hiveosV3.tar.gz
tar zxvf tonmine-hiveosV3.tar.gz
```

**for ubuntu 20.04**
```
comming soon
```

## 4. Start mining

**Mining command description：**

```
bash ~/tonmine/autoStart.sh <User email> <User ton address> <worker id>
```
> * `User email` ：When the `worker id` is not in normal mining. An email will be sent to notify the user.(This function has not been implemented yet, but it must be filled in)
> * `User ton address`：The user needs to enter the user's ton address. (It is strongly recommended that the address needs to complete the activation process)
> * `worker id`：The user can set a different `worker id` for each mining machine. This makes it easier to monitor.


**Sample mining commands：**
```
# If you need background execution tonmine miner. Then you need to enter `screen` here
screen

bash ~/tonmine/autoStart.sh tonmine@gmail.com EQCk_WdeFoaO6LCIwpywOEh0DeXAtlIW-xh5agDBDIEsTv9b worker1
```

> Reminder: If you enter an invalid `User email` `User ton address`, you will not receive a reward. Regarding whether the setting is successful, you can check your account status on toncoin.com after you start mining and a few minutes after submitting the share.
