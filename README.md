# assignment07

Read the analysis document before starting. As always, do not modify any file names, package names, or method signatures.

This assignment is due October 19 at 11:59 pm. You must work by yourself on this assignment.

The purpose of this assignment is to practice your knowledge of linked lists and stacks

The Problem

We have been asked to solve the problem of checking program source code for unbalanced symbols, e.g., a { without a matching }. You only need to support { }, ( ), and [ ] explicitly, but you must also handle the caveats in bullet 4 below.

We recognize the elegance of using a stack to keep track of matching symbols. 

If we read a (, {, or [, we will push it on the stack. 

If we read a ), }, or ], we will pop and examine the symbol at the top of the stack.
If the symbol matches, e.g., we read a ] and the top symbol is a [, then we will continue reading.
If the symbol does not match, e.g., we read a } and the top symbol is a [, then we will report the error and terminate.

When all symbols have been read, we will check for an empty stack.
If the stack is empty, then the program correctly matches all symbols.
If the stack is not empty, then we will report the error.

Two kinds of comments are allowed (// and /* ... */), and we will ignore any symbols contained in a comment. Furthermore, we will also ignore symbols contained in string and character literals.
 Since a stack data structure must be constructed to solve this problem, we decide to create a generic stack class, so that it may be used to solve other problems.

Requirements

The LinkedListStack.javaPreview the documentView in a new window class has been started for you. Fill in the methods where indicated. Note that the stack is backed by an instance of your DoublyLinkedList class from Assignment 6. (Do not implement a linked list directly in the stack class.) Recall that all stack methods must be O(1).

The BalancedSymbolChecker View in a new windowclass has been started for you. Fill in the checkFile method such that it uses an instance of LinkedListStack to determine if an input file contains unbalanced symbols using the technique described above. Be sure to use the provided error message methods so that your checker will be compatible with the TA grading program. For demonstration of how the checker should behave, see the examples below.

Create and submit tests for both classes given above.

Symbol Matcher Examples

Download a zip fileView in a new window containing all the .java files referenced in the examples below.

NOTE: The correct behavior of the checker is to report the line and column number where the symbol mismatch is detected, and not the line and column number of the original symbol.

Class1.java results in the message "ERROR: Unmatched symbol at line 6 and column 1. Expected ), but read } instead."
Class2.java results in the message "ERROR: Unmatched symbol at line 7 and column 1. Expected  , but read } instead."
Class3.java results in the message "No errors found. All symbols match."
Class4.java results in the message "ERROR: File ended before closing comment."
Class5.java results in the message "ERROR: Unmatched symbol at line 3 and column 18. Expected ], but read } instead."
Class6.java results in the message "No errors found. All symbols match."
Class7.java results in the message "ERROR: Unmatched symbol at line 3 and column 33. Expected ], but read ) instead."
Class8.java results in the message "ERROR: Unmatched symbol at line 5 and column 30. Expected }, but read ) instead."
Class9.java results in the message "ERROR: Unmatched symbol at line 3 and column 33. Expected ), but read ] instead."
Class10.java results in the message "ERROR: Unmatched symbol at line 5 and column 10. Expected }, but read ] instead."
Class11.java results in the message "ERROR: Unmatched symbol at the end of file. Expected }."
Class12.java results in the message "No errors found. All symbols match."
Class13.java results in the message "No errors found. All symbols match."
Class14.java results in the message "No errors found. All symbols match."
Finishing up

When preliminary coding is complete and your program compiles without error or warning, test the program thoroughly and systematically.

Your code should be well-commented (Javadoc comments are required) and formatted such that it is clear and easy to read. Be sure to put your name in the header comment of each file -- please make sure your name match what we have in Canvas. You must have at least: comments for every method you write, describing what the method does, what the arguments are (and what they mean), and what the return value is, as well as any special cases that the method handles or can run in to. You should also have comments on any line or block of code that is not self-explanatory.

Zip your source code files (no .class files, source code only) and upload the zip file here by 11:59pm on October 19. Be sure to include all files necessary for running your code. Please submit just one solution per pair (i.e., one partner should upload the zip file and an analysis doc, the other should only upload an analysis doc). Don't forget to include the files needed for your linked list from the assignment06 package.

Don't forget your assignment.properties file!
