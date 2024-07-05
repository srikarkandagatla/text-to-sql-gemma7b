# text-to-sql-gemma7b
Optimizing NLP Models through Quantization and Accelerated Training 

## Project Description: Text-to-SQL Model Training with Code-Gemma-7B
In this project, I trained a text-to-SQL model using the Code-Gemma-7B model to facilitate SQL query generation from natural language inputs. The project involved several key steps and methodologies:

## Objectives
1. **Develop a robust text-to-SQL model**: My goal was to generate accurate SQL queries based on user-provided English questions and a given database schema.
2. **Optimize training using LORA and quantization**: I aimed to enhance model efficiency and performance while reducing computational resource requirements.
3. **Utilize Weights & Biases (W&B)**: I tracked and logged the model training processes and outcomes for transparency and reproducibility.

## Methodologies
1. **Model Selection and Training**
  - **Model**: I selected Code-Gemma-7B, a large language model fine-tuned for text-to-SQL tasks.
  - **Optimization Techniques**:
    - **LORA (Low-Rank Adaptation)**: I applied LORA to update only a small percentage (approximately 0.6%) of the model's parameters, significantly reducing training overhead.
    - **Quantization**: This helped reduce the model size and memory usage without a substantial loss in performance.

2.**Training Process**
  - **Environment**: I utilized a Kaggle environment with limited GPU memory.
  - **Training Data**: I employed a custom dataset for fine-tuning the model, containing various SQL schema definitions and corresponding queries.
  - **Epochs and Batch Size**: I trained the model for 1 epoch due to memory constraints, experimenting with different batch sizes and sequence lengths to avoid out-of-memory errors.

3.**Logging and Monitoring**
  - **Weights & Biases**: I integrated W&B for real-time tracking and logging of training metrics such as loss, runtime, and parameter updates.
  - **Model Evaluation**: I evaluated the model's performance on test datasets, comparing generated SQL queries with original ones.

4.**Model Deployment**
  - **Model Saving and Uploading**: I saved the trained model and uploaded it to the Hugging Face Hub for easy access and deployment.
  - **Inference Pipeline**: I created a pipeline for generating SQL queries from natural language inputs using the fine-tuned model.

## **Results**
  - **Training Efficiency**: The training process, optimized with LORA and quantization, took nearly 2 hours for 1 epoch on the available GPU.
  - **Model Performance**: While the model generated decent results, there is room for improvement with further training and parameter tuning.
  - **Generated Queries**: The model produced SQL queries that, although not perfect, were reasonably accurate and could be further refined.

## **Future Work**
  - **Extended Training**: I plan to utilize more powerful GPUs (e.g., A100 on Google Colab) to increase the training data and epochs for better performance.
  - **Parameter Tuning**: I will experiment with different LORA ranks, batch sizes, and sequence lengths to optimize model accuracy and efficiency.
  - **Model Evaluation and Testing**: I will continue to evaluate the model on diverse datasets to ensure robustness and generalizability.

This project highlights the potential of large language models like Code-Gemma-7B for automating SQL query generation, offering significant time savings and accuracy improvements in database management and querying tasks.
