# confidence-distill
## Confidence Property Preservation of Knowledge Distillation Abstractions

## Folder Structure
### Inputs
* [_data](https://drive.google.com/drive/folders/1JY0JfuAKHCTQxMLoI8Bc8pgW9FdtcXTC?usp=share_link) - datatsets
* [_models](https://drive.google.com/drive/folders/1SA12d_mQf-Z6oG3tpCeAKWt2UV_JfjhQ?usp=share_link) - input models 
* **TinyBERT** - code with knowledge distillation [TinyBERT](https://arxiv.org/abs/1909.10351) with modifications for data collections
* **rq1_results.ipynb** - analysis of the properties and collected data for RQ1, S_{6L}
* **rq1_train_eval_tinybert_6l_sst2.sh** - runfile for experiments/research questions
* **requirements.txt** - basic CPU environment on ubuntu with py37 

### Outputs
* **_eval_output** - collected data on sotmax from the experiments

##  Example (SST-2 task)
Below we describe the process of distilling and then property analysis on SST-2 task.
The other tasks would follow the same path.


* Copy General Distill model
  * copy from [_models](https://drive.google.com/drive/folders/1SA12d_mQf-Z6oG3tpCeAKWt2UV_JfjhQ?usp=share_link)/General_TinyBERT_6L_768D  to your "./_models/" folder 

* Copy teacher model (uncased BERT fine-tuned on SST-2)
  * copy from [_models](https://drive.google.com/drive/folders/1SA12d_mQf-Z6oG3tpCeAKWt2UV_JfjhQ?usp=share_link)/bert-base-uncased-finetuned-sst2  to your "./_models/" folder 

* Copy dataset
  * copy from [_data](https://drive.google.com/drive/folders/1JY0JfuAKHCTQxMLoI8Bc8pgW9FdtcXTC?usp=share_link)/glue_data/SST-2 to your "./data/glue_data/RTE"

* Create environment
  * <code> pip install -r requirements.txt </code>

* Run distillation 
   * <code> source rq1_train_eval_tinybert_6l_sst2.sh </code> 
   * distilled model will be created and saved, softmax outputs will be saved to "_eval_output"
   * Expected output: ![distillation](https://user-images.githubusercontent.com/123794942/215983972-75b397b0-d782-494c-bf34-86e2db0f4887.png)


* Analyze results
  * <code> jupyter lab </code>
  * Expected output: ![confidence](https://user-images.githubusercontent.com/123794942/215984478-1cf5c3d6-361f-4bbe-a897-c0f0657e0024.png)


