# iScience_therapy_alliance

<b>File names under this repository ; description of the file/codes</b>

1. Transcript_preprocessing.ipynb ; Chop and preprocess therapy session transcript files.
              
This Notebook will:
read all the transcripts in '/Users/Heisig/Jihan/Transcripts/'; 
create split subject interviewer transcripts here: /Users/Heisig/Jihan/Transcripts/SplitTranscripts/';
create split subject interviewer turn transcripts here: /Users/Heisig/Jihan/Transcripts/SplitTurnsTranscripts';
create POS tagged tokens using stanza and saves them in: '/Users/Heisig/Jihan/POS/';
create a few plots and stats (optional);
Linguistic Inquiry Word Count software (LIWC-2015 edition) will be then run on split subject interviewer transcript.

2. Part_of_speech_tag_transition_matrix.ipynb ; Generate Part of Speech (POS) tags transition matrix.

This Notebook will:
read (or reconstruct) the POS file containing all the POS for each sentence;
compute word frequencies;
construct the transition matrix and the histograms

3. Language_feature_selection.ipynb ; Join LIWC, POS, clinical data and perform statistical tests to find statistically significant language features.

This Notebook will:
read session scores LIWC category counts, Part of Speech frequencies and transitions together along with alliance; 
perform feature selection by running F-test.
          
4. language.csv

De-identified langauge feature dataset extracted (LIWC-2015 and POS transition) in the sessions and associated clinical variables. Data dictionary: Closeness/Dependence/Anxiety - revised adult attachment scores of patients, Prev_alliance - strength of patient-rated alliance with the therapist in the previous treatment prior to the current one, Sex (0 = male patient, 1 = female patient), Telehealth (0 = in-person, 1 = telehealth), Therapist_experience (0 = trainee psychologist/psychaitrist with lifetime patients <10, 1 = trainee psychologist/psychiatrist with lifetime patients >=10 & <100, 2 = faculty psychotherapists with lifetime patients 100>=).

5. trustgame.csv

Trust game indices of each subject (ID) who played trustee. Data dictionary: Role - role of the trustee in real-world psychotherapy relationship, i.e. P = patient, T = therapist; Repayment fraction from round 1 to 10 made by trustee, i.e. rf1-rf10; investor total scores at the end of the game; trustee (i.e. subject) total scores at the end of the game; Scores_Total - the sum of investor and trustee total scores at the end of the game.

6. iScience_Fig_1_2_3.Rmd ; Generate Figure 1, 2, and 3 of the paper

This code will read language.csv and trustgame.csv and generate:
Fig 1 - histogram of patient and therapist first-person pronoun usage and correlations with alliance;
Fig 2 - histogram of patient and therapist non-fluency and correlations with alliance;
Fig 3 - extract average repayment fraction of subjects playing trust game as objective index of trust and run mediation analysis to see if it mediates
          the association between first-person pronoun features and alliance.

