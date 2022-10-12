# Using Git #

## Branching and Merging Strategy ##

The URI Ocean Robotics uses “gitfow” for collaborative software development.   Before you start working with lab projects please read up on this process by following the link below.

- [Gitflow Workflow (atlassian article)](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)


![image](https://user-images.githubusercontent.com/23006525/195377078-e47d087d-46af-4a55-bda8-4b324426bc46.png)


## URI Ocean Robotics Gitflow Conventions  ##

Please review the Atlassian tutorial before reading.

- Software development should occur in the “devel” branch.  
- Minor changes that don’t change (intend) behaviors can be pushed directly to the devel branch
- If you want to implement a new feature you MUST create a feature branch or a personal fork.   Depending on the scope of the project you can either:
  - merge this with the devel branch directly
  - create a pull request to the devel branch so that other members of your team can review it before merging.

### Our branch prefixes  ###

It seems everyone has a slightly different opinion on what the branch prefixes should be called.  Make sure you use the following branch prefixes so that we are consistent across our work.

**Branches**
- **Master/Main Branch:** master
- **Development Branch:** devel
**Prefixes**
- **Feature Branch:** feature/
- **Release Branch:** release/
- **Hotfix Branch:** hotfix/
- **Version Tag:**  v

