#P1
Compilation is done by gradle, launched in the method processCommit(). The method specifies both compilation and test runs. 
As for unit testing, several methods were hard to unit-test with Junit because not all methods produced a testable result or throwed reliable exceptions. Therefore the focus on testing was on helper functions that are responsible for the back-bone of the project more than the core functions. 
