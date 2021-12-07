# Hiveos mining client installation

## 1. Create a mining directory and download the client
```
cd ~
sudo rm -r tonmine*
mkdir tonmine
cd tonmine
wget https://www.dropbox.com/s/2zd1kan056vr2oz/tonmine-hiveosV3.tar.gz
tar zxvf tonmine-hiveosV3.tar.gz
```

## 2. Start mining

**Mining command description：**

```
bash ~/tonmine/autoStart.sh <User email> <User ton address> <worker id>
```
> * `User email` ：When the `worker id` is not in normal mining. An email will be sent to notify the user.
> * `User ton address`：The user needs to enter the user's ton address. (It is strongly recommended that the address needs to complete the activation process)
> * `worker id`：The user can set a different `worker id` for each mining machine. This makes it easier to monitor.

Sample mining commands：
```
# If you need background execution tonmine miner. Then you need to enter `screen` here
screen

bash ~/tonmine/autoStart.sh tonmine@gmail.com EQCk_WdeFoaO6LCIwpywOEh0DeXAtlIW-xh5agDBDIEsTv9b worker1
```

> Reminder: If you enter an invalid `User email` `User ton address`, you will not receive a reward. Regarding whether the setting is successful, you can check your account status on toncoin.com after you start mining and a few minutes after submitting the share.
