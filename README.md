# Responsive Email Grid<br> (extendable)
Build system use SASS, JADE preprocessors. Base is Gulp.js

[![CSSCODER grid email](https://raw.githubusercontent.com/csscoderRU/responsive-grid-email/master/screens/thumb.png)](http://dev.csscoder.pro/emails/Responsive-Email-Grid/index.html)

### Example [link](http://dev.csscoder.pro/emails/Responsive-Email-Grid/index.html)

Steps use system

    // 1 install node modules
    
    npm install
    
    // 2 build template
    
    gulp

Example

	// Block main setting
	block mainVariables
		- var gGutter = 20; //- gutter columns
		- var gContainer = 600; //- width container
		- var gColumns = 12; //- size column
	
	// Common wrapper-colors-center
	+wrapper('#f3f3f3', '#fcebb6')
		// Row line column
		+row
			// first column size 5 col (if summ size columns = 12)
			+column-first(5)
				.txt-h5.st-center Lorem text
			// center colomn size 4 col
			+column(4)
				.txt-h5.st-center Lorem text
			// last column in line 
			+column-last(3)
				.txt-h5.st-center Lorem text
		
		// Row line column
		+row
			// first column size 5 col (if summ size columns < 12)
			+column-first(5, 11)
				.txt-h5.st-center Lorem text
			// center colomn size 3 col
			+column(3)
				.txt-h5.st-center Lorem text
			// last column in line size 3 col
			+column-last(3)
				.txt-h5.st-center Lorem text
			
		
		
   
Also you must create file **.access.json** in root project folder for ftp load

    {
      "ftp": {
        "host": "test.com(IP)",
        "user": "user-test-FTP",
        "pass": "passwordToFTP",
        "site": "linkToSiteView"
      }
    }

Template tests from Litmus.com
* Outloolk 2000-2016
* Lotus Notes 8 - 9
* Thunderbird
* Apple mail
* Android, gmail.app
* iOS
* popular web clients


Screens folder [link](https://github.com/csscoderRU/Responsive-Email-Grid/tree/master/screens/)