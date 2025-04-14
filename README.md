# Train Synthesizer

This project implements a data generation and training pipeline for sentiment analysis, specifically focused on stock market sentiment using DPO (Direct Preference Optimization) techniques.

## Project Structure

```
.
├── data/                      # Dataset directory
├── figures/                   # Visualization results
│   ├── test_accuracy_barchart.png
│   └── test_accuracy_boxplot.png
├── prompt_templates/          # Templates for data generation
│   ├── dpo.txt               # DPO prompt template
│   └── sft.txt               # SFT prompt template
├── generate_dpo_data.ipynb    # Main notebook for data generation
└── requirements.txt           # Project dependencies
```

## Features

- Stock market sentiment analysis
- DPO (Direct Preference Optimization) data generation
- SFT (Supervised Fine-Tuning) data generation
- Data cleaning and preprocessing
- Visualization of test accuracy results

## Installation

1. Clone the repository:
```bash
git clone [repository-url]
cd train-synthesizer
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

1. The main data generation process is implemented in `generate_dpo_data.ipynb`. This notebook:
   - Loads and processes sentiment analysis data
   - Generates DPO training data
   - Handles stock ticker extraction and mapping
   - Processes and cleans the dataset

2. The project uses two types of prompt templates:
   - `prompt_templates/dpo.txt`: Template for DPO data generation
   - `prompt_templates/sft.txt`: Template for SFT data generation

3. The processed data is stored in the `data/` directory, with separate files for training and validation sets.

4. Visualization results are saved in the `figures/` directory:
   - `test_accuracy_barchart.png`: Bar chart visualization of test accuracy
   - `test_accuracy_boxplot.png`: Box plot visualization of test accuracy

## Data Generation

The project generates financial news headlines with sentiment labels:

- **Sentiment Labels**:
  - Bearish (0): Negative sentiment about a stock or market trend
  - Bullish (1): Positive sentiment about a stock or market trend
  - Neutral (2): Neutral or informational tone

- **Headline Guidelines**:
  - Concise and mimic real financial news
  - Sentence case formatting
  - Include stock tickers or company names
  - Cover various financial themes (downgrades/upgrades, price targets, market trends, etc.)
  - Include source attribution when relevant

## Results

The project includes visualization of test accuracy results in the `figures/` directory:
- `test_accuracy_barchart.png`: Bar chart visualization of test accuracy
- `test_accuracy_boxplot.png`: Box plot visualization of test accuracy

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


