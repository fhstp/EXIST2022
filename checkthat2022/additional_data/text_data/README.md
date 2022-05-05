Note --> the 20M, 21M, 46M, etc. just give an insight in the amount of additional data used. The length of checkthat data is not included in the name of the merge!


_______________________________________________________________
Checkthat.txt -->  5388978 chars

_______________________________________________________________
English dataset (Fake & Real): 
https://www.kaggle.com/datasets/astoeckl/fake-news-dataset-german

Fake = 23481 rows
Real = 21417 rows
--> in originals directory


preprocessing=
- \r  \t and \n got removed


prepared dataset = 
Merged_english = 44898 rows (and shuffled!)
110902984 chars
--> prep_ENGLISH_news_shuffled.txt


cutted dataset = 10000rows
24461513 chars --> 25M
--> prep_ENGLISH_news_shuffled_short_25M_chars.txt

10000000  chars --> 10M
prep_ENGLISH_news_shuffled_10M.txt




__________________________________________________________________________________
German Dataset: 
 Fake News Dataset German 9cc110a2-9
 https://www.kaggle.com/code/kerneler/starter-fake-news-dataset-german-9cc110a2-9/notebook
 1000 rows and 9 columns
 	id	url	Titel	Body	Kategorie	Datum	Quelle	Fake	Art


len original = 63868 rows
len txt = 160017417 chars




preprocessing=
- \r  \t and \n got removed
- some html code/javascript code was in the text column. I removed these rows by searchin for "<div" and "<p>"
len after rows dropped = 63847
len txt = 159930087 chars
--> prep_GERMAN_news_short.txt

cutted dataset = 
10000rows
21093974 chars --> 21M
--> prep_GERMAN_news_short_20M_chars.txt

10000000  chars --> 10M
prep_GERMAN_news_short_10M_chars.txt



_______________________________________________________________________________________
Additional Merged= 

German + English News =
--> prep_MERGED_news.txt --> 270833071chars
--> prep_MERGED_news_short_46M_chars.txt --> 45555487 chars



Final Merge
Checkthat + German + English News =
- prep_Checkthat_MERGED_news.txt  --> 270833071chars
- prep_Checkthat_MERGED_news_Short_46M.txt --> 21093974 chars from English --> 21M & 24461513 chars from German--> 25M
- prep_Checkthat_MERGED_news_Short_20M.txt --> contains 10000000 chars of English und 10000000 of German Dataset + Checkthat
- prep_Checkthat_MERGED_news_Short_10M.txt --> contains 5000000 chars of English und 5000000 of German Dataset + Checkthat
- prep_Checkthat_MERGED_news_Short_5M.txt --> contains 2500000 chars of English und 2500000 of German Dataset + Checkthat


