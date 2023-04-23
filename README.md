Download Link: https://assignmentchef.com/product/solved-assignment-1-making-pretty-printer-for-c-programs-cmpt-470-816
<br>
<strong>What to do?</strong>

<strong> </strong>

<ol>

 <li>Look at the example grammars for C and Pascal at the “SupportMaterials” folder in Dropbox. In particular, look at how the Pascal grammar was gradually made. It followed kind of the same process as of the lectures in making the text, assignment and if-then-else grammars.</li>

</ol>




<ol start="2">

 <li>Now lets start making the C grammar for the example programs in folder “MakeCgrammar”. You will see that there are 18 such programs. I also provided some Txl programs for the first few ones. For example, input 1abc_input.c will be run with txl programs 1a.Txl, 1b.Txl and 1c.Txl. Similarly, input 2_input.c will run with 2.Txl. Use the command, <em>txl 1a.Txl 1abc_input.c</em> and so on to compile. You do the rest. Because you are making a pretty-printer, make sure input programs of any format becomes the same as per your grammar. The bottom line idea would be the input programs should be displayed kind of the same as they are currently now. Also look at the Pascal pretty-printer provided in folder SupportMaterials/Pascal_PrettyPrinter. This Pascal grammar will give you lots of hints for making the C grammar. [45 marks]</li>

</ol>




<ol start="3">

 <li>Now for each of the example programs, make another similar example with names 1b_input.c, 2b_input.c, …, and 18b_input.c. Make sure that your corresponding Txl program runs on the new programs and pretty print them as per your grammar. [15 marks]</li>

</ol>




<ol start="4">

 <li>The grammar you made in step 2 above should run the programs in the folder “miniCgrammar”. If so, you are at a very good stage. If not, refine the grammar, make it generalized enough and attempt to run the examples. They should pretty print any such programs. I provided an example as the starting point. Just run <em>txl StartingInput.c</em> <em>Txl</em> to see how it works. [30 marks]</li>

</ol>




<ol start="5">

 <li>Now make a couple of similar programs as of the examples (e.g., similar to input_4.c and input_5.c) in the folder “miniCGrammar” and run the grammar. If they pretty print well, you are done! [10 marks]</li>

</ol>




P.S. You might get lots of warning messages from TXL processor. You try to remove them. If not, no worries much.



















<strong>How to start working on the grammar?</strong>




As noted above, start writing TXL grammar for the simple ones and then move building the complex ones. However, for each stage keep a copy of the old ones. For example, you make a grammar for a small syntactic construct in txl file named 1.Txl and it has the corresponding input file named 1_input. When you are done making the grammar for 1_input, you copy 1.Txl to make 2.Txl. You then further work on 2.Txl so that it will handle both input files of 1_input and 2_input where 2_input contains your next syntactic construct. In this way, you develop the complete grammar where the final grammar will support all the input files. This is kind of version control system. However, instead of using the version control, we are just keeping the old copies and making the new ones. When all the syntactic constructs are covered, you will need to change the grammar so that it will now support nested statements.  For example, there might be a nested “if –then- else” statement inside of which there might be “for loop” and so on. You might want to try this first with a small example similar to the “if-then-else” statement I was showing in the lecture. You will need to submit all these small programs and their input files in Moodle as well. <strong>If you follow a different method of developing the grammar that is also okay. However, keep the intermediate programs as an evidence of how you have come to the final grammar. Provide appropriate comments in your grammar as well.</strong>

<strong> </strong>




<strong>Expected output?</strong>

<strong> </strong>

This assignment will help you learn of how to make a pretty-printer for the C programs and hence for any such languages thereafter. Any programs written in C in any formatting styles will produce the consistent formatting after you use this pretty-printer. This is kind of the tool <em>Artistic Style</em> (<a href="http://astyle.sourceforge.net/">http://astyle.sourceforge.net/</a>) which supports multiple languages. You will be a proud author of a pretty-printer for C language. Also note that you can now do lots of software analysis tasks with this. Just look at the TXL Cook book in the Readings (CourseMaterials/TXL/Readings) folder in the course in Dropbox. Covering full C language constructs would be difficult, and also the full C grammar is available in the TXL website. I am thus just expecting a mini C pretty-printer as of the examples provided in the assignment folder. Some highlights below:




<ol>

 <li>The print and read statements.</li>

</ol>




<ol>

 <li>The expression grammar for any expressions. You may have separate expression grammar for Boolean/conditional expressions as well. Feel free to copy from TXL website.</li>

</ol>




<ol>

 <li>The assignment statement including complex assignment statements.</li>

</ol>




<ol>

 <li>The method declarations and method calls. Note that some methods are built-in in the programming language of choice and some are user defined. You may want to distinguish them or you may consider them as same type (i.e., consider the method name as [id] or so). They may accept any number of parameters of different types in the declarations or in the method calls.</li>

</ol>




<ol>

 <li>The variable and constant declarations. You don’t need to support all the different types. If your grammar can accept integers, I believe you can also make for other types as well.</li>

</ol>




<ol>

 <li>The if-then and if-then-else statements including the complex conditional statements within their conditions such as the <em>if (i &gt; 1)&amp;&amp; (i &lt; 100)</em>. You might want to have a separate non-terminal for representing the conditional statements.</li>

</ol>




<ol>

 <li>The case/switch statement</li>

</ol>




<ol>

 <li>The for-loop statement</li>

</ol>




<ol>

 <li>The while-loop statement</li>

</ol>




<ol>

 <li>Make sure that you apply appropriate formatting clues to have consistent output.</li>

</ol>







<strong>How to submit?</strong>

<strong> </strong>

<ol>

 <li>Make a directory named as: Assgn1_ PatALastName_PatBLastName.</li>

</ol>




<ol start="2">

 <li>Copy the folders MakeCgrammar and MiniCgrammar including the both the TXL and input files in folder Assgn1_ PatALastName_PatBLastName.</li>

</ol>




<ol start="3">

 <li>Make a zip/tar file of Assgn1_ PatALastName_PatBLastName and submit to Moodle. In case you experience troubles in submitting in Moodle, just email me your submission.</li>

</ol>




<ol start="4">

 <li>Enjoy and please feel free to contact me if you have any questions. I am always available for my students, even at late night or during the weekend. I don’t mind getting your emails anytime you send. You will also get a reply at the earliest time possible, possibly within an hour or so. If you are successful (even partially) in making the grammar, your hard efforts of coming to this lecture is well paid off, at least in my opinion. My email id is: <a href="/cdn-cgi/l/email-protection#75161d141b161d14195b071a0c35000614061e5b1614"><span class="__cf_email__" data-cfemail="ef9d8096af9a9c8e9c84c18c8e">[email protected]</span></a></li>

</ol>











