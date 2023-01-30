# confidence-distill
## Confidence Property Preservation of Knowledge Distillation Abstractions
Below we describe the process of distilling and then property analysis on RTE task.
The other tasks would follow the same path.
We selected RTE due to its relatively smaller size.

##  RTE task (example)
* Copy General Distill model
copy from drive/...  to your "./_models" folder 

* Copy teacher model (uncased BERT fine-tuned on RTE)
copy from drive/...  to your "./_models" folder 

* Copy dataset
copy from drive/.../glue_data/RTE to your "./data/glue_data/RTE"

* Run distillation (VM)
source rq1_rte.sh
(distilled model will be created and saved, softmax outputs will be save)

* Analyze results
jupyter lab

## All Experiment results 

To add
