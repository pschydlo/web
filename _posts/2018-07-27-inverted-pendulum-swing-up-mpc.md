---
layout: post
title:  "Inverted Pendulum Swing Up Model Predictive Control"
date:   2018-07-27 18:25:33 +0100
categories: 'control theory'
---
<p class="abstract">
Reinforcement learning has been applied with remarkable sucess in some classical control problems [1]. While this seems to indicate a good potential for more applications it is still important to look at these problems from a classic perspective to: first, have a strong understanding of how the field developed and, second, to have a broad palette of solutions.
</p>

<p>
One such problem is the so called Inverted Pendulum Swing-up problem. This problem's objective is to balance a pendulum in an upright position starting from a resting position, as can be seen in this demonstration video from the University of São Paulo:
</p>

<div class="figure">
<iframe class="video" src="https://www.youtube.com/embed/1svmVlx7UFw?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
<span class="caption center"> Vid. 1 - Inverted Pendulum Swingup</span>
</div>

In this article we will go over all the steps required to solve this problem with the Model Predictive Control (MPC) framework:
<ol>
<li><b>Mathematically modelling</b> the systems dynamics using the Lagrangian method. </li>
<li><b>Problem formulation</b> in an optimization setting, defining the cost function and constraints. </li>
<li><b>Optimization</b> solving the problem numerically.</li> 
</ol>

<h3> <b>1. Mthemtic Moe </b></h3>


<div class="figure">
<img src="/assets/inverted_pendulum.png"><br>
<span class="caption"> Fig. 1 - Inverted Pendulum</span>
</div>
