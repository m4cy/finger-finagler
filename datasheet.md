# Datasheet: Piano Fingering Dataset

Author: Macy Huang

Organization: University of Texas at Austin


## Motivation

*The questions in this section are primarily intended to encourage dataset creators to clearly articulate their reasons for creating the dataset and to promote transparency about funding interests.*

1. **For what purpose was the dataset created?** Was there a specific task in mind? Was there a specific gap that needed to be filled? Please provide a description.

	This dataset was created to be a publicly available academic resource for researchers interested in the problem of Automatic Piano Fingering. 

2. **Who created this dataset (e.g. which team, research group) and on behalf of which entity (e.g. company, institution, organization)**?

	This dataset was created in the process of training and evaluating and statistics-based approach to Automatic Piano Fingering and was produced by various researchers at the Kyoto University and Kisarazu College in Japan. 

3. **What support was needed to make this dataset?** (e.g. who funded the creation of the dataset? If there is an associated grant, provide the name of the grantor and the grant name and number, or if it was supported by a company or government agency, give those details.)

	This dataset did not require funding to be created.

4. **Any other comments?**

	The creators of the dataset request that their paper be explicitly cited and only allow nonprofit, academic use.

## Composition

*Dataset creators should read through the questions in this section prior to any data collection and then provide answers once collection is complete. Most of these questions are intended to provide dataset consumers with the information they need to make informed decisions about using the dataset for specific tasks. The answers to some of these questions reveal information about compliance with the EU’s General Data Protection Regulation (GDPR) or comparable regulations in other jurisdictions.*

1. **What do the instances that comprise the dataset represent (e.g. documents, photos, people, countries)?** Are there multiple types of instances (e.g. movies, users, and ratings; people and interactions between them; nodes and edges)? Please provide a description.

	The dataset is comprised of sheet music from Western classical music composers. These pieces all fall in the public domain and represent several eras of classical music, from baroque to more contemporary styles.

2. **How many instances are there in total (of each type, if appropriate)?**

	The dataset contains pieces by Bach, Mozart, Chopin, Beethoven, Debussy, Ravel, Schubert, Grieg, Mussorgsky, Liszt, Rachmaninoff, Brahms, Joplin, Dvorak, Mendelssohn, Faure, Tchaikovsky, Scarlatti, Saint-Saens, Satie, Scriabin, Bartok, and Albeniz for a total of 150 pieces. These composers are not represented in equal proportion and Bach and Beethoven pieces make up more of the dataset comparatively.

3. **Does the dataset contain all possible instances or is it a sample (not necessarily random) of instances from a larger set?** If the dataset is a sample, then what is the larger set? Is the sample representative of the larger set (e.g. geographic coverage)? If so, please describe how this representativeness was validated/verified. If it is not representative of the larger set, please describe why not (e.g. to cover a more diverse range of instances, because instances were withheld or unavailable).

	This dataset does not contain all possible types of music and is limited strictly to sampling some of the classical music canon. 

4. **What data does each instance consist of?** "Raw" data (e.g. unprocessed text or images) or features? In either case, please provide a description.

	The actual raw data consists of files for each piece in the format of (note ID) (onset time) (offset time) (spelled pitch) (onset velocity) (offset velocity) (channel) (finger number) for each note in a piece of music.

5. **Is there a label or target associated with each instance?** If so, please provide a description.

	The label associated with each note is the fingering a professional pianist labeled it with (referred to as finger number above).

8. **Are there recommended data splits (e.g. training, development/validation, testing)?** If so, please provide a description of these splits, explaining the rationale behind them.

	There are not recommended data splits. For the purposes of our model, we randomly sample some to be training, validating, and testing sets.

9. **Are there any errors, sources of noise, or redundancies in the dataset?** If so, please provide a description.

	There are no errors or redundancies in the dataset.

10. **Is the dataset self-contained, or does it link to or otherwise rely on external resources (e.g. websites, tweets, other datasets)?** If it links to or relies on external resources, a) are there guarantees that they will exist, and remain constant, over time; b) are there official archival versions of the complete dataset (i.e., including the external resources as they existed at the time the dataset was created); c) are there any restrictions (e.g. licenses, fees) associated with any of the external resources that might apply to a future user? Please provide descriptions of all external resources and any restrictions associated with them, as well as links or other access points, as appropriate.

	The dataset is self-contained and does not contain references to any external resources which could fall out of maintenance or become paywalled.

11. **Does the dataset contain data that might be considered confidential (e.g. data that is protected by legal privilege or by doctor-patient confidentiality, data that includes the content of individuals' non-public communications)?** If so, please provide a description.

	Data in the datset is public domain.

12. **Does the dataset contain data that, if viewed directly, might be offensive, insulting, threatening, or might otherwise cause anxiety?** If so, please describe why.

	The data is unoffensive since it is just scores of music.

13. **Does the dataset relate to people?** If not, you may skip the remaining questions in this section.

	No.

14. **Does the dataset identify any subpopulations (e.g. by age, gender)?** If so, please describe how these subpopulations are identified and provide a description of their respective distributions within the dataset.

	Skip.

15. **Is it possible to identify individuals (i.e., one or more natural persons), either directly or indirectly (i.e., in combination with other data) from the dataset?** If so, please describe how.

	Skip.

16. **Does the dataset contain data that might be considered sensitive in any way (e.g. data that reveals racial or ethnic origins, sexual orientations, religious beliefs, political opinions or union memberships, or locations; financial or health data; biometric or genetic data; forms of government identification, such as social security numbers; criminal history)?** If so, please provide a description.

	Skip.


## Collection

*As with the previous section, dataset creators should read through these questions prior to any data collection to flag potential issues and then provide answers once collection is complete. In addition to the goals of the prior section, the answers to questions here may provide information that allow others to reconstruct the dataset without access to it.*

1. **How was the data associated with each instance acquired?** Was the data directly observable (e.g. raw text, movie ratings), reported by subjects (e.g. survey responses), or indirectly inferred/derived from other data (e.g. part-of-speech tags, model-based guesses for age or language)? If data was reported by subjects or indirectly inferred/derived from other data, was the data validated/verified? If so, please describe how.

	The data associated with each musical piece was collected based on fingering assignments from 1-2 professional pianists. Onset/offset timing and velocity values included in the data were synthesized from score editing software and not collected from human performances.

2. **What mechanisms or procedures were used to collect the data (e.g. hardware apparatus or sensor, manual human curation, software program, software API)?** How were these mechanisms or procedures validated?

	Score editing software, manual human curation. There is no information about how these procedures were validated.

3. **If the dataset is a sample from a larger set, what was the sampling strategy (e.g. deterministic, probabilistic with specific sampling probabilities)?**

	No sampling strategy.

4. **Who was involved in the data collection process (e.g. students, crowdworkers, contractors) and how were they compensated (e.g. how much were crowdworkers paid)?**

	Professional pianists were paid for their time to label fingerings on each piece of music.

5. **Over what timeframe was the data collected?** Does this timeframe match the creation timeframe of the data associated with the instances (e.g. recent crawl of old news articles)? If not, please describe the timeframe in which the data associated with the instances was created. Finally, list when the dataset was first published.

	No information provided.

7. **Were any ethical review processes conducted (e.g. by an institutional review board)?** If so, please provide a description of these review processes, including the outcomes, as well as a link or other access point to any supporting documentation.

	No information provided but the Automatic Piano Fingering problem does not present any ethical concerns.

8. **Does the dataset relate to people?** If not, you may skip the remainder of the questions in this section.

	No.

9. **Did you collect the data from the individuals in question directly, or obtain it via third parties or other sources (e.g. websites)?**

	*Your Answer Here*

10. **Were the individuals in question notified about the data collection?** If so, please describe (or show with screenshots or other information) how notice was provided, and provide a link or other access point to, or otherwise reproduce, the exact language of the notification itself.

	*Your Answer Here*

11. **Did the individuals in question consent to the collection and use of their data?** If so, please describe (or show with screenshots or other information) how consent was requested and provided, and provide a link or other access point to, or otherwise reproduce, the exact language to which the individuals consented.

	*Your Answer Here*

12. **If consent was obtained, were the consenting individuals provided with a mechanism to revoke their consent in the future or for certain uses?** If so, please provide a description, as well as a link or other access point to the mechanism (if appropriate).

	*Your Answer Here*

13. **Has an analysis of the potential impact of the dataset and its use on data subjects (e.g. a data protection impact analysis) been conducted?** If so, please provide a description of this analysis, including the outcomes, as well as a link or other access point to any supporting documentation.

	*Your Answer Here*

14. **Any other comments?**

	*Your Answer Here*


## Preprocessing / Cleaning / Labeling

*Dataset creators should read through these questions prior to any pre-processing, cleaning, or labeling and then provide answers once these tasks are complete. The questions in this section are intended to provide dataset consumers with the information they need to determine whether the “raw” data has been processed in ways that are compatible with their chosen tasks. For example, text that has been converted into a “bag-of-words” is not suitable for tasks involving word order.*

1. **Was any preprocessing/cleaning/labeling of the data done (e.g. discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)?** If so, please provide a description. If not, you may skip the remainder of the questions in this section.

	Preprocessing of this data was done in the form of parsing input and label information out of the raw data and making labels classifiable.

2. **Was the "raw" data saved in addition to the preprocessed/cleaned/labeled data (e.g. to support unanticipated future uses)?** If so, please provide a link or other access point to the "raw" data.

	Yes, it is stored at the dataset's [website](https://beam.kisarazu.ac.jp/~saito/research/PianoFingeringDataset/).

3. **Is the software used to preprocess/clean/label the instances available?** If so, please provide a link or other access point.

	The algorithm for processing the data can be viewed in the Python notebook.

4. **Any other comments?**

	*Your Answer Here*


## Uses

*These questions are intended to encourage dataset creators to reflect on the tasks  for  which  the  dataset  should  and  should  not  be  used.  By  explicitly highlighting these tasks, dataset creators can help dataset consumers to make informed decisions, thereby avoiding potential risks or harms.*

1. **Has the dataset been used for any tasks already?** If so, please provide a description.

	No.

2. **Is there a repository that links to any or all papers or systems that use the dataset?** If so, please provide a link or other access point.

	No.

3. **What (other) tasks could the dataset be used for?**

	This dataset is most useful for the APF problem and does not have much value outside of it.

4. **Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses?** For example, is there anything that a future user might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g. stereotyping, quality of service issues) or other undesirable harms (e.g. financial harms, legal risks) If so, please provide a description. Is there anything a future user could do to mitigate these undesirable harms?

	The processing of the fingering files from the sheet music may lose too much information. Future use of this dataset might involve different processing to preserve different parts of the musical notation.

5. **Are there tasks for which the dataset should not be used?** If so, please provide a description.

	Not especially, it just is not relevant for many tasks.

6. **Any other comments?**

	*Your Answer Here*