Download Link: https://assignmentchef.com/product/solved-csc4103-assignment2-page-replacement-algorithm
<br>
To implement a page replacement algorithm used by operating systems.

Background

If the total memory demand exceeds the physical memory capacity, the operating system needs to replace pages from memory based on the locality principle. The CLOCK (i.e., Second-Chance) algorithm is an approximation of the well-known Least Recently Used (LRU) algorithm, which evicts the least recently accessed pages. The CLOCK algorithm uses a reference bit associated with each page to efficiently estimate the recency of page references and identify the victim pages for eviction.

<h1>Programming Task</h1>

Write a program that implements the CLOCK page replacement algorithm. Use the page reference sequence in the input file to drive your program. Report the number of page faults and latencies incurred by the page faults (see details below). The number of available page frames can be set as specified by an input parameter of your program. Assume that demand paging is used and the page frames are initially free. More details about the CLOCK algorithm can be found in the lecture notes and the textbook.

<strong><u>Programming Language</u></strong> C/C++ or Java.




<h1>Detailed Requirements</h1>

<ul>

 <li>The program should accept two input parameters to specify:

  <ol>

   <li>The memory size (the number of available page frames)</li>

   <li>The input page reference file that contains the page references.</li>

  </ol></li>

</ul>

Example: $ ./replace 20 pageref.txt

<em> </em>

<strong>Page Reference File Format</strong>: Each line has two fields. The first field is either “R” or “W”, meaning a read or a write to the page, respectively. The second field is the page number. Thus, each line of the input file specifies a page reference. Our course website provides two sample input page reference files: <u>http://www.csc.lsu.edu/~fchen/class/csc4103-sp19/assignments/pageref.txt</u> <u>http://www.csc.lsu.edu/~fchen/class/csc4103-sp19/assignments/pageref-simple.txt</u>







<ul>

 <li>The program should generate the following output information:

  <ol>

   <li>The total number of page references.</li>

   <li>The total number of page faults.</li>

   <li>The total number of time units for swapping in pages.</li>

   <li>The total number of time units for swapping out pages.</li>

  </ol></li>

</ul>




<em> </em>

<ul>

 <li>Page fault costs: The program needs to calculate the “cost” of page faults in terms of time units. In particular, upon a page hit (the page is found in memory), the reference cost is 0; upon a page miss (the page is not found in memory), it takes 5 time units to load (swap in) the page. When evicting a victim page, if the victim page is modified (i.e., the page has been written in memory), it takes 10 time units to write (swap out) the modified victim page to the swap space. We assume the pages are all initially in the swap space and not in memory.</li>

</ul>




<ul>

 <li>Your submission should include an README file to clearly explain how to compile and run your code, such as the command, parameters, and expected input and output, and any other necessary information. In the README file, please also provide your full name, LSU ID, and email address.</li>

</ul>


