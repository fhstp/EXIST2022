# EXIST2022
Github repo for EXIST, the first shared task on sEXism Identification in Social neTworks at IberLEF 2022.



## Team
* Andresel Medina (<Medina.Andresel@ait.ac.at>)
* Babic Andreas (<mt191075@fhstp.ac.at>)
* Boeck Jaqueline (Jaqueline.Boeck@fhstp.ac.at>)
* Hecht Manuel (<mt191064@fhstp.ac.at>)
* Kirchknopf Armin (<Armin.Kirchknopf@fhstp.ac.at>)
* Lampert Jasmin <Jasmin.Lampert@ait.ac.at>)
* Liakhovets Daria (<Daria.Liakhovets.fl@ait.ac.at>)
* Alexander Schindler (<alexander.schindler@ait.ac.at>)
* Schlarb Sven (<Sven.Schlarb@ait.ac.at>)
* Schütz Mina (<Mina.Schuetz@ait.ac.at>)
* Slijepčević Djordje (<Djordje.Slijepcevic@fhstp.ac.at>)
* Strebl Julia (<Julia.Strebl@fhstp.ac.at>)
* Zeppelzauer Matthias (<Matthias.Zeppelzauer@fhstp.ac.at>)

## Literature Research
[Link to Literature Research from EXIST2021](https://teamwork.fhstp.ac.at/quickteams/home/CVPR_JF/_layouts/15/WopiFrame2.aspx?sourcedoc=%7B57EDB0F6-E970-4665-974E-9EF63C776639%7D&file=Literature_Research_EXIST.xlsx&action=default)

## Data
Please use the fixed training and validation splits for your experiments.
* Training/validation splits (80/20%): s. data/EXIST_train_val_split
* **IMPORTANT** Translated training/validation splits:
    - Use **data/EXIST_train_val_split/merged_train.csv** for training and
    - Use **data/EXIST_train_val_split/val.csv** for validation
    - If you are experimenting with monolingual models: Create your own merge with a correct "language" indicator. 
    - Only translated: data/EXIST_train_val_split/transl_train.csv
    - Original + translated: data/EXIST_train_val_split/merged_train.csv
* Preprocessed data for language model fine-tuning: s. data/for_pretraining

## Approaches
##### Note: T5 for Task 2 cant't be used for solving Task 1 (Transformer does not know the class "sexist")

## Results / Task_1 (Validation Data)

| Model    | Approach    | Pretraining Data   | Finetuning Data 	| Acc | Precision (macro) | Recall (macro) | F1 (macro)  | Added by: |
| -------------- | --------------------- | --------------------- |	--------------------- | :-------: | :-------: | :-------: | :-------: | ---------- |
| mBERT | Baseline | EXIST 2022	| EXIST 2022 (task2) 	| 74.88%    | 76.47%    | 75.08%    | 74.59%   | MS |
| mBERT | Baseline | EXIST 2022	| EXIST 2022  	| 73.42%    | 73.70%    | 73.29%    | 72.17%   | MS |
| BERT | Baseline | EXIST 2022	| EXIST 2022 	| 81.1%    | 83%    | 83%    | 82.4%   | AB |
| XML-RoBERTa | Baseline | EXIST 2022	| EXIST 2022 (task2) 	| 82.18%    | 79.63%    | 87.24%    | 83.26%   | DL |
| XML-RoBERTa | Baseline | EXIST 2022+additional datasets	| EXIST 2022  (task2)	| 82.02%    | 79.91%    | 86.32%    | 82.99%   | DL |
| T5(Task1 Model) | Baseline | EXIST 2022	| EXIST 2022 	| 83.54%    | 83.60%    | 83.50%    | 83.52%   | JB |
| T5(Task1 Model) | Baseline | EXIST 2022 +additional datasets	| EXIST 2022 	| 83.39%    | 83.29%   | 83.29%    | 83.30%   | JB |
| T5(Task1 Model) | Baseline | EXIST 2022 +additional datasets	| EXIST 2022 + additional datasets 	| 82.57%    |   82.64%  | 82.53%    | 82.54%   | JB |

## Results / Task_2 (Validation Data)

| Model | Approach    | Pretraining Data   | Finetuning Data 	| Acc | Precision (macro) | Recall (macro) | F1 (macro)  | Added by: |
| -------------- | --------------------- | --------------------- |	--------------------- | :-------: | :-------: | :-------: | :-------: | ---------- |
| mBERT | Baseline | EXIST 2022	| EXIST 2022 	| 76.82%    | 71.50%    | 71.74%    | 71.53%   | MS |
| BERT | Baseline | EXIST 2022	| EXIST 2022	| 73.8%    | 68%    | 70%    | 68%   | AB |
| XML-RoBERTa | Baseline | EXIST 2022	| EXIST 2022 	| 69.48%    | 61.12%    | 63.82%    | 62.25%   | DL |
| XML-RoBERTa | Baseline | EXIST 2022+additional datasets	| EXIST 2022 	| 70.80%    | 63.31%    | 65.78%    | 64.40%   | DL |
| T5 | Baseline | EXIST 2022	| EXIST 2022 	| 75.19%    | 69.60%    | 70.21%    | 69.70%   | JB |
| T5 | Baseline | EXIST 2022 + additional datasets	| EXIST 2022 	| 75.47%    | 69.39%    | 71.46%    |70.30%   | JB |

## Results / Experiments (Validation Data)

| Model | Approach | Pretraining (PT)  | Finetuning (FT) | Preproc. (PT) | Preproc. (FT) | Acc | Prec (macro) | Rec (macro) | F1 (macro)  | Added by: | Epochs (FT) | Batchsize (FT) | MaxSeqLen (FT) | LearningRate (FT) | 
| -------------- | --------------------- | --------------------- |	--------------------- | :-------: | :-------: | :-------: | :-------: | ---------- | :-------: | :-------: | :----------: | ---------- | ---------- | ---------- |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 84.39%    | 84.52%    | 84.14%    | 83.44%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 1 | 83.27%    | 83.46%    | 83.23%    | 82.30%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 2 | 82.92%    | 82.86%    | 82.63%    | 81.77%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 3 | 83.85%    | 83.98%    | 83.59%    | 82.82%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 83.70%    | 83.32%    | 83.55%    | 81.46%   | MS | 6 | 8 | 128 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 83.31%    | 83.12%    | 82.65%    | 80.85%   | MS | 10 | 8 | 128 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 | EXIST 2022 + add data | none | none | 84.43%    | 84.73%    | 84.43%    | 83.48%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 | EXIST 2022 + add data | none | none | 84.55%    | 84.96%    | 84.43%    | 83.46%   | MS | 10 | 16 | 256 | 2e-5 (warmup1000)|
| mBERT | Task 1 | EXIST 2022 | EXIST 2022 + transl data | none | none | 83.93%    | 84.04%    | 83.80%    | 83.00%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022  + add data | EXIST 2022 + transl data | none | none | 84.43%    | 84.32%    | 84.11%    | 83.39%    MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022  + add data | EXIST 2022 + add data + transl data | none | none | 84.12%    | 84.15%    | 83.99%    | 83.19%    MS | 10 | 16 | 256 | 2e-5 |
| mBERT (FINAL) | Task 1 | EXIST 2022 + add data + tweets | EXIST 2022 + add data | none | none | 85.29%    | 85.51%    | 85.15%    | 84.37%   | MS | 7 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data + tweets | EXIST 2022 + add data | none | none | 85.02%    | 84.68%    | 84.87%    | 82.87%   | MS | 8 | 8 | 256 | 1e-5 |
| mBERT | Task 1 | EXIST 2022 + add data + tweets | EXIST 2022 + add data | none | none | 84.36%    | 84.60%    | 84.17%    | 83.47%   | MS | 10 | 16 | 256 | 2e-5(warmup1000) |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 81.56%    | 81.76%    | 81.49%    | 81.50%   | DL | 3 | 8 | 128 | 1e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 82.37%    | 82.46%    | 82.32%    | 82.34%   | DL | 3 | 8 | 128 | 2e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 84.39%    | 84.39%    | 84.38%    | 84.38%   | DL | 3/2 | 8 | 128 | 2e-5/1e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 | EXIST 2022 + add data | none | none | 83.19%    | 83.38%    | 83.12%    | 83.14%   | DL | 3 | 8 | 128 | 2e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 | EXIST 2022 + add data | none | none | 84.78%    | 84.88%    | 84.73%    | 84.75%   | DL | 3/2 | 8 | 128 | 2e-5/1e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 (task 2) | none | none | 85.28%    | 83.26%    | 88.92%    | 85.99%   | DL | 3/2 | 8 | 256 | 2e-5/1e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 + transl data (task 2) | none | none | 85.40%    | 83.77%    | 88.38%    | 86.02%   | DL | 3/2 | 8 | 256 | 2e-5/1e-5 |
| XLM-RoBERTa (FINAL) | Task 1 | EXIST 2022 + add data | EXIST 2022 + transl data (task 2) | none | none | 85.90%    | 84.37%    | 88.69%    | 86.48%   | DL | 3/2+1 | 8 | 256 | 2e-5/1e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 + transl data + add data | none | none | 84.74%    | 84.74%    | 84.73%    | 84.73%   | DL | 3/2+1 | 8 | 256 | 2e-5/1e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 | EXIST 2022 | none | none | 84.89%    | 85.06%    | 84.84%    | 84.86%   | DL | 3/2 | 8 | 128 | 2e-5/1e-5 |
| T5 (FINAL)| Task 1 | EXIST 2022| EXIST 2022| none | none | 83.39%    | 83.29%   | 83.29%    | 83.30%   | JB | 9 | 4 | 512 | 1e-4 |
| T5 | Task 1 | EXIST 2022 + add | EXIST 2022| yes lr=1e-4 | none | 82.92%    | 83.09%   | 82.86%    | 82.88%   | JB | 8 | 4 | 128 | 1e-4 |
| T5 | Task 1 | EXIST 2022 + add | EXIST 2022| yes lr=1e-4 | none | 83.39%    | 83.29%   | 83.29%    | 83.30%   | JB | 8 | 4 | 512 | 1e-4 |
| T5 | Task 1 | EXIST 2022 + add | EXIST 2022 + add| none retrain lr=1e-4 | none | 80.43%    | 82.09%   | 81.99%    | 82.09%   | JB | 8 | 4 | 128 | 1e-4 |
| T5 | Task 1 | EXIST 2022 + add | EXIST 2022 + add| none retrain lr=1e-4 | none | 82.03%    | 82.64%   | 82.53%    | 82.00%   | JB | 9 | 4 | 512 | 1e-4 |
| T5 | Task 1 | EXIST 2022 + add | EXIST 2022 + add| none retrain lr=3e-4 | none | 82.03%    | 82.64%   | 82.53%    | 82.54%   | JB | 7 | 4 | 512 | 1e-4 |
| T5 | Task 1 | EXIST 2022 | EXIST 2022 + add| none  | none | 82.53%    | 82.60%   | 82.57%    | 82.53%   | JB | 9 | 4 | 512 | 1e-4 |
| T5 | Task 1 | EXIST 2022 | EXIST 2022 + add| none  | none | 81.56%    | 82.00%   | 81.46%    | 81.46%   | JB | 9 | 4 | 512 | 3e-4 |
| T5 | Task 1 | EXIST 2022 | EXIST 2022 + transl data | none  | none | 83.07%    |  83.38%  | 83.00%    | 83.01%   | JB | 8 | 4 | 512 | 1e-3 |
| T5 (FINAL) | Task 1 | EXIST 2022 + add | EXIST 2022 + add + transl data | none retrain lr=3e-4 | none | 83.58%    |  83.92%  | 83.50%    | 83.51%   | JB | 6 | 4 | 512 | 3e-4 |
| mBERT (FINAL) | Task 2 | EXIST 2022 + add data | EXIST 2022 | none | none | 77.25%    | 67.50%    | 68.33%    | 65.53%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 2 | EXIST 2022 + add data | EXIST 2022 + transl data | none | none | 76.73%    | 67.41%    | 67.66%    | 65.13%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 2 | EXIST 2022 + add data | EXIST 2022 + transl data | none | none | 76.73%    | 67.41%    | 67.66%    | 65.13%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 2 | EXIST 2022 + add data | EXIST 2022 | none | none | 76.13%    | 64.90%    | 64.67%    | 63.10%   | MS | 7 | 8 | 128 | 2e-5 |
| mBERT | Task 2 | EXIST 2022 | EXIST 2022 | none | none | 76.22%    | 67.08%    | 67.45%    | 64.73%   | MS | 8 | 16 | 256 | 2e-5 |
| mBERT (FINAL) | Task 2 | EXIST 2022 + add data + tweets | EXIST 2022 | none | none | 77.06%    | 67.13%    | 67.39%    | 64.74%  | MS | 8 | 16 | 256 | 2e-5 |
| XLM-RoBERTa | Task 2 | EXIST 2022 | EXIST 2022 | none | none | 73.36%    | 66.01%    | 67.76%    | 66.81%   | DL | 3 | 8 | 128 | 2e-5 |
| XLM-RoBERTa | Task 2 | EXIST 2022 | EXIST 2022 | none | none | 74.96%    | 68.06%    | 70.11%    | 69.01%   | DL | 3/2 | 8 | 128 | 2e-5/1e-5 |
| XLM-RoBERTa | Task 2 | EXIST 2022 + add data | EXIST 2022 | none | none | 75.03%    | 68.76%    | 70.64%    | 69.62%   | DL | 3 | 8 | 128 | 2e-5 |
| XLM-RoBERTa | Task 2 | EXIST 2022 + add data | EXIST 2022 | none | none | 74.84%    | 68.74%    | 71.86%    | 70.09%   | DL | 3/2 | 8 | 128 | 2e-5/1e-5 |
| XLM-RoBERTa | Task 2 | EXIST 2022 + add data | EXIST 2022 (task 2) | none | none | 75.97%    | 69.07%    | 71.69%    | 70.28%   | DL | 3/2 | 8 | 256 | 2e-5/1e-5 |
| XLM-RoBERTa | Task 2 | EXIST 2022 + add data | EXIST 2022 + transl data (task 2) | none | none | 77.09%    | 71.01%    | 73.34%    | 72.09%   | DL | 3/2 | 8 | 256 | 2e-5/1e-5 |
| XLM-RoBERTa (FINAL) | Task 2 | EXIST 2022 + add data | EXIST 2022 + transl data (task 2) | none | none | 77.63%    | 71.40%    | 73.64%    | 72.46%   | DL | 3/2+1 | 8 | 256 | 2e-5/1e-5 |
| T5 (FINAL) | Task 2 | EXIST 2022| EXIST 2022| none | none | 75.19%    | 69.60%    | 70.21%    | 69.70%   | JB | 10 | 4 | 512 | 1e-4 |
| T5 | Task 2 | EXIST 2022 + add | EXIST 2022| none retrain lr=1e-4 | none | 75.82%    | 60.29%    | 61.07%    | 60.60%   | JB | 12 | 4 | 512 | 1e-4 |
| T5 (not Final cause preds show issue in inference Model)| Task 2 | EXIST 2022 + add | EXIST 2022| none retrain lr=3e-4 | none | 75.47%    | 69.39%    | 71.46%    | 70.30%   | JB | 11 | 4 | 512 | 1e-4 |
| T5 | Task 2 | EXIST 2022 | EXIST 2022 + transl data | none  | none | 74.26%    | 68.77%    | 68.36%    | 68.17%   | JB | 10 | 4 | 512 | 1e-4 |
| T5 | Task 2 | EXIST 2022 + add | EXIST 2022 + transl data | none retrain lr=3e-4 | none | 75.04%    | 69.63%    | 69.02%    | 69.19%   | JB | 8 | 4 | 512 | 1e-4 |
| T5 | Task 2 | EXIST 2022 + add | EXIST 2022 + transl data | none retrain lr=1e-4 | none | 75.27%    | 68.82%    | 71.85%    | 70.03%   | JB | 11 | 4 | 512 | 1e-4 |


## JUST TO SAVE IT - WITH OLD TRAIN/VAL SPLIT (Mina):
| Model | Approach | Pretraining (PT)  | Finetuning (FT) | Preproc. (PT) | Preproc. (FT) | Acc | Prec (macro) | Rec (macro) | F1 (macro)  | Added by: | Epochs (FT) | Batchsize (FT) | MaxSeqLen (FT) | LearningRate (FT) | 
| -------------- | --------------------- | --------------------- |	--------------------- | :-------: | :-------: | :-------: | :-------: | ---------- | :-------: | :-------: | :----------: | ---------- | ---------- | ---------- |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 88.26%    | 86.34%    | 87.42%    | 85.85%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 1 | 87.70%    | 85.65%    | 86.25%    | 84.90%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 2 | 87.65%    | 85.48%    | 86.54%    | 85.02%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 3 | 88.41%    | 86.35%    | 87.69%    | 86.03%   | MS | 10 | 16 | 256 | 2e-5 |


## Status Updates
*



