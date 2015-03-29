# ADO_BufferManager
ADO assignment2 BufferManager CS525
-------------------------------------------------------------------------------------------------------------------------------------------------------------

Instructions to Run the Code:

1) Go to Project root (Assignment2) using Terminal (Folder named "Alternate" contains an alternate version that does not work, it has been submitted for reference as described below)

2) Type "make clean" to delete old compiled .o files.

3) Type "make" to compile all project files including "test_assign2_1.c" file 


4) Type "make run" to run "test_assign2_1.c" file.


5) Type "make test2" to compile Custom test file "test_assign2_2.c"(added by the team for CLOCK and LFU algorithm test cases).


6) Type "make run2" to run "test_assign2_2.c" file. 




------------------------------------------------------------------------------------------------------------------------------------------------------------
About the Code:

We have implemented the following algorithms:


1) FIFO

2) LRU

3) CLOCK

4) LFU



Brief ideas:



1) FIFO: We maintain a global integer variable that is incremented each time a page is replaced. (This variable)%bufferSize enables us to point to
the page 

that has to be evicted at each turn. 



2) LRU: A global integer variable helps us to maintain the order in which the pages came in. For example:Consider buffersize 2 and if Page-90 is the 1000th 

page to be used from memory 
and page-91 is the 1001th page to be used from memory, The page to be evicted is page 90 as it was Least recently used. 
Our 

Global Integer variable acts as a kind of time stamp.



3) Clock: A clock pointer is maintained which points to the frame from where the replacement algorithm starts, another variable is toggled between 1 and 0, 

if this variable is 1 then
a second chance is given to this page and the value is toggled to 0 and the pointer in incremented to continue looking for a page 

to replace. A page is replaced if the variable value is 0 and
if it is the earliest page that came in.
	


4) LFU: A global integer variable maintains the number of time each page in memory was referenced. The page with Least number of references gets evicted. 

----------------------------------------------------------------------------------------------------------------------------------------
