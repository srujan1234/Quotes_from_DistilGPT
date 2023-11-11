

# Inspirational Quotes Generation with GPT-2

This code snippet demonstrates how to generate inspirational quotes using a pre-trained GPT-2 model for fine-tuned text generation. The process involves loading a pre-trained model and fine-tuning it for generating inspirational quotes based on seed text. Here's a breakdown of the key steps in this code:

## 1. Use a Pre-trained Model with a Pipeline

The code first uses the Transformers library to create a text generation pipeline. It specifies the model to be used as "noelmathewisaac/inspirational-quotes-distilgpt2." This pre-trained model is designed for generating inspirational quotes.

## 2. Load Model Directly

Alternatively, the code provides instructions on how to load the model directly using its tokenizer and model architecture. This approach offers more flexibility for advanced users who may want to customize model parameters.

## 3. Check for GPU Availability

The code checks for the availability of a GPU. If a GPU is available, it sets the device to "cuda" to leverage GPU acceleration; otherwise, it uses the CPU.

## 4. Load Tokenizer and Model

The tokenizer and model are loaded from the pre-trained "noelmathewisaac/inspirational-quotes-distilgpt2" model. The model is loaded on the specified device (GPU or CPU).

## 5. Load Preprocessed Dataset

The code loads a preprocessed dataset containing text data from a CSV file. The path to the dataset should be provided, and the specific column with text data (in this case, "first_3_words") is selected.

## 6. Generate Inspirational Quotes

The code defines a function, `generate_quotes_for_each_row`, which generates inspirational quotes for each row in the dataset. It loops through the rows, uses the seed text (the text from the selected column), and generates quotes using the fine-tuned GPT-2 model. The generated quotes are stored along with their source row index.

## 7. Create a DataFrame for Generated Quotes

The generated quotes are organized into a new DataFrame. Each row in the DataFrame contains a generated quote and the source row it was based on.

## 8. Save Generated Quotes

Finally, the code saves the generated quotes to a new CSV file called "generated_quotes.csv."
