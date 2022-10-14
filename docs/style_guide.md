# Style Guide #

Software development occurs mostly in Python and c++.   Increasingly, our software is ROS based.  As such, we have adopted the ROS style guide as a basis for our own styles and conventions.  

here is a quick example for C++

```
#ifndef TEMPLATE_CLASS_H
#define TEMPLATE_CLASS_H

#include <ros/ros.h>

class TemplateClass  // Object types are camel cased with the leading letter in caps
{
public:
  TemplateClass();
  void spin();  
  void spin_once();   // member function are camel cased with lower case first char

protected:
  ros::NodeHandlePtr ros_node_ptr_;  // variables are underscored with
                                     // member variables have a trailing underscore
};

#endif // TEMPLATE_CLASS_H
```

There are a lot more style conventions though!  When in doubt, review the official ROS cpp or Python style guides.

- [ROS Cpp Style Guide](http://wiki.ros.org/CppStyleGuide)
- [Ros Python Style Guide](http://wiki.ros.org/PyStyleGuide)

## ROS-based build systems ##

### Basic c++ and/or python package ###

Our packages are based on the ROS package standard conventions.

http://wiki.ros.org/Packages

Additionally,  we typically add a few more common directories and convention for internal constancy.

ROS messages should be in their own sub-package.   That way they can be easily built and imported by external packages without the need to compile the parent package.

### File structure (for the main package): ###

- **include/package_name** this is where all of your c++ headers should go
- **nodes/** This is where all your cpp files that you want to turn into executable go.  In other words every file in this directory should include an “int main()” function
- **src/** This is where all of your c++ source files should 
- **launch/** All launch files should be placed in this directory
- **param/** this directory should include any configuration files some examples are:
  - parameter configurations (YAML)
  - RVIZ configurations
- **urdf/** This directory should include any URDF for XACRO files
- **doc/** If you are using doxygen/readthedocs/etc.. all of your configuration and source files (.md, .rtd) should live here

### Build Sytem ###
A standard cmake file has been created that is based on the file system described above.  There is no need to manually edit the cmakelist.txt when you add new files (although you may need to re-run cmake).  You can look at the template packages linked below as a starting point.

https://bitbucket.org/croman_and_the_barbarians/template_package/src/master/

A standard cmake file has been created that is based on the file system described above.  There is no need to manually edit the cmakelist.txt when you add new files (although you may need to re-run cmake).  You can look at the template packages linked below as a starting point.

- Whenever possible, you should organize source files by directory and automatically “GLOB” them using cmake.  Avoid adding files manually.
- If you have things that are likely to be changed or modified at a later date make them available near the top of the cmake.   An example might be libraries that you want to include.

## Extensions to the ROS style guides ##

Conventions listed in this section are in addition to those listed in the third-party style guides above.

### Cpp ##

#### Namespaces: ####

If you are designing code that is meant to be included by other software it should be namespaced properly.   Follow the guidelines below to be consistent with the rest of the group and to avoid naming conflicts with other packages.

- All code that is designed to be included in other software (i.e. defined in headers) should be namespace with the name of the project.  For the case of ROS consider the project name to be the package name.  For very long package names abbreviation is acceptable.  If you decide to abbreviate, be consistent.

**Example: **
```
namespace template_package {…}
// -- or ---
namespace tp {…}
```

- All namespaces should be lower case and underscored.

**Example: **
```
namespace template_package {…}
// ---not--- 
namespace TemplatePackage {…}
```
- Functions defined outside of a class MUST be namespaced.

**Example:** Assume we have a header that defines arithmetic functions, arithmetic.h
```
namespace template_package { namespace arithmetic{
  double add(double x, double y);
  double mult(double x, double y);
}}
```

