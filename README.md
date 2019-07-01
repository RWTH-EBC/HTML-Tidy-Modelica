# HTML-Tidy-Modelica
This script converts HTML Code in Modelica to get a HTML and Dymola conform code.

### How to use the script **html-tidy.py**:

1. Install tidylib for python with
	- `pip install pytidylib`

2. Install library
	- Get binary from: http://binaries.html-tidy.org/
	
		!Take correct version (64bit 32bit)!

	- Pack .dll and .exe data to PATH environment variable in windows

3. copy html_tidy.py into the modelica directory in which you want to correct your modelica files
	
	*Important: The html_tidy.py has to be in one directory with your package.mo file. All files in this directory and the directory below will be scanned and corrected*
	
4. use `python html_tidy.py --help` for instructions


### How to use the script **view_html_errors.py**:

1. Install pytidylib with dll's as described above
2. run from command line::
	
	`$ python view_html_errors.py <file> [file [...]]`

The script will 

* collect all the HTML code (`<html>...</html>`) in the Modelica file and
* print out the original code with line numbers as well as 
* the tidy version of the code (with line numbers). 
* tidylib will look for errors and present the respective line numbers. 

You can then inspect the code and make corrections to your Modelica
file by hand. You might want to use the tidy version as produced by
tidylib.

#### Note
	This script uses Python 3.6 for printing syntax and
	function parameter annotations.
	

### License
- The script was made for usage at the EON ERC EBC at RWTH Aachen University
- It uses [HTML Tidy](http://www.html-tidy.org/documentation/)
- Some parts of the code are based on the validator.py script from [BuildingsBy](https://github.com/lbl-srg/BuildingsPy)
- Feel free to use and manipulate the script
