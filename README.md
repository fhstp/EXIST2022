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
* Training/validation splits (80/20%): s. data/train_val_split
* Preprocessed data for language model fine-tuning: s. data/for_pretraining

## Approaches

## Results / Task_1 (Validation Data)

| Model    | Approach    | Pretraining Data   | Finetuning Data 	| Acc | Precision (macro) | Recall (macro) | F1 (macro)  | Added by: |
| -------------- | --------------------- | --------------------- |	--------------------- | :-------: | :-------: | :-------: | :-------: | ---------- |
| mBERT | Baseline | EXIST 2022	| EXIST 2022 (task2) 	| 74.88%    | 76.47%    | 75.08%    | 74.59%   | MS |
| mBERT | Baseline | EXIST 2022	| EXIST 2022  	| 74.88%    | 76.47%    | 75.08%    | 74.59%   | MS |
| BERT | Baseline | EXIST 2022	| EXIST 2022 	| 81.1%    | 83%    | 83%    | 82.4%   | AB |
| XML-RoBERTa | Baseline | EXIST 2022	| EXIST 2022 (task2) 	| 82.18%    | 79.63%    | 87.24%    | 83.26%   | DL |
| XML-RoBERTa | Baseline | EXIST 2022+additional datasets	| EXIST 2022  (task2)	| 82.02%    | 79.91%    | 86.32%    | 82.99%   | DL |
| T5 | Baseline | EXIST 2022	| EXIST 2022 	| 78.38%    | 75.90% (check if macro)   | 84.19% (check if macro)   | 79.83% (check if macro)  | JB |
| T5 | Baseline | EXIST 2022 +additional datasets	| EXIST 2022 	| 79.77%    | 76.44% (check if macro)   | 87.01% (check if macro)   | 81.39% (check if macro)  | JB |
| T5 | Baseline | EXIST 2022 +additional datasets	| EXIST 2022 + additional datasets 	| 85.29%    | 74.50% (check if macro)   | 83.71% (check if macro)   | 78.84% (check if macro)  | JB |


## Results / Task_2 (Validation Data)

| Model | Approach    | Pretraining Data   | Finetuning Data 	| Acc | Precision (macro) | Recall (macro) | F1 (macro)  | Added by: |
| -------------- | --------------------- | --------------------- |	--------------------- | :-------: | :-------: | :-------: | :-------: | ---------- |
| mBERT | Baseline | EXIST 2022	| EXIST 2022 	| 76.82%    | 71.50%    | 71.74%    | 71.53%   | MS |
| BERT | Baseline | EXIST 2022	| EXIST 2022	| 06.9%    | 10.2%    | 10%    | 10.9%   | AB |
| XML-RoBERTa | Baseline | EXIST 2022	| EXIST 2022 	| 69.48%    | 61.12%    | 63.82%    | 62.25%   | DL |
| XML-RoBERTa | Baseline | EXIST 2022+additional datasets	| EXIST 2022 	| 70.80%    | 63.31%    | 65.78%    | 64.40%   | DL |
| T5 | Baseline | EXIST 2022	| EXIST 2022 	| XXX%    | XXX%    | XXX%    | XXX%   | JB |

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
| mBERT | Task 1 | EXIST 2022 + add data + tweets | EXIST 2022 + add data | none | none | TBD%    | TBD%    | TBD%    |TBD %   | MS | 10 | 16 | 256 | 2e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 81.56%    | 81.76%    | 81.49%    | 81.50%   | DL | 3 | 8 | 128 | 1e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 82.37%    | 82.46%    | 82.32%    | 82.34%   | DL | 3 | 8 | 128 | 2e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 84.39%    | 84.39%    | 84.38%    | 84.38%   | DL | 3/2 | 8 | 128 | 2e-5/1e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 | EXIST 2022 + add data | none | none | 83.19%    | 83.38%    | 83.12%    | 83.14%   | DL | 3 | 8 | 128 | 2e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 | EXIST 2022 + add data | none | none | 84.78%    | 84.88%    | 84.73%    | 84.75%   | DL | 3/2 | 8 | 128 | 2e-5/1e-5 |
| mBERT | Task 2 | EXIST 2022 + add data | EXIST 2022 | none | none | 77.25%    | 67.50%    | 68.33%    | 65.53%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 2 | EXIST 2022 + add data | EXIST 2022 | none | none | 76.13%    | 64.90%    | 64.67%    | 63.10%   | MS | 10 | 8 | 128 | 2e-5 |
| mBERT | Task 2 | EXIST 2022 + add data + tweets | EXIST 2022 | none | Version X | %    | %    | %    | %   | %   | MS | 10 | 16 | 256 | 2e-5 |
| XLM-RoBERTa | Task 2 | EXIST 2022 | EXIST 2022 | none | none | 73.36%    | 66.01%    | 67.76%    | 66.81%   | DL | 3 | 8 | 128 | 2e-5 |
| XLM-RoBERTa | Task 2 | EXIST 2022 | EXIST 2022 | none | none | 74.96%    | 68.06%    | 70.11%    | 69.01%   | DL | 3/2 | 8 | 128 | 2e-5/1e-5 |
| XLM-RoBERTa | Task 2 | EXIST 2022 + add data | EXIST 2022 | none | none | 75.03%    | 68.76%    | 70.64%    | 69.62%   | DL | 3 | 8 | 128 | 2e-5 |
| XLM-RoBERTa | Task 2 | EXIST 2022 + add data | EXIST 2022 | none | none | 74.84%    | 68.74%    | 71.86%    | 70.09%   | DL | 3/2 | 8 | 128 | 2e-5/1e-5 |
| XLM-RoBERTa | Task 2 | EXIST 2022 + add data | EXIST 2022 | none | none | 75.97%    | 69.07%    | 71.69%    | 70.28%   | DL | 3/2 | 8 | 256 | 2e-5/1e-5 |

## JUST TO SAVE IT - WITH OLD TRAIN/VAL SPLIT (Mina):
| Model | Approach | Pretraining (PT)  | Finetuning (FT) | Preproc. (PT) | Preproc. (FT) | Acc | Prec (macro) | Rec (macro) | F1 (macro)  | Added by: | Epochs (FT) | Batchsize (FT) | MaxSeqLen (FT) | LearningRate (FT) | 
| -------------- | --------------------- | --------------------- |	--------------------- | :-------: | :-------: | :-------: | :-------: | ---------- | :-------: | :-------: | :----------: | ---------- | ---------- | ---------- |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 88.26%    | 86.34%    | 87.42%    | 85.85%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 1 | 87.70%    | 85.65%    | 86.25%    | 84.90%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 2 | 87.65%    | 85.48%    | 86.54%    | 85.02%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 3 | 88.41%    | 86.35%    | 87.69%    | 86.03%   | MS | 10 | 16 | 256 | 2e-5 |


## Status Updates
*



