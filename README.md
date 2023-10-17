# MentalHealthAssistant

## Fine-tuning Llama2 for Mental Health Counseling
### Introduction
Approximately 1 in 4 adults in the United States face mental health challenges annually. In the quest to provide immediate guidance, this project harnesses the power of artificial intelligence to create a virtual assistant for mental health counseling. Using the 7 billion parameter Llama 2 model, this notebook walks through the development process of this prototype.

Access the trained model: Huggingface - [langecod/CounselLlama7B](https://huggingface.co/langecod/CounselLlama7B)

### Table of Contents
Dataset Overview
Model Preparation
Training and Prompting
Chatbot Interface
Conclusion
### 1. Dataset Overview
The dataset, [Amod/mental_health_counseling_conversations](https://huggingface.co/datasets/Amod/mental_health_counseling_conversations), comprises 3,512 Q&A pairs from counselchat.com. With advice from certified psychologists, it's tailor-made to train language models on mental health queries.

### 2. Model Preparation
Meta's 7 billion parameter Llama 2 chat model was chosen for the task of text generation. For memory efficiency and faster training, the model was quantized to 4-bit and the "Quantized Low-Rank Adaptation" (QLoRA) method was used to fine-tune the model on the dataset.

### 3. Training and Prompting
An emphasis is placed on the significance of the prompt, guiding the model to produce safe and beneficial mental health advice that comforts the user and refers them to the appropriate resources. A formatting function was also applied so that the model was trained for 3 epochs on text that followed Llama's specific prompt-context-response input style.

### 4. Chatbot User Interface
Using Ipywidgets, a basic chatbot interface was established, allowing users to interact with the model. While the model generally produces relevant and helpful responses, there are noted challenges like short and repetitive sentences. These, along with potential hallucinatory replies, are areas highlighted for future refinement.

<img width="909" alt="CounselGPT" src="https://github.com/Cody-Lange/MentalHealthAssistant/assets/50972659/ced5eee9-fed8-4d52-9034-1309ca622c1d">

### Conclusion
The notebook illustrates the potential of large language models in the domain of mental health counseling. The Llama 2 model, fine-tuned with counselchat.com data, represents a step forward in immediate virtual assistance. However, there's room for growth. Upgrading the model, refining prompts, expanding the dataset, and introducing a more sophisticated UI can enhance the utility and user experience in subsequent iterations.
