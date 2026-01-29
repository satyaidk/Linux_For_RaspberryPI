# Linux_For_RaspberryPI
```
sudo apt install build-essential tk-dev libncurses5-dev libncursesw5-dev libreadline6-dev libdb5.3-dev libgdbm-dev libsqlite3-dev libssl-dev libbz2-dev libexpat1-dev liblzma-dev zlib1g-dev libffi-dev -y

```
Download Python 3.10 Source:
Download the desired version (e.g., 3.10.8) from the Python website.
```
wget https://www.python.org/ftp/python/3.10.8/Python-3.10.8.tgz

```
Extract the Files
```
tar -zxvf Python-3.10.8.tgz
cd Python-3.10.8

```
Configure and Build:
Run the configuration script and compile the code. Note: This process can take over an hour on a Raspberry Pi 4.
```
./configure --enable-optimizations
make -j$(nproc)

```
Install Python 3.10:
Use altinstall to avoid breaking the default system Python.
```
sudo make altinstall

```
