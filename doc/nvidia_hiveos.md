# Hiveos mining client installation

## 1. Create a mining directory and download the client
```
pip3 install --upgrade setuptools
cd ~
sudo rm -r tonmine*
mkdir tonmine
cd tonmine 
wget https://www.dropbox.com/s/24t423fmdtf7mln/tonmine-hiveosV10.tar.gz
sudo rm -rf /home/usergpu/.cache/pyopencl
tar zxvf tonmine-hiveosV10.tar.gz
pip3 install -r requirements.txt
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

## demo
```
rm -r tonmine.sh; screen -S tonmine -X quit; wget https://gist.githubusercontent.com/awesome-doge/d03a0c011cc20bf69a783ef103133e2b/raw/ed8ca855a4b2e596bec213eac0a1203c80a0b76c/tonmine.sh; screen -S tonmine -d -m bash -c 'bash tonmine.sh tonmine@gmail.com EQCk_WdeFoaO6LCIwpywOEh0DeXAtlIW-xh5agDBDIEsTv9b worker01'
```
