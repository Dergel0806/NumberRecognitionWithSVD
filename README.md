# NumberRecognitionWithSVD

Number recognition with custom SVD and Least Squares methods.

Jupyter notebook contains same code as Rmd file, but Rmd has additional comments and clarifications.

## Problem statement

Given	a	set	of	manually	classified	digits,	classify	a	set	of	unknown	digits using	SVD	method.

## DataSet
US	postal	Service	database	that	contains	1707 training and	2007	test	digits.  
Each	image	is	a	grayscale	16x16	image	that	is	converted	to	a	256x1	column	vector by	stacking	all	the	columns	of	each	image	matrix above	each	other.

## Methodology

1. Form	a	matrix	A	for	each	digit,	such	that	each	row in	A	represents	an	image	of	that	digit.
1. Determine	the singular	value	decomposition	for each	A.  
Right singular vectors	$V_i$ are	an orthogonal	basis	in	the	image	space	of	that	digit. We	will	refer	to	the right singular	vectors	as “singular	images.”
1. Express	test	images	as	a	linear	combination	of	the	first	k=20 singular	images	of	each	digit.
1. Compute	the	distance	between	test	images	and	their	least	square	approximations.
1. Classify	each	test	image to	be	the	digit	corresponding	to	the	smallest	residual.	
1. Calculate	the	overall	correct	classification	rate,	as	well	as	correct	classification	rate	for	each	digit	
in	a	confusion	matrix.
