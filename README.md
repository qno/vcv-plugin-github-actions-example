# vcv-plugin-github-actions-example
Example repository for building and publishing a VCV Rack plugin with GitHub Actions.

![Build VCV Rack Plugin](https://github.com/qno/vcv-plugin-github-actions-example/workflows/Build%20VCV%20Rack%20Plugin/badge.svg)

___

### How to build a VCVRack plugin with Github Action

1. In your plugin repository create a folder `.github/workflows`
2. Put the workflow definition [build-plugin.yml](https://github.com/qno/vcv-plugin-github-actions-example/blob/main/.github/workflows/build-plugin.yml) into this folder
3. Make changes to your sources and push them to Github
4. In your Github repository navigate into the Action tab to see the progress and status of the Workflow run
5. To create a Github Release that contains the built plugin for all platforms you need to create and push a tag, e.g. like this:
   * `git tag v2.0.9 -m "create v2.0.9"`
   * `git push origin --tags`
   * **Note:** Make sure that your tag version number is the same as the version in the [plugin.json](https://github.com/qno/vcv-plugin-github-actions-example/blob/main/plugin.json#L4) and the tag starts with v (it is a convention), otherwise the the publish step will be canceled.
