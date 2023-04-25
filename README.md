---

---






# Model Card for Finger Finagler

<!-- Provide a quick summary of what the model is/does. [Optional] -->
Automated Piano Fingering Tool, uses an LSTM architecture to process a sequence of notes and guess the next fingering to use.




#  Table of Contents

- [Model Card for Finger Finagler](#model-card-for--model_id-)
- [Table of Contents](#table-of-contents)
- [Model Details](#model-details)
  - [Model Description](#model-description)
- [Uses](#uses)
  - [Direct Use](#direct-use)
  - [Downstream Use [Optional]](#downstream-use-optional)
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
- **Shared by [Optional]:** Macy Huang
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

<!-- This section is for the model use without fine-tuning or plugging into a larger ecosystem/app. -->
<!-- If the user enters content, print that. If not, but they enter a task in the list, use that. If neither, say "more info needed." -->


## Out-of-Scope Use

<!-- This section addresses misuse, malicious use, and uses that the model will not work well for. -->
<!-- If the user enters content, print that. If not, but they enter a task in the list, use that. If neither, say "more info needed." -->




# Bias, Risks, and Limitations

<!-- This section is meant to convey both technical and sociotechnical limitations. -->

Significant research has explored bias and fairness issues with language models (see, e.g., [Sheng et al. (2021)](https://aclanthology.org/2021.acl-long.330.pdf) and [Bender et al. (2021)](https://dl.acm.org/doi/pdf/10.1145/3442188.3445922)). Predictions generated by the model may include disturbing and harmful stereotypes across protected classes; identity characteristics; and sensitive, social, and occupational groups.


## Recommendations

<!-- This section is meant to convey recommendations with respect to the bias, risk, and technical limitations. -->





# Training Details

## Training Data

<!-- This should link to a Data Card, perhaps with a short stub of information on what the training data is all about as well as documentation related to data pre-processing or additional filtering. -->

More information on training data needed


## Training Procedure

<!-- This relates heavily to the Technical Specifications. Content here should link to that section when it is relevant to the training procedure. -->

### Preprocessing

More information needed

### Speeds, Sizes, Times

<!-- This section provides information about throughput, start/end time, checkpoint size if relevant, etc. -->

More information needed
 
# Evaluation

<!-- This section describes the evaluation protocols and provides the results. -->

## Testing Data, Factors & Metrics

### Testing Data

See [datasheet](./datasheet.md) for more details.

### Factors

<!-- These are the things the evaluation is disaggregating by, e.g., subpopulations or domains. -->

More information needed

### Metrics

<!-- These are the evaluation metrics being used, ideally with a description of why. -->

More information needed

## Results 

More information needed

# Model Examination

More information needed

# Environmental Impact

<!-- Total emissions (in grams of CO2eq) and additional considerations, such as electricity usage, go here. Edit the suggested text below accordingly -->

Carbon emissions can be estimated using the [Machine Learning Impact calculator](https://mlco2.github.io/impact#compute) presented in [Lacoste et al. (2019)](https://arxiv.org/abs/1910.09700).

- **Hardware Type:** MacOS Intel CPU
- **Hours used:** 12ish
- **Carbon Emitted:** a little bit

## Model Architecture and Objective

More information needed

# How to Get Started with the Model

Use the code below to get started with the model.

<details>
<summary> Click to expand </summary>

More information needed

</details>