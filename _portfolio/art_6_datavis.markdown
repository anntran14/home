---
layout: post
title: Data Visualization
description: 
img: ../img/icons/catatonic-closeup.jpg
---

# overview
<br/> During Spring 2016, for our final project in CS 207: Data Science and Visualization, my team analyzed a data set of Haverford College Honor Code violations dating from Spring 1993. Categorical data included “Release Semester and Date”, “Confrontation Type”, and “Type of Trial”. We were asked to investigate the data set and explore any patterns in the trials. For example, if there were any case attributes that were surprising indicators of others. These analyses would be presented to the College’s 1,500-person student population. It would encourage students to self-reflect on the perceived versus actual role of the Honor Code.

# research and hyothesis
1. I created a network that used the k-nearest neighbors algorithm (k-NN) to connect points, the PageRank algorithm to size points, and "Confrontation Type" categorical data to color points. 

2. From 1., I wanted to explore if Confrontation Type is a deciding factor on other case attributes in order to observe the distinction between academic and social Honor Code trials. I used two different techniques to do so - visualizing case Trial Types with texture, and removing the Confrontation Type in two new network that use the same k-NN (k = 8) to link points.

3. Finally, I wanted to see if the data set still clustered by Confrontation Type when the attribute was removed. I hypothesized that in the new network, points of the same Confrontation Type would still cluster more closely together, and that there would be certain clusters of points with higher PageRank like in the original network. I also expected that points originally in the center of the graph would now either link more closely to a cluster’s center, since Confrontation Type may have been a dividing factor, or stretch far away from other cases if they were outliers.

# results


# analysis
We see in both new networks that a case’s attributes rely frequently on its Confrontation Type. In the textured network, the greatest takeaway is that often, Confrontation Type correlates to Trial Type. In the network with Confrontation Type removed, the greatest takeaway is that points of the same Confrontation Type usually contained common variables. Both networks affirm what was suspected, which is that there is a pattern to attributes depending on a trial’s Confrontation Type.

Both new graphs reinforce that the data set breaks down into two clusters, and these clusters are categories: academic or social Honor Code violations. Furthemore, they also only corroborated the idea that there are common contexts and protocols in those clusters. Sadly, the notion that underlying patterns in the trials exist undermines the hope that Honor Code infractions are anomalies of Haverford’s long-held tradition of principles.

# reflection
The data shows that Haverford administration may play a greater role in administering the Honor Code than expected. This goes against the average student’s perception of the Code as a set of social and academic expectations run by, administered by, and agreed upon by students.

To research the role of Confrontation Type as an indicator for trial details, I generated two new networks where points were still linked using k-NN (k = 8). The first network textured points based on the Trial Type they were related to, and the second was generated without the “Confrontation Type” attribute, yet colored according to it. Both networks produced two clusters, one with mainly Confrontation Type (1), and the other with Confrontation Types (2), (4), and (7). The textured network revealed Trial Types as a common attribute to points within a cluster. The network that removed Confrontation Type revealed that when comparing all attributes, points with the same Confrontation Type usually still shared features. This suggests an underlying structure within case protocol and context, which juxtaposes the principles of the Code that say that regardless of either, students are expected to follow the system.

Presenting Code violations to students as visualizations may shed light on the reality of the nature of the Honor Code, where most cases actually rely on administrative leads and all cases link to common features. Recently, a friend of mine was on trial for plagiarizing, and she admitted to me that the Honor Code felt intangible compared to the reality of her grades. I agreed that the Code is viewed in an idyllic light rather than a concrete one, as seen in the email’s self-disciplinary expectation. Essentially, all of my networks show that other students have made mistakes at Haverford College. Visualizing these mistakes may guide students to see the students put on trial, trial repercussions, and the restorative processes for students as concrete and effective.

You can download the full analysis here.

