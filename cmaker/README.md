# Cmaker README

Robin.Rowe@Cinepaint.org 2009/3/5

Cmaker is a set of programs that create a framework of cmake files. This saves time when creating a project and ensures consistency in cmake design. It also creates unit tests for use with ctest. 

## Usage

Add cmaker directory to your path or use with full path to call. 

Cmaker expects to find a LICENSE file in your project directory from which it will read the first line as the license text to paste into the project files it creates. If you don't have a LICENSE file, you can create one like this:

	echo "MIT Open Source" > LICENSE

Creating a complete frameworks, including project, program, class files, and unit tests:

	cd YourProjectDirectory
	export AUTHOR="Your Name"
	cmaker_project.sh YourProjectName
	cmaker_program.sh YourExecutableName
	cmaker_class.sh YourClassName AnotherClassName ...
	mkdir build
	cd build
	cmake ..
	make
	ctest

To add another program or class to your project later, simply call the relevant script again. You only need to call cmaker_project.sh once. 

The purpose of cmaker_sources.sh is to import existing legacy files. Is not needed by new projects.
	
--0--