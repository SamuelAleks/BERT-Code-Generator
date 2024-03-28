# Bert Code Completion Agent

2022 - Current

Author: Samuel Aleks

## Description

Bert Code Completion Agent (BCCA) is a simple BERT-based program that takes input from code, and outputs a generated response.

This program is designed to be trained on custom data, or someone can use the pretrained models for specific languages.

BERT is light enough that a personal computer is capable of training a usable model in a few days, or in a few minutes with cloud compute.

However, because of the grammatical predictive limitations of BERT, this program has a low accuracy, and thus better suited for providing inspiration rather than solid answers.

---

## 0_SetupData.ipynb

!!This program will remove any concatenate files that exist in the parent folder!!

- This program uses " +++$+++" as a delimiter for the data prior to tokenization and training

- (Make sure your input data does not contain this sequence, if it does, please modify the delimiter as needed)

- This program assumes input data is contained in a folder named "rawData".

- The program then sanitizes  the input files to remove comments and blank lines.

- Then, the output is stored in two files.

- "concatenateLines.txt" lists each "program" being identified with u{x}
  
  - The following data represents the "lines" of the program. 
  
  - This is so when training on the entire dataset, there is some knowledge of continuity between lines

- "concatenate.txt" contains the actual data the model will be trained on, in this case, lines of code
  
  - The syntax of each line is **&lt;line&gt; &lt;delim&gt; &lt;u (program number)&gt; &lt;delim&gt; &lt;original filename&gt; &lt;delim&gt; &lt;line of code&gt;**

## Tokenize.ipynb

## 1_DIYtrained_java.ipynb

## 2_Pretrained_JavaBERT_CAUKiel.ipynb

---

## Goals

At this current point, user-facing functionality is rather limited, so there are some goals at improving user-interaction and extending the abilities of the program.

- [ ] Create a TUI

- [ ] Create options flags

- [ ] Streamline agent training

- [ ] Streamline model tweaking

- [ ] Create a GUI
