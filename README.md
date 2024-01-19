[![Automatic version updates](https://github.com/ZOSOpenTools/shdocport/actions/workflows/bump.yml/badge.svg)](https://github.com/ZOSOpenTools/shdocport/actions/workflows/bump.yml)

# shdocport
shdoc is a documentation generator for bash/zsh/sh for generating API documentation in Markdown from shell scripts source.  shdoc parses annotations in the beginning of a given file and alongside function definitions, and creates a markdown file with ready to use documentation.


Generate documentation with the following command:

`$ shdoc < lib.sh > doc.md`

Source [examples/readme-example.sh](https://github.com/reconquest/shdoc/blob/master/examples/readme-example.sh)

Output: [examples/readme-example.md](https://github.com/reconquest/shdoc/blob/master/examples/readme-example.md)


### Features:

### @name
A name of the project, used as a title of the doc. Can be specified once in the beginning of the file.

**Example**
	
	#!/bin/bash
	# @name MyLibrary
	
### @file
Identical to @name.

### @brief
A brief line about the project. Can be specified once in the beginning of the file.

**Example**

	 #!/bin/bash
	 @brief A library to solve a few problems.
	 
### @description
A multiline description of the project/section/function.

* 	Can be specified once for the whole file in the beginning of the file.
*  Can be specified once for on top of a function definition.

Example

	#!/bin/bash
	# @description A long description of the library.
	# Second line of the project description.
	# @description My super function.
	# Second line of my super function description.
	function super() {
	    ...
	}
	

### Further reading: [here](https://github.com/reconquest/shdoc/blob/master/README.md).
