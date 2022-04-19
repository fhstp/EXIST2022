### XLM-RoBERTa predictions

* **Pre-trained** on EXIST 2022 + additional datasets
* **Fine-tuned** on	EXIST 2022 + original and translated data (only **task 2**)
* No preprocessing
* Max. sequence length 256
* Trained 3 epochs with max. LR of 2e-5 and 3	epochs with max. LR of 1e-5 
* Batch size 8

#### Submission files
final_xlmr_task1.csv, final_xlmr_task2.csv

#### Softmax output
* ./softmax_output/softmax_train.csv, softmax_test.csv
* softmax_train.csv contains also translations (s. **"is_translated"** column)
* there are some duplicates in softmax_train.csv 

