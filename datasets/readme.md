# Datasets Overview

The files in this folder contain our datasets for **Reuter (news)**, **Enron (email)**, and **Persuade (essay)**.

## Column Descriptions

- **`key`**: Specific key to track the original source text (typically in the format of `human_name + index_of_the_text_in_original_human_dataset`).
- **`source`**: Source of the text. The possible values are:
  - `human`
  - `gpt_3.5`
  - `text-bison-001`
  - `mistral_7b`
  - `llama2_chat`
- **`intro_text`**: Introduction of the text, extracted from the text by LLM.
- **`body_text`**: Body segment of the text, extracted by LLM.
- **`conclusion_text`**: Conclusion segment of the text, extracted by LLM.
