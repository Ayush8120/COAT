<h1 align="center">
Commonsene Object Affordance Task [COAT]
</h1>
  
<p align="center">
  <br>
  <a href="https://openreview.net/pdf?id=xYkdmEGhIM">OpenReview</a> | <a href="https://drive.google.com/drive/u/4/folders/1reH0JHhPM_tFzDMcAaJF0PycFMixfIbo">Datasets</a> | <a href="https://github.com/Ayush8120/COAT-code">Code</a> 
</p>

<p align="center">
<img src="https://github.com/com-phy-affordance/COAT/blob/main/levels-intro.png" alt="Paper Summary Flowchart">
<em>A 3 level framework adumbrating human commonsense style reasoning for estimating object affordance for various tasks</em>
</p>

### Experimental Setup:
- Task List: [tasks](https://github.com/com-phy-affordance/com-affordance/blob/main/tasks.json)
- Object List: [objects](https://github.com/com-phy-affordance/com-affordance/blob/main/concepts.json)
- Utility List[^1]: [utilities](https://github.com/com-phy-affordance/com-affordance/blob/main/concepts.json)
- Variables Used:
  ```temperature```, ```mass```, ```material```, ```already-in-use```, ```condition```
  
### Utility Level Pruning:
This gives us ```Utility```to``Object`` mappings also called ```utility objects```
- GT Object-Utility Mappings : [utility-mappings](https://github.com/com-phy-affordance/com-affordance/blob/main/objects.json)

### Task-u(Utility Level):
Here we evaluate models on their ability to prune out appropriate objects on the basis of Utility. 
- GT (Utility)-(Object) Mappings: [utility-objects](https://github.com/com-phy-affordance/com-affordance/blob/main/objects.json)
- Task-u Dataset: [4 Variations](https://drive.google.com/drive/folders/1JJSIicKGp0a7ThsenKl0XWKsTtPL_b5z?usp=sharing)
  
### Task-0(Context Level):
Here we evaluate models on their ability to prune out appropriate objects on the basis of Context. This gives us ```(Task,Utility)```to``Object`` mappings also called ```context objects```
- GT (Task-Utility)-(Object) Mappings: [context-objects](https://github.com/com-phy-affordance/com-affordance/blob/main/oracle.json)
- Task-0 Dataset: [4 Variations](https://drive.google.com/drive/folders/1reH0JHhPM_tFzDMcAaJF0PycFMixfIbo?usp=sharing)

### Task-1(Physical State Level):
Here we evaluate models on their ability to prune out the ```ideal``` configuration when presented with a number of ```context object``` configurations. (Something that is pretty obvious to humans)
- All Possible Common Configurations: [possible configurations](https://github.com/com-phy-affordance/com-affordance/blob/main/task-1/possible_configurations_v1.json)
- Ideal Configurations: [ideal configurations](https://github.com/com-phy-affordance/com-affordance/blob/main/task-1/pouch_config_oracle.json)
- Commonsense Common Occurence Variables: [common variables values](https://github.com/com-phy-affordance/com-affordance/blob/main/task-1/common_var_responses.json)
- Task-1 Dataset: [12 Variations](https://drive.google.com/drive/folders/1reH0JHhPM_tFzDMcAaJF0PycFMixfIbo?usp=sharing)

### Task-2(Physical State Level):
Here we evaluate models on their ability to prune out the most appropriate```sub-optimal``` configuration when presented with a number of sub-optimal configurations of ```context objects```. (Something that is pretty obvious to humans)
- Suboptimal Configurations: [suboptimal configurations](https://github.com/com-phy-affordance/com-affordance/blob/main/task-2/pouch_suboptimal.json)
- Human Preference Material Order: [material preference](https://github.com/com-phy-affordance/com-affordance/blob/main/task-2/material_preference.json)
- Task-2 Dataset: [14 Variations](https://drive.google.com/drive/folders/1reH0JHhPM_tFzDMcAaJF0PycFMixfIbo?usp=sharing)
---------------------------------------------------------------------------------------------------------------

### Finetuning Datasets 

Please refer to [Appendix F.1](https://openreview.net/pdf?id=xYkdmEGhIM) for dataset details

- Finetuning Dataset for Object Level Selection : [Google Drive Link](https://drive.google.com/drive/folders/1GtrGQxTTtYEczYK1ytB71Y2HGxM1TEu5?usp=drive_link)
- Finetuning Dataset for Physical State Level Selection : [Google Drive Link](https://drive.google.com/drive/folders/1FiZc8u_G8wUrN4NroZmIgmcTe0jor72T?usp=drive_link)

### Full Pipeline Evaluation Datasets

Please refer to [Appendix F.2](https://openreview.net/pdf?id=xYkdmEGhIM) for dataset deatails

- Ideal Object Choice Datasets : [Google Drive Link](https://drive.google.com/drive/folders/1SMM2TU1BKH32oKtfmW0gS3QfyUA68IZ0?usp=drive_link)
- Moderate Object Choice Datasets : [Google Drive Link](https://drive.google.com/drive/folders/1SlZQBp4Iao3VHnmOFZMKfzn_LWOctnVE?usp=drive_link)


<h3>Prompts Used</h3>
<p>
  
  [Quantitative Examples](https://giant-licorice-a62.notion.site/Prompts-for-Appendix-Examples-d58e0184d1c546bd8632024de3f7ac25)
</p>

### Implementations For Language Models:
- PaLM/GPT3.5-Turbo: API
- LLama13B: huggingface text generation pipeline [link](https://huggingface.co/blog/llama2)
- Vicuna13B: lmsys [link](https://github.com/lm-sys/FastChat)
- Vicuna7B: lmsys [link](https://github.com/lm-sys/FastChat)
- Mistral-7B: huggingface [link](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.1)
- ChatGLM-6B: huggingface [link](https://huggingface.co/THUDM/chatglm-6b)
- ChatGLM2-6B: huggingface [link](https://github.com/THUDM/ChatGLM2-6B)

[^1]: For the purpose of datasets, we've used `concept and utility` interchangeably.
----------------------------------------------------------------------------------------------------------------
### Upcoming Stuff:
- generating object, task, utility jsons for your purpose 
- generating task-0 datasets for your own task list, object list, utility lists
- generating task-1, task-2 datasets for your own variables, your preferred possible configurations, handcrafted penalty schema and your own preferences.

> play around, create more variables, go for more comprehensive reward structures, go in any depth you wish. Let's create more agents capable of physical commonsense reasoning!

PS: If you need any help experimenting with this data or curating your own datasets, feel free to create an Issue.
