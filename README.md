# Kumiko Live! model files
[![Chat](https://discord.com/api/guilds/813738237864312842/widget.png?style=shield)](https://discord.gg/jt4dpvzA58)
[![YouTube](https://img.shields.io/endpoint?url=https%3A%2F%2Frunkit.io%2Fsuk0m8u%2Fyoutube-subscribers-badge%2Fbranches%2Fmaster%3Fid%3DUCGcClcnm7Y0-jWSeSV5xnKw%26key%3DAIzaSyDmc6HmurAU4Hf5WvuxSTsym18SjR7fguc)](https://www.youtube.com/channel/UCGcClcnm7Y0-jWSeSV5xnKw)

_![Current preview](.Kumiko.fvp.content/print_data/images/print_image_front.png)_

## About
This repository contains all 3D models of [Kumiko Live!](https://www.youtube.com/channel/UCGcClcnm7Y0-jWSeSV5xnKw)

## Used software:
 - [VRoid Studio](https://vroid.com/en/studio) 0.13.1
 - [Krita](https://krita.org/en) 4.4.2

## How to clone
 1. Install [Git LFS](https://git-lfs.github.com)
 2. Prepare LFS by issuing the command `git lfs install` once.
 3. Fork this repository.
 4. Clone it.
 5. Add the filter by issuing the following commands:
 ```bash
 git config filter.zip.clean "unzip -v %f | tail -n +4 | head -n -2 | awk '{ print \$7,\$8 }' | grep -vE /$ | LC_ALL=C sort -sfk 2,2"
 git config filter.zip.smudge "cat"
 git config filter.zip.required true
 ```
 6. Install the hooks by issuing the command `git config core.hooksPath .githooks`.
 7. Apply the checkout hook once by issuing the command `.githooks/post-checkout`.
 8. Apply the filter once by issuing the command `git add -A`.

## Good to know
 - Steps `5.` and `7.` of `How to clone` doesn't work in `PowerShell`, so please use `Git Bash` for this step if you are working with Windows.

## License
Please don't use it without explicit permission.

## Credits
 * Please check the commits for further details.
 * [Git repository](https://github.com/Kumiko-Live/model.git)
