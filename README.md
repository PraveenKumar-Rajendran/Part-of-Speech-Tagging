# Part of Speech Tagger using Hidden Markov Model (HMM)

This repository contains a Jupyter notebook that demonstrates the implementation of a Part of Speech (POS) tagger using a Hidden Markov Model (HMM).

## Overview

The notebook implements an HMM-based POS tagger which involves:
1. **Data Preparation:** Reading and processing input data to extract words and their corresponding tags.
2. **Model Initialization:** Creating an instance of the HMM model.
3. **State Creation:** Defining states with emission probabilities.
4. **Adding Transitions:** Setting up transitions between states based on observed data.
5. **Finalizing the Model:** Baking the model to make it ready for use.
6. **Evaluation:** Evaluating the tagger on a test dataset.

## Flow of the Notebook

1. **Initialization:**
   - Import necessary libraries and modules.

2. **Data Preparation:**
   - Set up data streams to extract words and tags.
   - Generate tag and word lists from the data stream.
   - Calculate emission counts for the words given tags.

3. **Most Frequent Class Tagger (MFCTagger):**
   - Implement a simple baseline tagger that assigns the most frequent tag for each word.
   - Compare the performance of this baseline with the HMM tagger.

4. **HMM Model Initialization:**
   - Create an instance of the HMM model.

5. **State Creation:**
   - For each tag, calculate the emission probabilities and create states using these probabilities.
   - Add these states to the HMM model.

6. **Adding Transitions:**
   - Add transitions from the start state to each tag state.
   - Add transitions from each tag state to the end state.
   - Add transitions between tag states based on bigram counts.

7. **Finalizing the Model:**
   - Finalize the HMM model by baking it.

8. **Evaluation:**
   - Evaluate the HMM tagger on a test dataset.
   - Compare the accuracy of the HMM tagger and the MFCTagger.

## How to Use

To use this notebook, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone <repository_url>
   cd <repository_directory>
   ```

2. **Set Up the Environment:**
   - Ensure you have Conda installed.
   - Create and activate the Conda environment using the provided `hmm-tagger.yaml` file:
     ```bash
     conda env create -f hmm-tagger.yaml
     conda activate hmm-tagger
     ```

3. **Run the Notebook:**
   - Launch Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - Open `HMM Tagger.ipynb` and run the cells to execute the POS tagging process.

3. **Execute the Cells:**
   - Run the cells in the notebook sequentially to execute the POS tagging process.

## Additional Information

- **Most Frequent Class Tagger (MFCTagger):** This section implements a simple baseline tagger that assigns the most frequent tag for each word. The `MFCTagger` class is provided to mock the interface of the HMM models so that they can be used interchangeably.
- **Evaluation:** Evaluate the tagger on a test dataset and compare the accuracy of the HMM tagger and the MFCTagger.

For more information, please refer to the provided README from [Udacity](./README_Udacity.md).