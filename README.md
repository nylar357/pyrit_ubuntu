## ๐๐๐ด๐ฟ-1: ๐๐ฟ๐ณ๐ฐ๐๐ด ๐ฐ๐ฝ๐ณ ๐ธ๐ฝ๐๐๐ฐ๐ป๐ป ๐ณ๐ด๐ฟ๐
For packages that need to be installed on your system, execute the following commands in terminal.
Update the system:

```  sudo apt update -y   ```

# ๐ด๐๐๐๐๐๐ ๐๐๐ ๐๐๐๐๐๐๐๐๐๐๐๐:

```  sudo apt install git python2-dev libssl-dev libpcap-dev -y   ```

 

## ๐ข๐ฃ๐๐-โ: ๐๐๐๐๐๐๐ ๐๐จ๐ก๐๐ฃ

```  git clone https://github.com/JPaulMora/Pyrit.git --depth=1   ```

```  sed -i "s/COMPILE_AESNI/COMPILE_AESNIX/" Pyrit/cpyrit/_cpyrit_cpu.c    ```

#   ๐ญโโโโโ ๐ฎโโโโโ ๐ณโโโโโ ๐นโโโโโ
If you skip the above step, you will get the following error after pyrit -h command:

Traceback (most recent call last):
  File "/usr/local/bin/pyrit", line 4, in <module>
    import pyrit_cli
  File "/usr/local/lib/python2.7/dist-packages/cpyrit/util.py", line 54, in <module>
    import _cpyrit_cpu
ImportError: /usr/local/lib/python2.7/dist-packages/cpyrit/_cpyrit_cpu.so: undefined symbol: aesni_key

แดฟแตโฟ แตสฐแต แถ แตหกหกแตสทโฑโฟแต หขแตแตแตหข โฑโฟ แตสณแตแตสณโ 

``` pyrit -h ``` 

```   python2 setup.py clean   ```

 ```   python2 setup.py build   ``` 

running build
running build_py
creating build
creating build/lib.linux-x86_64-2.7
copying pyrit_cli.py -> build/lib.linux-x86_64-2.7
creating build/lib.linux-x86_64-2.7/cpyrit 
running build_scripts
creating build/scripts-2.7
copying and adjusting pyrit -> build/scripts-2.7
changing mode of build/scripts-2.7/pyrit from 644 to 755  

## ๏ผณ๏ฝ๏ฝ๏ฝ๏ผ๏ผ๏ผ ๏ผฉ๏ฝ๏ฝ๏ฝ๏ฝ๏ฝ๏ฝ ๏ผฐ๏ฝ๏ฝ๏ฝ๏ฝ
 
 # ๐๐ฅ ๐๐๐ช ๐๐๐ง๐ ๐ค๐ ๐๐ ๐จ๐๐ฃ๐๐๐๐๐ค ๐๐๐ฅ๐๐ฃ ๐๐ ๐๐ก๐๐๐๐ฅ๐๐ ๐. ๐๐๐๐ ๐ฃ๐ฆ๐ ๐ฅ๐๐ ๐๐๐ค๐ฅ๐๐๐ ๐๐ ๐๐๐๐๐:
```sudo python2 setup.py install```

![preview](img/pyrit1.png)


![preview](img/pyrit2.png)


![preview](img/pyrit3.png)
