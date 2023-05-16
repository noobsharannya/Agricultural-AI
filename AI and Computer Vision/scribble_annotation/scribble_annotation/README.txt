----------------------
ScribbleSup: Scribble-Supervised Convolutional Networks for Semantic Segmentation
----------------------

The data corresponds to the scribbles provided by the annotators. The scribbles are stored as xml file for each image. 

The format of each xml file is like:

<annotation>
	<folder>anno</folder>
	<filename>000001.png</filename> \\ The file name of the image
	<source>
		...
	</source>
	<owner>
		...
	</owner>
	<size>
		<width>706</width>          \\ The width of the image
		<height>500</height>        \\ The height of the image
		<depth>3</depth>            \\ The depth of the image
	</size>
	<segmented>1</segmented>
	<polygon>                       \\ The start of a scribble
		<tag>person</tag>
		<point>                     \\ The coordinate of a pixel in the scribble
			<X>167</X> 
			<Y>46</Y>
		</point>
		...
	</polygon>                      \\ The end of a scribble
</annotation>

The folder "pascal_2007", "pascal_2012" and "pascal_context" respectively contain the scribbles on the PASCAL VOC 2007, 2012 
and PASCAL-CONTEXT datasets. We provide a demo which reads a xml file and visualizes the scribbles using MATLAB
script. Please check the script named "visualize.m" in the folder "demo".