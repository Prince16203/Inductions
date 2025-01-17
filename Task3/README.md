# Conversational AI with Fine-Tuned GPT-2

This project demonstrates how to fine-tune GPT-2 for generating natural, human-like conversations between two individuals. The resulting model can be used in chatbots, virtual assistants, or any application requiring realistic conversational AI.

---

## Features

- **Pretrained GPT-2:** Fine-tunes the GPT-2 model for dialogue generation.  
- **Customizable Prompts:** Generates conversations based on user-provided prompts.  
- **Realistic Responses:** Produces coherent, contextually appropriate answers.  
- **Scalable Model:** Compatible with different GPT-2 sizes (small, medium, large).  

---

## Choice of LLM
The model used for this project is **GPT-2**, a transformer-based language model developed by OpenAI. GPT-2 was selected due to its balance of performance, accessibility, and efficiency for the intended use case.

### Justifications for Choosing GPT-2
- **Proven Capability**: GPT-2 has demonstrated robust natural language processing capabilities across various tasks.
- **Computational Efficiency**: Compared to larger models (e.g., GPT-3), GPT-2 is computationally less demanding, making it suitable for fine-tuning on resource-constrained systems.
- **Ease of Fine-Tuning**: The model's architecture is well-documented, allowing straightforward customization for domain-specific applications.

## Fine-Tuning Method

### Methods Used
1. **Transformer Architecture**: 
   - The base GPT-2 architecture was utilized for its transformer-based design, enabling efficient context handling and sequence generation.
2. **Low-Rank Adaptation (LoRA)**:
   - LoRA was applied to fine-tune the model while reducing the number of trainable parameters. This method is particularly advantageous for adapting large pre-trained models using smaller datasets and limited computational resources.

## Dataset

A structured dataset containing dialogues between two persons is required for fine-tuning. Each conversation should have alternating lines, such as:

```plaintext
Person1: Hello! How are you?  
Person2: I'm good, thank you! How about you?  
Person1: I'm doing well, thanks for asking.  
Person2: Glad to hear that!  
```

## Model Weights
The fine-tuned model weights have been uploaded to a public Hugging Face account for accessibility.

### Hugging Face Model Link
(https://wandb.ai/stevestarc16-iit-indore/huggingface/runs/urhojhaq?nw=nwuserstevestarc16)

## Training Process

The training process involves the following steps:


