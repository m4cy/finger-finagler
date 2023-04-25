---

---






# Model Card for Finger Finagler

Automated Piano Fingering Tool, uses an LSTM architecture to process a sequence of notes and guess the next fingering to use.




#  Table of Contents

- [Model Card for Finger Finagler](#model-card-for--model_id-)
- [Table of Contents](#table-of-contents)
- [Model Details](#model-details)
  - [Model Description](#model-description)
- [Uses](#uses)
  - [Direct Use](#direct-use)
  - [Out-of-Scope Use](#out-of-scope-use)
- [Bias, Risks, and Limitations](#bias-risks-and-limitations)
  - [Recommendations](#recommendations)
- [Training Details](#training-details)
  - [Training Data](#training-data)
  - [Training Procedure](#training-procedure)
    - [Preprocessing](#preprocessing)
    - [Speeds, Sizes, Times](#speeds-sizes-times)
- [Evaluation](#evaluation)
  - [Testing Data, Factors & Metrics](#testing-data-factors--metrics)
    - [Testing Data](#testing-data)
    - [Factors](#factors)
    - [Metrics](#metrics)
  - [Results](#results)
- [Model Examination](#model-examination)
- [Environmental Impact](#environmental-impact)
- [Technical Specifications [optional]](#technical-specifications-optional)
  - [Model Architecture and Objective](#model-architecture-and-objective)
- [How to Get Started with the Model](#how-to-get-started-with-the-model)


# Model Details

## Model Description

<!-- Provide a longer summary of what this model is/does. -->
Automated Piano Fingering Tool, uses an LSTM architecture to process a sequence of notes and guess the next fingering to use.

- **Developed by:** Macy Huang
- **Model type:** Language model
- **Language(s) (NLP):** en
- **License:** mit
- **Parent Model:** No parent model
- **Resources for more information:** 
    - [GitHub Repo](https://github.com/m4cy/finger-finagler)
    - [Associated Paper](https://www.overleaf.com/read/xddwsfjrbxwy)

# Uses

This model's user base includes novice piano students who do not have the skills to predict comfortable and dynamic fingerings. The model accepts data in a very particular form, which is .txt files containing manual transcriptions of sheet music in the following format:

```
(note ID) (onset time) (offset time) (spelled pitch) (onset velocity) (offset velocity) (channel) (finger number)
```

Beyond this, the model has very limited scope and applicability though future work could include adapting it for fingering sheet music for other instruments.

## Direct Use

A user is not able to directly evaluate fingerings on a piece of sheet music yet. Potentially, they could enter their own processed sheet music and generate future fingerings but generally the model cannot be directly used yet. 


## Out-of-Scope Use

Given the subject material, the model cannot be misused to great effect and malicious use is generally inconsequential. Possible negative impacts on a user would be if the model did not find the most optimal fingering and a user of the model followed the fingering exactly, to their discomfort.


# Bias, Risks, and Limitations

One limitation is that this model performs better on classical music with fewer chord-based melodies because of the nature of its training set. Since the classical music canon is extremely eurocentric, it does display bias toward non-Western musical forms. Again, because the problem is very niche and does not deal with particular stereotypes and social issues, there are few risks of unfairness. 

## Recommendations

We recommend that this model is employed mostly with classical music scores until work can be done to expand the model to contemporary forms of music to make the model more robust.


# Training Details

## Training Data

See [datasheet](./datasheet.md) for more details. Information on processing can be found in the [paper](./Finger_Finagler.pdf) as well.

## Training Procedure

The model was trained on the PIano fingerinG (PIG) dataset, which is composed of 150 pieces of sheet music by Western classical music composers. These pieces of music had fingerings added by professional pianists.

### Preprocessing

The PIG dataset had to be processed into an acceptable input for the model and a label (the fingering). Additionally, fingering labels had to be scaled from 0 to 9 instead of [-5, -1] and [1,5] for both hands.

### Speeds, Sizes, Times

Each model training took around 10-15 minutes which is relatively efficient.
 
# Evaluation

The model was validated against a held-out test set and MSE loss was observed as a measure of accuracy.

## Testing Data, Factors & Metrics

### Testing Data

See [datasheet](./datasheet.md) for more details.

### Factors

The model was assessed based on how accurate it was in predicting the label (fingering) for a note at the current state. It received information from previous states about their fingerings.

### Metrics

The evaluation metric was MSE loss, taken between the actual fingering label and the model's predicted fingering label.

## Results 

After training, loss was around 0.0505 for the baseline model, and fell to 0.0503 for some experimental iterations of the model.

# Environmental Impact

- **Hardware Type:** MacOS Intel CPU
- **Hours used:** 12ish

## Model Architecture and Objective

The model was composed of an LSTM layer and a simple linear layer to learnably transform the hidden state to output state. The LSTM layer was initialized with an input size, hidden state size, and output size in order to match the features of the dataset and desired output.