# ZIP treatment for Git
This repository is a suggestion for treating ZIP archive based file types in Git.

# Usage hints
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
 8. Test it.
 9. Remove the example files `hello-world.odt` and `hello-world.kra`.
 10. Use it :-)

## License
This project is free software under the terms of the CC BY 4.0 license.
For more details please see the LICENSE file or: [Creative Commons](http://creativecommons.org/licenses/by/4.0)

## Credits
 * 2021 by Vivien Richter <vivien-richter@outlook.de>
 * Git repository: [GitHub](https://github.com/vivi90/git-zip.git)
