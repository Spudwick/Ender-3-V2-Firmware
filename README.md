
## Merging new Marlin Version

Clone custom Firmware repository.
```
$ git clone git@github.com:Spudwick/Ender-3-V2-Firmware.git
```

Add Marlin repository as an additional repository remote.
```
$ git remote add marlin https://github.com/MarlinFirmware/Marlin.git

$ git remote -v
marlin  https://github.com/MarlinFirmware/Marlin.git (fetch)
marlin  https://github.com/MarlinFirmware/Marlin.git (push)
origin  git@github.com:Spudwick/Ender-3-V2-Firmware.git (fetch)
origin  git@github.com:Spudwick/Ender-3-V2-Firmware.git (push)
```

Fetch branch and tag information from Marlin remote.
```
$ git fetch marlin

$ git branch -r
marlin/1.0.x
marlin/1.1.x
...
origin/HEAD -> origin/main
origin/main

$ git tag
1.0.0-beta
1.0.1
1.0.2
1.0.2-1
...
```

Checkout desired Marlin tag or branch into a new local branch.
```
$ git checkout tags/2.1.1 -b marlin-2.1.1

$ git checkout main
```

Merge local Marlin branch back into `main`.
```
$ git merge marlin-2.1.1 --allow-unrelated-histories
```

## Marlin 2.1.1 License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
