PEBILRegressionTesting
======================
This repo will have the regression tests for PEBIL. 

The objective for initial version is as follows: 

Project goal: create a set of regression tests for PEBIL's various instrumentation tools
The goal of a regression test is to check the accuracy and the overhead of using the instrumentation tool. There are a series of instrumentation tools that each should have a regression test. In addition PEBIL works on serial, MPI, OpenMP, and hybrid (MPI+OpenMP) codes. Each regression test should have a test for each type of code as well as a version for Fortran, C, and C++.  To design an individual test for a code you should keep in mind how to test the accuracy of the tool being tested. The following are the tools to create a test for:
jbb
siminst
reuse
locality

NOTE: There is a testing framework set up in PEBIL already which focuses on correctness of results in jbb and sim that you may be able to leverage so in order to avoid starting from scratch. Find the `make check' target at the top level and follow the flow. Also,  checking for correctness in parallel runs may be a little challenging. In particular, threaded code is virtually guaranteed to execute somewhat differently from run to run, so using a diff-based approach (as is done now for sequential execution) isn't really feasible. When you get to this point we can all discuss options.
