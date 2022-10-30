
## Merging new Marlin Version

git clone git@github.com:Spudwick/Ender-3-V2-Firmware.git

git remote add marlin https://github.com/MarlinFirmware/Marlin.git

git remote -v

git fetch marlin

git branch -r
git tag

git checkout tags/2.1.1 -b marlin-2.1.1

git checkout main

git merge marlin-2.1.1 --allow-unrelated-histories

## Marlin 2.1.1 License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.