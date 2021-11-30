# Hiveos mining client installation

## 1. Download and install the mining client

**Install opencl environment**
```
sudo apt-get update
sudo apt-get upgrade -y python3
sudo apt-get install -y opencl-headers ocl-icd-libopencl1 ocl-icd-opencl-dev clinfo
```

**Create a mining directory and download the client**
```
cd ~
sudo rm -r tonmine*
mkdir tonmine
cd tonmine
wget https://github.com/tonmine/tonmine-client/releases/download/v0.2/tonmine-hiveos.tar.gz
tar zxvf tonmine-hiveos.tar.gz
```

## 2. Start mining

Mining command description：

```
bash ~/tonmine/autoStart.sh <User email> <User ton address> <worker id>
```

Sample mining commands：
```
bash ~/tonmine/autoStart.sh tonmine@gmail.com EQCk_WdeFoaO6LCIwpywOEh0DeXAtlIW-xh5agDBDIEsTv9b worker1
```

> Reminder: If you enter an invalid <User email> <User ton address>, you will not receive a reward. Regarding whether the setting is successful, you can check your account status on toncoin.com after you start mining and a few minutes after submitting the share.