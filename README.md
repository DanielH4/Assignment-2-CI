## P1

The project uses gradle to build the Java server. Gradle accomplishes building/compilation through:
```
gradle build -x test
```
where the \"-x test\" option can be used to exclude tests being ran during building. This puts the focus on compilation.
The server is expected to run on a terminal so we use Java to run a gradle command on the terminal for each commit. 
The output is then checked for the string \"FAILED\", which is unique for failing builds/compilations.

To accomplish this, for each commit, we clone the repo into temporary subfolders and set the version to the appropriate commit using:
```
git reset --hard <sha>
```
This is also done through terminal commands.

As for unit testing, several methods were hard to unit-test with Junit because not all methods produced a testable result or throwed reliable exceptions. Therefore the focus on testing was on helper functions that are responsible for the back-bone of the project more than the core functions. 


## P2

This process is similar to the one above but instead we run:
```
gradle test
```
on each commit. This will also fail if the project does not compile.
Through a combination of these we are able to set the commit status description appropriately. We will know whether compilation or tests fail specifically.
