Download Link: https://assignmentchef.com/product/solved-csde502-homework4
<br>
<strong>Instructions:  </strong>

<ol>

 <li>Create an R Markdown Rmd file and render it to a self-contained HTML file. Use the output format <strong>bookdown::html_document2</strong> in the YAML header so you can use various methods of cross referencing. Feel free to use any of the code examples provided or any other resources at your disposal.</li>

 <li>Upload both the Rmd and HTML files to the course Canvas site</li>

</ol>

<a href="https://canvas.uw.edu/courses/1434040">(</a><a href="https://canvas.uw.edu/courses/1434040">https://canvas.uw.edu/courses/1434040</a><a href="https://canvas.uw.edu/courses/1434040">)</a>. Upload two separate files rather than creating a zip file.




<strong>Guidelines: </strong>

Make sure your document includes at least the following:




<ul>

 <li>Your name and contact information</li>

 <li>Date of creation</li>

 <li>A table of contents</li>

 <li>Sequentially numbered section headers for each question</li>

 <li>Any additional R Markdown elements to make your document easier to navigate, read, and understand. All tables and figures should be captioned and cross-referenced.</li>

 <li>Source code for the Rmd at the end of the document</li>

 <li>For any data driven values reported in the text (e.g., mean of a vector), use the construction</li>

</ul>

`r somecode`

<ul>

 <li>Pay attention to the number of decimal places you report</li>

</ul>




<strong>Explanation: </strong>

This assignment will build your skills in writing R functions. Functions are particularly useful if you will be running the same set of operations multiple times on different data sets that have the same structure. For example if you wanted to make identical bar plots from the Add Health race and ethnicity variables, it would be more efficient to write a function rather than copying-andpasting a block of code and making a series of small edits.




This exercise uses an example of bootstrapping: sampling <em>with replacement</em> from a sample of size <em>n</em>, many samples of size <em>n</em>.




Figure 1 shows simulated data for a hypothetical study asking graduate students to rate graduate school on a pain scale from zero to 10, where zero is no pain and 10 is the worst pain imaginable. You are going to resample from this data and look at the distribution of the mean.







Figure 1: Survey results on pain of graduate school




Create the data using the following R statement:




gradpain &lt;- c(rep(0,11), rep(1,1), rep(2,2), rep(3,6), rep(4,8), rep(5,10),               rep(6,8), rep(7,30), rep(8,10), rep(9,6), rep(10,2))




FYI: The plot was created with the following R statement:




barplot(table(gradpain), las=1, ylab=”Frequency”, xlab=”Pain Scale”,         main=”How painful is graduate school?”)




<strong>Answer the following questions: </strong>




<ol>

 <li>How many graduate students are in the sample? Use R code to determine this.</li>

</ol>




<ol start="2">

 <li>What is the sample mean?</li>

</ol>




<h1>Box 1</h1>

Create a function, with these arguments:

<ol>

 <li>the vector of data: “d.vec”</li>

 <li>the size of the sample: “n”</li>

</ol>

The function will sample <strong><em>with replacement</em></strong> a sample of size “n” from the vector “d.vec”. The function will return a <em>list</em> that contains

<ol>

 <li>the size of the sample</li>

 <li>the mean of the sample</li>

</ol>




<h1>Box 2</h1>

Use <sub>set.seed(7)</sub> then run your function passing in the “gradpain” vector calculated above and a sample size of <sub>length(gradpain)</sub>. Use a loop to do this 100 times and store all 100 returned means.




<ol start="3">

 <li>What is the mean of these 100 means?</li>

</ol>




<ol start="4">

 <li>What is the standard deviation of these 100 means?</li>

</ol>




<table width="639">

 <tbody>

  <tr>

   <td width="639"><strong>Box 3 </strong>Write another function that performs the steps listed in Box 2. That should be a function with these arguments:1.  the vector of data: “d.vec”2.  the size of the sample: “n”3.  the number of samples: “num.samples” The function should sample <strong><em>with replacement</em></strong> a sample of size “n” from the vector “d.vec” and does this “num.samples” times. The function should return a <em>list</em> that contains1.  the size of each sample2.  the number of samples3.  a vector of length num.samples with the mean of each sample4.  the mean of the means5.  the standard deviation of the means6.  the 95% confidence interval around the mean Run your function with the three argumentsd.vec = gradpain, n = length(gradpain), num.samples = 100</td>

  </tr>

 </tbody>

</table>




<ol start="5">

 <li>What does your function return for the mean of means?</li>

</ol>




<ol start="6">

 <li>What does your function return for the standard deviation of means?</li>

</ol>




<ol start="7">

 <li>What does your function return for the 95% confidence interval around the mean?</li>

</ol>


