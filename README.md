# Intel QAT with 5G NR Security

## Dependency

The code is verified with the following dependencies.

- Hardware: Intel® C62x Chipset
- Software: Driver v1.7.l.4.9.0-00008

## Usage

Download and install Intel QAT software.

```bash
sudo apt-get install build-essential g++ pkg-config libssl-dev zlib1g-dev libudev-dev
mkdir ~/qat && cd qat
wget https://01.org/sites/default/files/downloads/qat1.7.l.4.9.0-00008.tar.gz
tar -zxof qat1.7.l.4.9.0-00008.tar.gz
./configure
make
sudo make install
sudo service qat_service start
```

Clone and build the code for 5G NR security.

```bash
git clone https://github.com/stevenchiu30801/5GNR-QAT.git
cd 5GNR-QAT
make
```

Run
```bash
# Arguments:
#     ALGO        Security algorithm - nea1, nea2 or nea3
#     TESTSET     Test set number - 1 to 3
sudo ./main [ALGO] [TESTSET]
```
