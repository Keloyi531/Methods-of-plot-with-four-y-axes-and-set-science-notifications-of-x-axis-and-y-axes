Prenotice:
The founction in this code is based on the function "move_sn_y()" from a blog of "werthmuller.org", link: https://werthmuller.org/blog/2014/move-scientific-notation/.
And also based on the matplotlib tutorial.

Result:

![image](https://github.com/Keloyi531/Methods-of-plot-with-four-y-axes-and-set-science-notifications-of-x-axis-and-y-axes/blob/main/pic_move_sn_multiAxes/Result.png)

Once I need to illustrate the experimental data and need to plot a graph with four y-axes, but the y-ticks were overlaped on the second y-axis because of the extra fourth y-axis. At that time, the answer that could solve the overlap problem of double y-axis can't solve my problem. In another way, it can be solved by erase the overlaped ticks by PS, but I want to solve this problem fundamentally.
Overlap like this:

![image](https://github.com/Keloyi531/Methods-of-plot-with-four-y-axes-and-set-science-notifications-of-x-axis-and-y-axes/blob/main/pic_move_sn_multiAxes/Overlap_ticks.png)

So I modified the code continuously and even tried to modify the source code of the functions, so confused. Once by a mistake, I found that just write the code at line 19 as par3.axis["right"], not par3.axis["left"], although the y4-axis is on the left, the problem is solved...... If you know the reason why, please tell me about this.
Considering a situation that the x and y data need to be displayed in scientific notation format. I searched and got the "move_sn_y()" of set the format and location of y-tick-label, then applied it to my work. The figsize and location parameters aren't perfect, you can change it in your need.

A problem: If just write one function to set x-axis and y-axis, the science notifications will overlap, looks like the font is bolded. 

![image](https://github.com/Keloyi531/Methods-of-plot-with-four-y-axes-and-set-science-notifications-of-x-axis-and-y-axes/blob/main/pic_move_sn_multiAxes/Overlap_notification.png)

So I set the founctions of setting these two axes separately, and the code also looks cleaner. The one function setting method also showed in this repository, named "Set x and y axis in one function, overlap notificaiton".
