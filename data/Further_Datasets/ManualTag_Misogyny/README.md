Title: ManualTag_Misogyny.csv
Author: Lynn et al
Year: 2019
Task: two columns: the text-based definition from Urban Dictionary and its respective classification.
Description: 2,285 definitions gathered from the Urban Dictionary platform from 1999 to 2006.
URL Code: http://dx.doi.org/10.17632/3jfwsdkryy.3

Labels:
1 for misogynistic and 0 for non- misogynistic



Latest version
Version 3
Published:
23-04-2019
DOI:
10.17632/3jfwsdkryy.3
Cite this dataset

Lynn, Theodore; Endo, Patricia Takako; Rosati, Pierangelo; Silva, Ivanovitch; Santos, Guto Leoni; Ging, Debbie (2019), “Urban Dictionary definitions dataset for misogyny speech detection”, Mendeley Data, V3, doi: 10.17632/3jfwsdkryy.3

http://dx.doi.org/10.17632/3jfwsdkryy.3





___________________________________TO DO: ________________________________________________________


Preprocessing: 
______________

	remove: 
		
		- punctuation, 
		- change label value: 
			- is_misogyny "0" => " non-misogyny
			- HS "1" => " mysogyny
		- remove \r\n\r\ (and its variants)
		- (add id (?))
		- filter women related tweets with poposed keyword set 



Last modified: JB - 30.03.2021