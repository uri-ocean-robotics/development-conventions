---
label: using-git
---

# Using Git

## Branching and Merging Strategy

The URI Ocean Robotics uses “gitfow” for collaborative software development.   Before you start working with lab projects please read up on this process by following the link below.

- [Gitflow Workflow (atlassian article)](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)


![image](https://user-images.githubusercontent.com/23006525/195377078-e47d087d-46af-4a55-bda8-4b324426bc46.png)


## URI Ocean Robotics Gitflow Conventions

Please review the Atlassian tutorial before reading.

- Software development should occur in the “devel” branch.
- Minor changes that don’t change (intend) behaviors can be pushed directly to the devel branch
- If you want to implement a new feature you MUST create a feature branch or a personal fork.   Depending on the scope of the project you can either:
  - merge this with the devel branch directly
  - create a pull request to the devel branch so that other members of your team can review it before merging.

### Our branch prefixes

It seems everyone has a slightly different opinion on what the branch prefixes should be called.  Make sure you use the following branch prefixes so that we are consistent across our work.

**Branches**
- **Master/Main Branch:** master
- **Development Branch:** devel
**Prefixes**
- **Feature Branch:** feature/
- **Release Branch:** release/
- **Hotfix Branch:** hotfix/
- **Version Tag:**  v

### Version Numbering Scheme

We use a, three field, [Semantic Versioning](https://semver.org/) scheme:  a.b.c

- **c:**  <bugfixes, minor improvements, incremental performance improvements > increment this number if you made minor changes that don’t add any major features or preformed minor bug fixes
- **b:** <new features> increment this number if you added a significant new feature that won’t change the behavior of existing code
- **a:** <breaking changes> Increment this number if you made significant changes to the code that alters the behavior or existing parts software.

For more details read up on [Semantic Versioning 2.0](https://semver.org/)

**some examples:**

If I have a package that depends on version 1.1.1  it is not guaranteed to work with version 2.0.0

If I have a package that depends on version 1.1.1 it is guaranteed to work with version 1.2.0 or 1.1.2

If I have a package that depends on version 1.2.2 is should work with the older version 1.2.1 but may not work with 1.1.x since it may depend on a new feature added.


## Sofware to help with Git and GitFlow

This branching/merging strategy may seem overwhelming via command line.   If you are new to Git, it is recommended that you use Git Kraken to help you manage complex git tasks and visualize this branching strategy in action.

As a student, you can get the full pro version for free by following the instructions on [this page](https://www.gitkraken.com/github-student-developer-pack).

### GitKraken and GitFlow

GitKraken has native support for GitFlow.  Follow the instructions here to set it up.  Just make sure your set  your prefixes Correctly according to the branch names and prefixes set above in this document.

Keep in mind this configuration needs to be set for EACH repo you work on.  This is not a global setting.

https://help.gitkraken.com/gitkraken-client/git-flow/

![image](https://user-images.githubusercontent.com/23006525/195403892-e64e1c1b-21c4-475e-9a0c-2aa2b89eec84.png)



