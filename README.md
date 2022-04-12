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
| BERT | Baseline | EXIST 2022	| EXIST 2022 	| 81.1%    | 83%    | 83%    | 82.4%   | AB |
| XML-RoBERTa | Baseline | EXIST 2022	| EXIST 2022 (task2) 	| 82.18%    | 79.63%    | 87.24%    | 83.26%   | DL |
| XML-RoBERTa | Baseline | EXIST 2022+additional datasets	| EXIST 2022  (task2)	| 82.02%    | 79.91%    | 86.32%    | 82.99%   | DL |
| T5 | Baseline | EXIST 2022	| EXIST 2022 	| 78.38%    | 75.90% (check if macro)   | 84.19% (check if macro)   | 79.83% (check if macro)  | JB |
| T5 | Baseline | EXIST 2022 +additional datasets	| EXIST 2022 	| 79.77%    | 76.44% (check if macro)   | 87.01% (check if macro)   | 81.39% (check if macro)  | JB |
| T5 | Baseline | EXIST 2022 +additional datasets	| EXIST 2022 + additional datasets 	| 85.29%    | 74.50% (check if macro)   | 83.71% (check if macro)   | 78.84% (check if macro)  | JB |


## Results / Task_2 (Validation Data)

| Model | Approach    | Pretraining Data   | Finetuning Data 	| Acc | Precision (macro) | Recall (macro) | F1 (macro)  | Added by: |
| -------------- | --------------------- | --------------------- |	--------------------- | :-------: | :-------: | :-------: | :-------: | ---------- |
| mBERT | Baseline | EXIST 2022	| EXIST 2022 (task2) 	| 76.82%    | 71.50%    | 71.74%    | 71.53%   | MS |
| BERT | Baseline | EXIST 2022	| EXIST 2022 (task2)	| 06.9%    | 10.2%    | 10%    | 10.9%   | AB |
| XML-RoBERTa | Baseline | EXIST 2022	| EXIST 2022 (task2) 	| 69.48%    | 61.12%    | 63.82%    | 62.25%   | DL |
| XML-RoBERTa | Baseline | EXIST 2022+additional datasets	| EXIST 2022 (task2) 	| 70.80%    | 63.31%    | 65.78%    | 64.40%   | DL |
| T5 | Baseline | EXIST 2022	| EXIST 2022 	| XXX%    | XXX%    | XXX%    | XXX%   | JB |

## Results / Experiments (Validation Data)

| Model | Approach | Pretraining (PT)  | Finetuning (FT) | Preproc. (PT) | Preproc. (FT) | Acc | Prec (macro) | Rec (macro) | F1 (macro)  | Added by: | Epochs (FT) | Batchsize (FT) | MaxSeqLen (FT) | LearningRate (FT) | 
| -------------- | --------------------- | --------------------- |	--------------------- | :-------: | :-------: | :-------: | :-------: | ---------- | :-------: | :-------: | :----------: | ---------- | ---------- | ---------- |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | %    | %    | %    | %   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 1 | %    | %    | %    | %   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 2 | %    | %    | %    | %   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 3 | %    | %    | %    | %   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | Version X | Version X | %    | %    | %    | %   | MS | 10 | 16 | 256 | 2e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 80.04%    | 80.29%    | 79.96%    | 79.97%   | DL | 3 | 8 | 128 | 7e-6 |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 81.56%    | 81.76%    | 81.49%    | 81.50%   | DL | 3 | 8 | 128 | 1e-5 |
| XLM-RoBERTa | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | %    | %    | %    | %   | DL | 3 | 8 | 128 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data + tweets | EXIST 2022 + add data | none | Version X | %    | %    | %    | %   | %   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 2 | EXIST 2022 + add data | EXIST 2022 | none | none | %    | %    | %    | %   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 2 | EXIST 2022 + add data | EXIST 2022 | none | Version X | %    | %    | %    | %   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 2 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version X | %    | %    | %    | %   | %   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 2 | EXIST 2022 + add data + tweets | EXIST 2022 | none | Version X | %    | %    | %    | %   | %   | MS | 10 | 16 | 256 | 2e-5 |

## JUST TO SAVE IT - WITH OLD TRAIN/VAL SPLIT (Mina):
| Model | Approach | Pretraining (PT)  | Finetuning (FT) | Preproc. (PT) | Preproc. (FT) | Acc | Prec (macro) | Rec (macro) | F1 (macro)  | Added by: | Epochs (FT) | Batchsize (FT) | MaxSeqLen (FT) | LearningRate (FT) | 
| -------------- | --------------------- | --------------------- |	--------------------- | :-------: | :-------: | :-------: | :-------: | ---------- | :-------: | :-------: | :----------: | ---------- | ---------- | ---------- |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | none | 88.26%    | 86.34%    | 87.42%    | 85.85%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 1 | 87.70%    | 85.65%    | 86.25%    | 84.90%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 2 | 87.65%    | 85.48%    | 86.54%    | 85.02%   | MS | 10 | 16 | 256 | 2e-5 |
| mBERT | Task 1 | EXIST 2022 + add data | EXIST 2022 + add data | none | Version 3 | 88.41%    | 86.35%    | 87.69%    | 86.03%   | MS | 10 | 16 | 256 | 2e-5 |


## Status Updates
*



