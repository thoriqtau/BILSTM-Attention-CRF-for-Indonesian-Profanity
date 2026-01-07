# Context-Based Detection of Indonesian Profanity

## Background

<p align="justify">
Traditional approaches such as simple word-matching systems based on profanity lists are unable to capture sentence context; for example, the word “anjing” can function as a vulgar insult, but it may also be neutral when referring to a pet dog.
</p>

## Purpose

<p align="justify">
Producing a system capable of detecting offensive words with outputs in the form of per-token labels, namely “PER” for behavioral related profanity, “FIS” for physical related profanity, “HWN” for animal related profanity, and “SEKS” for sexual related profanity.
</p>

# About Dataset

## Dataset Source

<div align="justify">

The dataset used in this project was originally developed by **M. Ibrohim and Budi (2018).**

You can find the original paper and data through the following links:

- **Paper:** [A Dataset and Preliminaries Study for Abusive Language Detection in Indonesian Social Media](https://doi.org/10.1016/j.procs.2018.08.169)
- **GitHub Repository:** [id-abusive-language-detection](http://github.com/okkyibrohim/id-abusive-language-detection)

</div>

---

<div align="justify">

In this study, the original dataset was modified to align with a **token classification** approach. The process involved:

1.  **Tokenization**: Breaking down sentences into individual tokens (words and punctuation).
2.  **Annotation**: Assigning labels to each token based on its specific named entity.

This modification enables the model to detect abusive language with higher specificity and contextual accuracy at the **token level**.

</div>

## Defined Entity

The named entities used in this research can be seen in table below.

<table border="1" cellpadding="6" cellspacing="0">
  <thead>
    <tr>
      <th>Tag</th>
      <th>Abbreviation</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>FISIK POSITIF</td>
      <td>FIS-POS</td>
      <td>Positive words referring to physical attributes or a person's body</td>
    </tr>
    <tr>
      <td>FISIK NEGATIF</td>
      <td>FIS-NEG</td>
      <td>Negative or offensive words related to physical attributes or a person's body</td>
    </tr>
    <tr>
      <td>HEWAN POSITIF</td>
      <td>HWN-POS</td>
      <td>Positive words that use animal references in a non-offensive or metaphorical manner</td>
    </tr>
    <tr>
      <td>HEWAN NEGATIF</td>
      <td>HWN-NEG</td>
      <td>Negative or offensive words that use animal names as insults or derogatory expressions</td>
    </tr>
    <tr>
      <td>PERILAKU POSITIF</td>
      <td>PER-POS</td>
      <td>Positive words describing behavior, intelligence, attitude, or personal traits</td>
    </tr>
    <tr>
      <td>PERILAKU NEGATIF</td>
      <td>PER-NEG</td>
      <td>Negative or offensive words describing behavior, intelligence, attitude, or personal traits</td>
    </tr>
    <tr>
      <td>SEKSUAL NEGATIF</td>
      <td>SEKS-NEG</td>
      <td>Negative or offensive words containing sexual or gender-related elements</td>
    </tr>
  </tbody>
</table>

<p align="justify">
Entity naming in NER tasks is required to classify words according to the domain of offensive language. Defining the domain serves as an annotation guideline to ensure consistency and accuracy in labeling entities within the dataset.
</p>

## Annotation Process

<div align="justify">

The annotation process is performed at the token level (token-level annotation), where each word in a sentence is segmented into tokens, and then labeled according to its meaning and context of use.

- token/label

Example:

- lucunya/O adalah/O kak/O pacar/O nyadain/O ini/O telat/O bgt/O anjir/PER-NEG

</div>

# License

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
