Download Link: https://assignmentchef.com/product/solved-math-281-workbook-1
<br>



<h2>Contents</h2>

<a href="#_Toc4885"><strong>1 Project Outline</strong>                                                                                                                                                                                               <strong>2</strong></a>

<a href="#_Toc4886"><strong>2 Workbook Questions [20 points total]</strong>                                                                                                                                       <strong>3</strong></a>




<h1><a name="_Toc4885"></a>1                 Project Outline</h1>

The term project is divided into three section, each with a corresponding Jupyter workbook. Each workbook will ask you to investigate various aspects of numerical methods or PDEs. You will then be expected to submit a PDF report for each workbook, answering the questions. You are also expected to submit your workbooks (.ipynb files) along with your reports. The code, if run by the instructors / TAs, should reproduce the figures included in your reports. <em>You will submit the documents to Gradescope.</em>

<strong>Notes about Grading        </strong>Your grade on the reports will depend on:

<ul>

 <li>The over-all organization of your work</li>

 <li>The completeness and clarity of your answers</li>

 <li>How well you substantiate your claims with results (i.e. soundness of, and reference to, numerical findings), and how you connect the results to the underlying mechanics.</li>

 <li>How well you present your numerical findings (i.e. quality of graphs [note: quantity is not the same as quality!])</li>

</ul>

<strong>Note about Figures        </strong>Take care with your graphs. Some things to consider are:

<ul>

 <li>labeling (what is plotted on the axes? What are their units [if any]?)</li>

 <li>legibility (labels, axis numbers, etc should be large enough to be easily read when included in the report</li>

 <li>captions are a useful way to give a (brief) explanation of what is shown in a figure.</li>

</ul>

<h1><a name="_Toc4886"></a>2             Workbook Questions [20 points total]</h1>

<ol>

 <li>(a) [2 marks] Suppose that we have a spatial domain <em>x </em>∈ [0<em>,</em>1]. Using <em>u</em>(<em>x</em>) = sin(2<em>πx</em>), numerically compute the derivative for three grids:

  <ul>

   <li>{0<em>,</em>0<em>.</em>1<em>,</em>0<em>.</em>2<em>,…,</em>0<em>.</em>9}</li>

   <li>{0<em>.</em>05<em>,</em>0<em>.</em>15<em>,</em>0<em>.</em>25<em>,…,</em>0<em>.</em>95}</li>

   <li>{0<em>,</em>0<em>.</em>1<em>,</em>0<em>.</em>2<em>,…,</em>1<em>.</em>0}</li>

  </ul></li>

</ol>

A partial solution is provided in the workbook that computes the derivative for the first grid. Create a plot comparing the three solutions (basic plot started in sample solution). What differences, if any, are there between the three solutions, and what causes them?

You should create a final plot that shows the three derivatives together to support your answer.

(b) [2 marks] Consider the function <em>u</em>(<em>x</em>) = exp(−<em>x</em><sup>2</sup>) on a series of grids ranging from <em>x </em>∈ [−1<em>,</em>1], <em>x </em>∈ [−2<em>,</em>2], <em>x </em>∈ [−3<em>,</em>3], and <em>x </em>∈ [−5<em>,</em>5], each with the same spacing of ∆<em>x </em>= 0.1.

Compute <em>du/dx </em>for each grid using the second-order scheme, and plot the derivatives on the same graph. Nominally, these would all be the same (they’re derivatives of the same function). What differences do your observe, and what causes them?

The last case (Lx = 10) is already completed in the workbook.

<ol start="2">

 <li>[5 marks]</li>

</ol>

The provided code uses 2nd and 4th order finite difference approximations to compute the derivative of sin(<em>x</em>) for various values of ∆<em>x</em>. The error is then plotted as a function of the resolution, which illustrates the order of convergence. That is, as ∆<em>x </em>decreases, the error in the computed derivative decreases. More-over, the second order scheme decreases at the same rate as ∆<em>x</em><sup>2</sup>, while the fourth order scheme decreases at the same rate as ∆<em>x</em><sup>4</sup>.

If you change the variable ‘Nmodes’ to be 10, the code will produce the results for sin(10<em>πx</em>).

Describe the change in the error curve, and provide an explanation [hint: what happens for large ∆<em>x</em>?].

The plots of the derivatives (also included in the provided code) may be useful.

<ol start="3">

 <li>[5 marks] We saw that a basic scheme for stepping forwards in time is</li>

</ol>

In this question you will investigate the impact of the choice of ∆<em>t </em>on the solution.

For the set of ODEs below, you need to:

<ul>

 <li>Compute the analytic (true) solution</li>

 <li>Numerically integrate over the specified time range to get the approximate solution.</li>

 <li>Compare the numerical results to the analytic results, and discuss the impact of ∆<em>t</em></li>

 <li>What can you say about the long-term trend in the error? Is this different from the other cases?</li>

</ul>

Why or why not?

ODEs to consider:

) from <em>t </em>= 0 to <em>t </em>= 2. <em>u</em>(0) = 0. Use ∆<em>t </em>= 0<em>.</em>01<em>,</em>0<em>.</em>05<em>,</em>0<em>.</em>2  from <em>t </em>= 0 to <em>t </em>= 100. <em>u</em>(0) = 0<em>.</em>01. Use ∆<em>t </em>= 0<em>.</em>001<em>,</em>0<em>.</em>01<em>,</em>0<em>.</em>05. You may want to use a

log-y plot.

= 2 from <em>t </em>= 0 to <em>t </em>= 10. <em>u</em>(0) = 0<em>.</em>. Use ∆<em>t </em>= 0<em>.</em>01<em>,</em>0<em>.</em>1<em>,</em>1<em>.</em>0.

The workbook includes a sample solution for .

<ol start="4">

 <li>[6 marks]</li>

</ol>

Consider the following PDE:

<ul>

 <li><em><u>∂u</u></em><em>∂t </em>= <em><u>∂u</u></em><em>∂x</em></li>

 <li><em>u</em>(0<em>,x</em>) = exp(−<em>x</em><sup>2</sup>)</li>

 <li><em>x </em>∈ [−5<em>,</em>5] (periodic domain)</li>

 <li><em>t </em>∈ [0<em>,</em>10]</li>

</ul>

Recall that our (simplest) differentiation schemes are:

Putting these into our PDE, we get

The provided code computes a numerical solution for a given ∆<em>x </em>and CFL coefficient. Repeat the process for a selection of CFL coefficients: 0.5, 0.1, 0.01.

What kind of errors do you observe? (i.e. describe the physical appearance of the error terms).

Using trial and error (i.e. pick some numbers to try), how large can you reasonable take your CFL factor? Explain your reasoning. [Note: we’re not looking for a specific answer here, but rather your reasoning and justification].