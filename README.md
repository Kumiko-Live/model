# Kumiko Live! model files
[![Chat](https://discord.com/api/guilds/813738237864312842/widget.png?style=shield)](https://discord.gg/jt4dpvzA58)
[![YouTube](https://img.shields.io/endpoint?url=https%3A%2F%2Frunkit.io%2Fsuk0m8u%2Fyoutube-subscribers-badge%2Fbranches%2Fmaster%3Fid%3DUCGcClcnm7Y0-jWSeSV5xnKw%26key%3DAIzaSyDmc6HmurAU4Hf5WvuxSTsym18SjR7fguc)](https://www.youtube.com/channel/UCGcClcnm7Y0-jWSeSV5xnKw)

_![Current preview](.Kumiko.fvp.content/print_data/images/print_image_front.png)_

## About
This repository contains all 3D models of [Kumiko Live!](https://www.youtube.com/channel/UCGcClcnm7Y0-jWSeSV5xnKw)

## How to clone
 1. Install [Git LFS](https://git-lfs.github.com)
 2. Prepare LFS by issuing the command `git lfs install` once.
 3. Fork this repository.
 4. Clone it.
 5. Add the filter by issuing the following commands:
 ```bash
 git config filter.zip.clean "unzip -v %f | tail -n +4 | head -n -2 | awk '{ print \$7,\$8 }' | grep -vE /$ | sort -k 2"
 git config filter.zip.smudge "unzip -v %f | tail -n +4 | head -n -2 | awk '{ print \$7,\$8 }' | grep -vE /$ | sort -k 2"
 ```
 6. Install the hooks by issuing the command `git config core.hooksPath .githooks`.
 7. Apply the checkout hook once by issuing the command `.githooks/post-checkout`.
 8. Apply the filter once by issuing the command `git add -A`.

## Credits
 * 2021 by [Vivien Richter](https://github.com/vivi90) and [Romy Kircheis](https://github.com/RomyKircheis)
 * Git repository: [GitHub](https://github.com/Kumiko-Live/model.git)
