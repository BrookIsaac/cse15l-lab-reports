# **Lab Report 1**
1. ## `cd` Examples
   ![Image](cdexamples.png)
    * The current directory was home and `cd` with no arguments didn't do anything because we're already in the home directory so there's nothing to change. This didn't give an error.
    * With a path given to lecture1, starting at the `/home` directory, `cd` took us to that folder, and displayed the folder we were in. This didn't give an error.
    * However given a path to a file, with the current directory being `/home` it showed an error that the there was no such file. This is probably because I inputted the path to the file incorrectly.
2. ## `ls` Examples
     ![Image](lsexamples.png)
     * With no arguments and `/home` being the current directory `ls` listed the folders within the `/home` directory. There was no error.
     * With the path to `/lecture1` and `/home` still being the current directory, it listed the files and folders within lecture1. This didn't cause an error.
     * But with a path to a file within "lecture1" ls couldn't access it, and an error popped up, probably since there were no other files to be listed within that file.
3. ## `cat` Examples
     ![Image](catexamples.png)
      * With no arguments and `/home` as the working directory, `cat` didn't do anything, probably because it had nothing to display
      * With a correct path to a folder and `/home` as the working directory, `cat` printed out the path to the folder and also prints out "Is a directory" to tell us the path we inputted is valid. This was an error, since there was not a specified file with content `cat` could print out
      * With a correct path to a file starting from the `/home` directory, the contents of that file are printed out in full. There was no error.

