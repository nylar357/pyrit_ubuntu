Pre-requisites
Step-1: Update System and Install Dependencies

For packages that need to be installed on your system, execute the following commands in terminal.
Update the system:

```  sudo apt update -y   ```

Install the dependencies:

```  sudo apt install git python2-dev libssl-dev libpcap-dev -y   ```

 
Step-2: Compile Pyrit
Pull the application from the Github page:

```  git clone https://github.com/JPaulMora/Pyrit.git --depth=1   ```
```  sed -i "s/COMPILE_AESNI/COMPILE_AESNIX/" Pyrit/cpyrit/_cpyrit_cpu.c    ```

  HINT:
If you skip the above step, you will get the following error after pyrit -h command:

Traceback (most recent call last):
  File "/usr/local/bin/pyrit", line 4, in <module>
    import pyrit_cli
  File "/usr/local/lib/python2.7/dist-packages/cpyrit/util.py", line 54, in <module>
    import _cpyrit_cpu
ImportError: /usr/local/lib/python2.7/dist-packages/cpyrit/_cpyrit_cpu.so: undefined symbol: aesni_key

  Run the following steps in order:

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

 
Step-3: Install Pyrit
It may give some warnings after compilation. Then run the install command:

```   sudo python2 setup.py install

```running install
running build
running build_py
running build_ext
running build_scripts
running install_lib
creating /usr/local/lib/python2.7/dist-packages/cpyrit
copying build/lib.linux-x86_64-2.7/cpyrit/_cpyrit_cpu.so -> /usr/local/lib/python2.7/dist-packages/cpyrit
copying build/lib.linux-x86_64-2.7/cpyrit/cpyrit.py -> /usr/local/lib/python2.7/dist-packages/cpyrit
copying build/lib.linux-x86_64-2.7/cpyrit/pckttools.py ->  ```
.
.
.
``` byte-compiling /usr/local/lib/python2.7/dist-packages/pyrit_cli.py to pyrit_cli.pyc
writing byte-compilation script '/tmp/tmpEBSxgv.py'
/usr/bin/python2 -O /tmp/tmpEBSxgv.py
removing /tmp/tmpEBSxgv.py
running install_scripts
copying build/scripts-2.7/pyrit -> /usr/local/bin
changing mode of /usr/local/bin/pyrit to 755
running install_egg_info
Writing /usr/local/lib/python2.7/dist-packages/pyrit-0.5.1.egg-info  ```



After this step, go up one directory to avoid messing with module searches:

```   cd ..  ```

``` pyrit -h ```          

 
ALSO READ: How to set up WordPress Reverse Shell [100% Working]
Step-5: Using Pyrit

Run the following command to list the available cores:

```  pyrit list_cores  ```
