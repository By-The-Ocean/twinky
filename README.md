We are yet in ALPHA, feel free to use and comment.
#What is Twinky?

* Have you ever been tired to change a single line of code in your project over and over when uploading to a web server?
* Would you like to have some parts of your code to be automatically commented in or out when it is needed?
* Would you choose to use some other people code instead of writing your own deploy script for the next cople of hours?

If the answer is YES, try twinky!

Twinky
-
Twinky is written as a small, yet efficient tool for day to day web app deploying. What it does is simple. Mark some code like this:

    /*tagname#start*/
	     Your code block!
    /*tagname#end*/
    
   replace "tagname" with any text, numbers, underscores.
   

   Then in chosen directory:

       $ twinky -t=tagname,some_other_tag   
Then in a directory you will get a zip archive with all files in folder, and in every file, every code block withhin chosen tags will be open:

   
    /*tagname#start*/
	     Your code block!
    /*tagname#end*/
And every other, closed:

        /*other#start*/
        //  Your code block!
        /*other#end*/
Simple!

Other info
-
* .twinkyignore 
Script creates this file on run and check if every directory and file in main folder match the written.
Those that match are not put in output archive.

* -t=TAGS,SEPARATED,BY,COMA
use -t option to pass tags you want Twinky to use.
