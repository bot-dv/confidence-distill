# confidence-distill
## Confidence Property Preservation of Knowledge Distillation Abstractions

## Folder Structure
### Inputs
* [_data](https://drive.google.com/drive/folders/1JY0JfuAKHCTQxMLoI8Bc8pgW9FdtcXTC?usp=share_link) - datatsets
* [_models](https://drive.google.com/drive/folders/1SA12d_mQf-Z6oG3tpCeAKWt2UV_JfjhQ?usp=share_link) - input models 
* TinyBERT - code with knowledge distillation TinyBERT with modifications for data collections
* *.jpyter - analysis of the properties and collected data
* *.sh - runfiles for experiments/research questions
* VM - basic CPU environment with py37 that can also be otained via requirements.txt

### Outputs
* logs - prints out losses and accuracy
* models_train - saved fine-tune distilled models
* eval_results - collected data on sotmax from the runs

##  RTE task (example)
Below we describe the process of distilling and then property analysis on RTE task.
The other tasks would follow the same path.
We selected RTE due to its relatively smaller size.


* Copy General Distill model
  * copy from [_models](https://drive.google.com/drive/folders/1SA12d_mQf-Z6oG3tpCeAKWt2UV_JfjhQ?usp=share_link)/General_TinyBERT_6L_768D  to your "./_models/" folder 

* Copy teacher model (uncased BERT fine-tuned on RTE)
  * copy from [_models](https://drive.google.com/drive/folders/1SA12d_mQf-Z6oG3tpCeAKWt2UV_JfjhQ?usp=share_link)/bert-base-uncased-rte  to your "./_models/" folder 

* Copy dataset
  * copy from [_data](https://drive.google.com/drive/folders/1JY0JfuAKHCTQxMLoI8Bc8pgW9FdtcXTC?usp=share_link)/glue_data/RTE to your "./data/glue_data/RTE"

* Run distillation (VM)
   * source rq1_rte.sh
(distilled model will be created and saved, softmax outputs will be save)

* Analyze results
  * jupyter lab

## All Experiment results 

To add
