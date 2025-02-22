# Defi Wallet for Raspberry Pi

The official DeFiChain AppImage release of the Defi Wallet for Linux will not work for the Raspberrys. So I have made for myself a compiled version of the Defi Wallet for my Raspberry Pi 4B 4GB with official Raspberry Pi OS (32-Bit). This so called `armv7l` version is different to other Linux distributions as well as different to the Raspberry Pi 64-Bit version `arm8` respective `arm64`. 

The compiled Raspberry Pi AppImage bases on the DeFiChain original source code. No code was modyfied and was ~100% taken from the DeFiChain repository - ok, the npm workspace file package.json includes now the build for the arm processors😏
  

## Documentation

- [DeFiChain.com](https://defichain.com/)
- [DeFiCh/app](https://github.com/DeFiCh/app)
- [Build from Scratch](https://github.com/Martin8617/Defi-Wallet-for-Raspberry-Pi/blob/main/build-app.md)


## DeFi Wallet App

Use DeFi Wallet to interact with DeFiChain. It is a wallet for \$DFI, wrapped BTC, ETH, USDT. Liquidity mine, use the DEX, create masternodes, and more.
![Image](https://defichain.com/img/app/liquidity@2x.png)
There are actually 3 different ways `(i./ii./iii.)` to set up a Defi Wallet (Desktop App including DeFi Node), however don't mix up! You have to decide for one of the different ways. Because you are here, I guess you have decided to use my AppImage😉:
- Setup the Raspberry Pi with the offical [Raspberry Pi OS](https://www.raspberrypi.org/software/). Next you have to install the Defi Wallet on your Raspberry Pi:
  1) Using the AppImage from [here](https://github.com/Martin8617/Defi-Wallet-for-Raspberry-Pi/releases) (from this page). 
  2) Using the Script from [DefiNode](https://github.com/DefiNode/DeFiNode/blob/main/README.md#download-script-and-execution). Follow the steps as descripted and build your own Defi Wallet.
  
- Setup the Raspberry Pi with the DeFi-Node-Raspi-Image:
  
  3) Using the Raspberry Pi Image provided on [Google Drive](https://drive.google.com/drive/folders/1yGWeP8gqt5JNypeeJTZ-0aqh-k04m7Jj?usp=sharing) with the [RaspberryPI Imager](https://www.raspberrypi.org/software/). 


## Howto Start

- You can [download here the desktop app](https://github.com/Martin8617/Defi-Wallet-for-Raspberry-Pi/releases) for your Raspberry Pi.
- You can check for official DeFiChain [releases](https://github.com/DeFiCh/app/releases) for latest downloadable installers for Windows, Mac and Linux, however they have no release for the Raspberry - that's why you are here.

After download the AppImage, save the file where you want (e.g. /home/user/desktop/), mark the file as executable (right-klick the icon, choose preferences) and run the AppImage - that's all...

The Defi Wallet will initiate and guide you. Further information is available at the [DeFiChain-Wiki](https://defichain-wiki.com/wiki/DeFi_Wallet).


## Howto Continue

### Buy Hardware

On [DefiNode](https://github.com/DefiNode/DeFiNode) you find a shopping list for the hardware of a Raspberry Pi node as well as a 3D case with DeFiChain logo. A good installation guide of the setup of a Raspberry Pi you can find there as well.

### Run your own Masternode

Just to remember, the Defi Wallet includes a running fullnode so called "Defi Node". On top you can setup the fullnode as a masternode.
The [DefiChain-Wiki](https://defichain-wiki.com/wiki/Masternode_installation_extended) tells you the steps to setup a masternode and the guys from [mydeficha.in](https://mydeficha.in) will serves you with operating your own masternode. 


## Licenses

By using `Defi-Wallet for Raspberry Pi` (this repo), you (the user) agree to be bound by [the terms of this license](LICENSE).

Last updated August 14, 2021
