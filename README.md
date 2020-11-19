# behave-testrunner

Python script testrunner allowing to run multiple times python behave tests. 
To be used in conjunction with behave tests, with the following options:

- Run a single test scenario x times (option -n)
- Run any given number of different test scenarios x times (option -n)
- Run a single feature x times (option -f)
- Run any given number of different feature files x times (option -f)
- Run the whole testsuite x times
- The logs can also be stored on a file (option -o)

-----

Note on how to run it:

If testrunner script is not located on folder included on $PATH:
python testrunner ...

If testrunner script is located on PATH, the python command does not need to be indicated:
testrunner ...

-----

Examples of how it can be run:

Run a single test scenario x times (option -n):
testrunner 4 -n F02-S03

Run any given number of different test scenarios x times (option -n):
testrunner 5 -n F01-S04 F02-S03 

Run a single feature x times (option -f):
testrunner 5 -n F01-S04 F02-S03

Run any given number of different feature files x times (option -f):
testrunner 3 -f mode0Features/F03-mode0Actions.feature mode1Features/F06-mode1DisallowedCondTransitions.feature

Run the whole testsuite x times:
testrunner 2

The logs can also be stored on a file (option -o):
testrunner 2 -n F02-S03 -o out.txt


With this option (taken from -o option from behave), the output is not in its totality redirected to the file; e.g the summary is still displayed on stdout on the console. If desired to redirect the full output to a file, just do:
testrunner 2 -n F02-S03 > out.txt
