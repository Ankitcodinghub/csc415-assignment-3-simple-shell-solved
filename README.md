# csc415-assignment-3-simple-shell-solved
**TO GET THIS SOLUTION VISIT:** [CSC415 Assignment 3-Simple Shell Solved](https://www.ankitcodinghub.com/product/csc415-assignment-3-simple-shell-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;93551&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSC415 Assignment 3-Simple Shell Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (4 votes)    </div>
    </div>
&nbsp;

In our slides we talked about a simple shell. For this assignment you will implement your own shell that runs on top of the regular command-line interpreter for Linux.

Your shell should read lines of user input, then parse and execute the commands by forking/creating new processes. For each command, your shell should call fork() followed by execvp(). Following each command, your shell should wait for its child process to complete, and then print the child PID and the **return result from the child process**. The user should be able to specify the command to execute by giving a path to the executable file (e.g. `/bin/ls`) or by using path expansion to locate the executable file (i.e. searching each directory in the PATH environment variable). (Note that the execvp() function perform this processing automatically; you do not need to program it yourself.)

If your shell encounters an error while reading a line of input it should report the error and exit. If your shell encounters EOF while reading a line of input, it should exit gracefully without reporting an error.

Ensure that you do not overflow a 180 byte buffer when fetching the line of input (functions that do not accept the size of your buffer are not able to prevent overflows whereas functions that do accept a size generally do; be sure to check the manpage of any function you use carefully). You do not need to report an error if the user’s input line is larger than the 180 byte buffer; just use the truncated input as the command.

You can test the EOF by running `make run &lt; commands.txt`

Before your shell forks a new process to call `execvp()`, it should parse the input string and separate it into a collection of substrings representing the executable file and any command-line arguments. If the user entered an empty line, report an error and fetch a new line of input. Your code must handle at least four command-line arguments (in addition to the name of the executable file itself).

You should store pointers to the substrings in an array (similar to the “argv” array passed to main()) and pass this array of arguments to execvp(). Note that the number of command-line arguments is variable; this is indicated in the array by including a NULL pointer in the array after the last substring. (This means that if the user specifies N substrings, your array must hold N + 1 pointers where the last pointer is NULL.) If the user enters the **exit** command, your shell should terminate (returning to the regular shell).

Note: your shell does not need to support `cd` (change directory).

Your program must also accept a command line argument which is the prefix prompt. If no value is specified use “&gt; ” as the prompt.

Here is a sample execution:

“`

student@student-VirtualBox:~/CSC415/assignment3$ ./assn3 prompt$

prompt$ ls -l

total 20

-rwxr-xr-x 1 student student 13216 Feb 23 13:44 assn3

-rw-r–r– 1 student student 1583 Feb 23 13:44 assn3.c

Child 2124, exited with 0

prompt$ ls foo

ls: cannot access ‘foo’: No such file or directory

Child 2125, exited with 2

prompt$ exit

student@student-VirtualBox:~/CSC415/assignment3$

“`

You should submit your source code file(s), and Makefile along with a short writeup in PDF format that includes a description of what you did issues you had and resolutions and the compilation and execution output (screen shots) from your program to GitHub and just the PDF also to iLearn. Your execution output should include commands with command-line arguments. Then use the exit command to exit your program and show the output of the same commands in the regular command-line interpreter for that machine to ensure they match.

All filenames should be `&lt;lastname&gt;_&lt;firstname&gt;HW&lt;#&gt;_&lt;optional&gt;.&lt;proper extension&gt;`

&nbsp;
