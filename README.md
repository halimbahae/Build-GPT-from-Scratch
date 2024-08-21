# Build GPT from Scratch

This repository contains a notebook demonstrating the creation of a GPT-like language model from scratch using PyTorch. The notebook includes the following components:

- **Data Preparation**: Reading and tokenizing text data.
- **Dataset Creation**: Building a custom dataset for training.
- **Embedding Layers**: Implementing word and positional embeddings.
- **Self-Attention**: Understanding and applying self-attention mechanisms.

## Getting Started

### Prerequisites

- Python 3.x
- PyTorch
- `tiktoken` for tokenization

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/build-gpt-from-scratch.git
   cd build-gpt-from-scratch
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

### Usage

1. Open the notebook `build_llm_from_scratch.ipynb` using Jupyter Notebook or JupyterLab:
   ```bash
   jupyter notebook build_llm_from_scratch.ipynb
   ```

2. Follow the steps in the notebook to build and train a basic GPT-like model.

### Example

Here's a brief example of how to use the provided data loader:
```python
import tiktoken
from torch.utils.data import DataLoader

tokenizer = tiktoken.get_encoding("gpt2")
text = "Your training data here."
dataset = DatasetV1(text, tokenizer, max_length=8, stride=1)
data_loader = DataLoader(dataset, batch_size=4, shuffle=True)

for input_ids, target_ids in data_loader:
    print(input_ids, target_ids)
```

### Contributing

Feel free to open issues or submit pull requests if you have suggestions or improvements.

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
