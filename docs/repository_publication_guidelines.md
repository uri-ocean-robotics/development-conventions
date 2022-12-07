# Public Repository Checklist 

## Requirements

All public repositories for this organization must comply with the following checklist.  If they do not, an administrator will make your repository private until it complies. 

- **README.md file:** Every package must have a README.md file in the root of the repository.  The readme must describe, at least, the following:
  - The name of the package
  - A few sentences briefly describing what the package is for
  - Installation instructions detailed enough to be executed by a novice linux/ROS user
  - A quick start guide or hello world
  - A template [README.md](templates/README.md) is available here.
- **CONTRIBUTING.md file:** This file describes how to contribute to the project.  A default [CONTRIBUTING.md](templates/CONTRIBUTING.md) is available here.  It can be modified as necessary.
- **LICENSE file:** A license file should be included.  See our [licensing guidelines](license) for some options.
- **Semantic Versioning:** The repo must adhere to [Semantic Versioning 2.0](https://semver.org/).
- **An initial tagged release:** 
  - If the project is ready to ship  include initial release with `v1.0.0`
  - Pre-release code may be shared and must be tagged as `v0.x.y`
- **All code in the master branch must ALWAYS be deployable**

## Highly Encouraged

- **Adherence to our [Style Guide](style_guide):** This is especially recommended if you are starting a new project.  If you are migrating an old one, it can be overlooked.
- **Use of GitFlow:** Follow our [guidelines on version control](version_control) for more info

## Sugested
- Issues template
- Doxygen documentation for C++ code
- Sphinx documentation for python code
