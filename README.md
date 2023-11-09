<h1 align="center">
Physical Commonsene-Affordance
</h1>
<p align="center">
<img src="https://github.com/com-phy-affordance/com-affordance/blob/main/tmlr.png" alt="A not so confused robot">
</p>
Supporting Material For Physical CommonSense Affordance

## Task-0:
- GT Concept-Object Mappings : [Concept-Mappings](https://github.com/com-phy-affordance/com-affordance/blob/main/objects.json)
- GT Task-Concept-Object Mappings: [Oracle-Mappings](https://github.com/com-phy-affordance/com-affordance/blob/main/oracle.json)
- Task List: [Tasks](https://github.com/com-phy-affordance/com-affordance/blob/main/tasks.json)
- Concept List: [Concepts](https://github.com/com-phy-affordance/com-affordance/blob/main/concepts.json)
- Task-0 Dataset: [Variation-{1-4}](https://drive.google.com/drive/folders/1reH0JHhPM_tFzDMcAaJF0PycFMixfIbo?usp=sharing)

## Task-1:
- All Possible Common Configurations: [possible configurations](https://github.com/com-phy-affordance/com-affordance/blob/main/task-1/possible_configurations_v1.json)
- Oracle Configurations:[Ideal Configurations](https://github.com/com-phy-affordance/com-affordance/blob/main/task-1/pouch_config_oracle.json)
- Commonsense Common Occurence Variables: [common variables](https://github.com/com-phy-affordance/com-affordance/blob/main/task-1/common_var_responses.json)
- Task-1 Dataset: [Variation-{1-12}](https://drive.google.com/drive/folders/1reH0JHhPM_tFzDMcAaJF0PycFMixfIbo?usp=sharing)

## Task-2:
- Suboptimal Configurations: [suboptimal configurations](https://github.com/com-phy-affordance/com-affordance/blob/main/task-2/pouch_suboptimal.json)
- Human Preference Material Order: [material preference](https://github.com/com-phy-affordance/com-affordance/blob/main/task-2/material_preference.json)
- Task-2 Dataset: [Variation-{1-14}](https://drive.google.com/drive/folders/1reH0JHhPM_tFzDMcAaJF0PycFMixfIbo?usp=sharing)

### Prompts Used: [Quantitative Examples](https://giant-licorice-a62.notion.site/Prompts-for-Appendix-Examples-d58e0184d1c546bd8632024de3f7ac25)
### Implementations For Language Models:
- PaLM: Free API
- GPT3.5-Turbo: Student Azure Subscription
- LLama13B: huggingface text generation pipeline [Reference Link](https://huggingface.co/blog/llama2)
- Vicuna13B: lmsys [Link](https://github.com/lm-sys/FastChat)
- Vicuna7B: lmsys [Link](https://github.com/lm-sys/FastChat)
- Mistral-7B: huggingface [Link](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.1)
- ChatGLM-6B: huggingface [Link](https://huggingface.co/THUDM/chatglm-6b)
- ChatGLM2-6B: huggingface [Link](https://github.com/THUDM/ChatGLM2-6B)

----------------------------------------------------------------------------------------------------------------
## Upcoming Stuff:
- exporting an excel sheet to create object, task, concept jsons
- generating task-0 datasets for your own task list, object list, concept lists
- generating task-1, task-2 datasets for your own variables, your preferred possible configurations, handcrafted penalty schema and your own preferences.

> play around, create more variables, go for more comprehensive reward structures, go in any depth you wish. Let's create more agents capable of physical commonsense reasoning!

PS: If you need any help experimenting with this data or curating your own datasets, feel free to open a pull request.
