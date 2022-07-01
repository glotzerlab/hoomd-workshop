# Instructions to build binaries for colab

* Install `constructor` with conda.
* Before making the release, run `bump2version` to:
  * Update the condacolab install lines in the notebooks to point to the new release.
  * Update the release number in `construct.yaml`.
* Run:

      constructor --platform linux-64 .

* Make a GitHub release and upload the file to the release. For example:

      git tag -a v2022.0.1
      git push origin --tags
      gh release create 2022.0.1 hoomd-workshop-2022.0.1-Linux-x86_64.sh

For more information see: https://pypi.org/project/condacolab/
