# java-universal-executable
Create a file that's directly executable on both Windows and Mac OS from a java project.
The result is a **hello world** program weighting 100MB.

### simple mode
Creates an executable jar file and prepends it by a combined shell/batch script 
([header-simple.txt](header-simple.txt)) that basically executes
`java -jar <the file itself>`.

Created by `mvn install -Psimple`.
 
### complete mode
Additionally adds a java runtime environment for Windows and Mac OS to the jar file.
The starter script ([header-complete.txt](header-complete.txt)) 
unpacks the correct runtime if necessary and uses it to execute 
`java -jar <the file itself>`.

Created by `mvn install -Pcomplete`.
