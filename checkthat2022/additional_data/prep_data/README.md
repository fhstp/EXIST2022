English dataset (Fake & Real): 
https://www.kaggle.com/datasets/astoeckl/fake-news-dataset-german

Fake = 23481 rows
Real = 21417 rows

prepared dataset = 
Merged = 44898 rows (and shuffled!)
\r  \t and \n got removed
__________________________________________________________________________________
German Dataset: 
 Fake News Dataset German 9cc110a2-9
 https://www.kaggle.com/code/kerneler/starter-fake-news-dataset-german-9cc110a2-9/notebook
 1000 rows and 9 columns
 	id	url	Titel	Body	Kategorie	Datum	Quelle	Fake	Art


len original = 63868 rows
preprocessing=
some html code/javascript code was in the text column. I removed these rows by searchin for "<div" and "<p>"
len after rows dropped = 63847



___FINAL____________________
len texts: 
English(shuffled) = 59838891
German = 160017415

Merged = 219856306

Translated Checkthat data: 
- prep_CheckThat_merged_shuffled_train.txt merged_shuffled_train = 7974455 chars
- prep_CheckThat_merged_shuffled_dev.txt merged_shuffled_val =3488162