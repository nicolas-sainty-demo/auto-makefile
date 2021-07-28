# auto-makefile

[![forthebadge](https://forthebadge.com/images/badges/compatibility-emacs.svg)](https://forthebadge.com)\
[![forthebadge](https://forthebadge.com/images/badges/not-a-bug-a-feature.svg)](https://forthebadge.com)\
<img src="https://img.shields.io/badge/TEK-1-green.svg"/>

Just a little script named automakefile, that generates a nice Makefile given a configuration file.
This configuration file can contain the following (potentially unordered) lines:

* source_filename;dependence1 dependence2. . .         (specify the full names of the files, from the header subfolder below)
* PROJECT_DIR;name_of_the_project_root_folder
* SOURCES_DIR;subfolder_containing_the_source_files
* HEADERS_DIR;subfolder_containing_the_header_files
* LIBS_DIR;subfolder_containing_librairies
* EXEC;executable_name
* CC;compilator_binary
* CFLAGS;compilation_flag1 compilation_flag1. . .
* LDFLAGS;linking_flag1 linking_flag2. . .



The following rules are added to the generated Makefile:

* archive
  * backup the source files in a compressed format, in the project folder
* revert
  * recreate the project from last backup
* num
  * print the current version number
* delete
  * delete last backup
