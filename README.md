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

MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


