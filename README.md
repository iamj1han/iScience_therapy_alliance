# iScience_therapy_alliance

<b>File names under this repository ; main objective of the file/codes</b>

1. Transcript_preprocessing.ipynb ; Chop and preprocess therapy session transcript files.
              
This Notebook will:
read all the transcripts in '/Users/Heisig/Jihan/Transcripts/' 
create split subject interviewer transcripts here: /Users/Heisig/Jihan/Transcripts/SplitTranscripts/'
create split subject interviewer turn transcripts here: /Users/Heisig/Jihan/Transcripts/SplitTurnsTranscripts'
create POS tagged tokens using stanza and saves them in: '/Users/Heisig/Jihan/POS/'
create a few plots and stats (optional)
Linguistic Inquiry Word Count software (LIWC-2015 edition) will be then run on split subject interviewer transcript.

2. Part_of_speech_tag_transition_matrix.ipynb ; Generate Part of Speech (POS) tags ad transition matrix.

This Notebook will:
read (or reconstruct) the POS file containing all the POS for each sentence
compute word frequencies
construct the transition matrix and the histograms

3. Language_feature_selection.ipynb ; Join LIWC, POS, clinical data and perform statistical tests to find statistically significant language features.

This Notebook will:
read session scores LIWC category counts, Part of Speech frequencies and transitions together along with alliance. 
perform feature selection by running F-test.

4. iScience_Fig_1_2_3.Rmd ; Generate Figure 1, 2, and 3 of the paper

Fig 1 - histogram of patient and therapist first-person pronoun usage and correlations with alliance.
Fig 2 - histogram of patient and therapist non-fluency and correlations with alliance.
Fig 3 - extract average repayment fraction of subjects playing trust game as objective index of trust and run mediation analysis to see if it mediates
          the association between first-person pronoun features and alliance.
