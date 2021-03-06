---
layout: post
title: Data Visualization
description: 
img: ../img/icons/cluster.jpg
---

# overview
<br/> During Spring 2016, for our final project in CS 207: Data Science and Visualization, my team analyzed a data set of Haverford College Honor Code violations dating since Spring 1993. Categorical data included “Release Semester and Date”, “Confrontation Type”, and “Trial Type”. We were asked to investigate the data set and explore any patterns in the trials. For example, if there were any case attributes that were surprising indicators of others. These analyses would be presented to the College’s 1,500-person student population to encourage students to reflect on the perceived versus actual role of the Honor Code.


# research and hypothesis
<br/> 
1. I created a network that used the k-nearest neighbors algorithm (k-NN) to connect points, the PageRank algorithm to size points, and "Confrontation Type" categorical data to color points. 

2. From 1., I wanted to explore if Confrontation Type is a deciding factor on other case attributes in order to draw a distinction between academic and social Honor Code trials. I used two different techniques to do so - visualizing case Trial Types with texture, and removing the Confrontation Type in two new network that use the same k-NN (k = 8) to link points.

3. Finally, I wanted to see if the data set still clustered by Confrontation Type when the attribute was removed. I hypothesized that in the new network, points of the same Confrontation Type would still cluster more closely together, and that there would be certain clusters of points with higher PageRank like in the original network. I also expected that points originally in the center of the graph would now either link more closely to a cluster’s center, since Confrontation Type may have been a dividing factor, or stretch far away from other cases if they were outliers.


# results

<div class="imag_row">
	<img class="col three" src="../../img/datavis/1-original.png" alt="" />
</div>
<div class="col three caption">
1. Visualization of Honor Code network using the k-NN algorithm (k = 8) to link points, the PageRank algorithm to size points, and "Confrontation Type" categorical data to color points. The red circles indicate inner clusters identified by pageRank. </div>

<div class="imag_row">
	<img class="col three" src="../../img/datavis/2-texture.png" alt="" />
</div>
<div class="col three caption"> 2. Visualization of Honor Code network using the k-NN algorithm (k = 8) to link points. Point colors are based on "Confrontation Type" and point textures are based on only two Trial Types. Otherwise, points are not textured. </div>

<div class="imag_row">
	<img class="col three" src="../../img/datavis/3-noconfrontationtype.png" alt="" />
</div>
<div class="col three caption">
3. Visualization of Honor Code network with “Confrontation Type” attribute removed. It uses the k-NN algorithm (k = 8) to link points, the PageRank algorithm to size points, and "Confrontation Type" categorical data to color points. </div>

# analysis
<br/> We see in both new networks that a case’s attributes rely frequently on its Confrontation Type. In the textured network, the greatest takeaway is that often, "Confrontation Type" correlates to "Trial Type". In the network with Confrontation Type removed, the greatest takeaway is that points of the same Confrontation Type usually contained common variables. Both networks affirm what was suspected, which is that there is a pattern to attributes depending on a trial’s Confrontation Type.

Both new graphs reinforce that the data set breaks down into two clusters, and these clusters are categories: academic or social Honor Code violations. Furthemore, they also only corroborated the idea that there are common contexts and protocols in those clusters. Curiously, the underlying pattern found in the trials undermines the notion that Honor Code infractions are anomalies of Haverford’s long-held moral traditions.


# reflection
<br/> The data shows that Haverford administration may play a greater role in administering the Honor Code than expected. This goes against the average student’s perception of the Code as a set of social and academic expectations run by, administered by, and agreed upon by students.

To research the role of "Confrontation Type" as an indicator for trial details, I generated two new networks where points were still linked using k-NN (k = 8). The first network textured points based on the "Trial Type" they were related to, and the second was generated without the “Confrontation Type” attribute, yet colored according to it. Both networks produced two clusters, one with mainly "Confrontation Type" (1), and the other with "Confrontation Types" (2), (4), and (7). The textured network revealed "Trial Type" as a common attribute to points within a cluster. The network that removed "Confrontation Type" revealed that when comparing all attributes, points with the same "Confrontation Type" usually still shared features. This suggests an underlying structure within case protocol and context, which juxtaposes the principles of the Code that say that regardless of either, students are expected to follow the system.

Presenting Code violations to students as visualizations may shed light on the real nature of the Honor Code, where most cases actually rely on administrative leads and all cases link to common features. Visualizing these violations may guide students to see the students put on trial, trial repercussions, and the restorative processes for students as concrete and effective.

<a href="http://anntrandesign.com/img/AnnTran-HonorCode.pdf">You can download the full analysis here.</a>
