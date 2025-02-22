# Build DeFi Wallet on Raspberry Pi 4B with Raspberry OS 32-Bit or 64-Bit


## Documentation
- DefiCh/app (https://github.com/DeFiCh/app)
- DefiCh/jellyfish (https://github.com/DeFiCh/jellyfish)
- Nodejs (https://github.com/nodesource/distributions/blob/master/README.md#debinstall)
- Workspaces (https://docs.npmjs.com/cli/v7/using-npm/workspaces)
- Electron (https://www.beekeeperstudio.io/blog/electron-apps-for-arm-and-raspberry-pi)
- Defi Node (https://github.com/Martin8617/Defi-Node-for-Raspberry-Pi/blob/main/build-ain-armv7l.md)


## Source Code
Download source code and extract them to your `/home/user/` directory:
- app-2.6.2 (https://github.com/DeFiCh/app/releases)


## Build app-2.6.2

### Install dependencies for node
Once installed, the node, npm and yarn commands are available for use and will remain updated for the channel you selected.
```
curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt-get update
sudo apt-get install -y nodejs
sudo apt-get install gcc g++ make
```
You need `node v14`, and `npm v7` for this project, it's required to set up the npm workspaces. So you have to upgrade npm.
```shell
sudo npm -g install npm@7.21.0
```

### Install dependencies for yarn (if needed)
````
curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | gpg --dearmor | sudo tee /usr/share/keyrings/yarnkey.gpg >/dev/null
echo "deb [signed-by=/usr/share/keyrings/yarnkey.gpg] https://dl.yarnpkg.com/debian stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update
sudo apt-get install yarn
````


### Setup the required binary
Copy respective replace the [files](https://github.com/Martin8617/Defi-Wallet-for-Raspberry-Pi/tree/main/files) into `home/pi/app-2.6.2`(or further versions):
```
pre-build-armv7l.sh
pre-build-arm64.sh
package.json
```
Note: The files `pre-build-armv7l.sh` and `pre-build-arm64.sh` will download my Defi Node from this homepage and copy it into your app directory. If you use your own build Defi Node you have to replace the download link in the files with your directory.


### To build the app using arm platform
```
cd /home/pi/app-2.6.2
npm run init
```
Note: A few warnings occures, however the app works. The Raspberry OS 32-Bit works fine, the 64-Bit version too - even with more warnings...


### Build app
And finally:
- for 32-Bit OS run `npm run build:armv7l`
- for 64-Bit OS run `npm run build:arm64`
