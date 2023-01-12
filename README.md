[![module3_task2](https://github.com/WilsonValer/holbertonschool-validation/actions/workflows/module3_task2.yml/badge.svg)](https://github.com/WilsonValer/holbertonschool-validation/actions/workflows/module3_task2.yml)

# how to install GO.
* sudo apt update -> upgrade
* wget https://go.dev/dl/go1.19.4.linux-amd64.tar.gz
* tar -xvf go1.19.4.linux-amd64.tar.gz
* sudo mv go /usr/local
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
* source ~/.bashrc
* go version ..
* go version go1.19.4 linux/amd64
# how to install hugo 
* sudo apt update -> upgrade
* wget ` https://github.com/gohugoio/hugo/releases/download/v0.109.0/hugo_extended_0.109.0_linux-amd64.deb`
* sudo dpkg -i `hugo_extended_0.109.0_linux-amd64.deb`
* hugo version
* hugo v0.109.0-47b12b83e636224e5e601813ff3e6790c191e371+extended linux/amd64 BuildDate=2022-12-23T10:38:11Z VendorInfo=gohugoio
