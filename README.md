# Plucking-Style-Detection
The main components presented here are **string number classification** and **plucking style classification**. 

The data used in this project are two subsets of the [IDMT-SMT-GUITAR dataset](https://www.idmt.fraunhofer.de/en/business_units/m2d/smt/guitar.html)\
Features and labels extracted from the recordings are available at the the `pkl` directories. 

The first subset contains single note recordings. The single-pluck recordings have corresponding annotations regarding the pitch, onset, string number, and plucking style. However, all recordings in the first subset are played with a pick. There is thus only one plucking style involved, making it inappropriate for training and testing the plucking style classifier. \
 `Exps_on_subset_1.ipynb` presents experiments performed on this subset, including the string classifier and pitch estimation algorithm. Corresponding features and labels are in `dataset1_pkl`. 

The second subset contains realistic guitar phrases with note-level annotations regarding the pitch, onset, string number, and plucking style. It covers all the three plucking styles (fingerstyle, picked, and muted). According to the annotated onsets and offsets, the phrases were split into a total of 4,812 single notes, which were then used for training and testing the plucking style classifier. The monophonic portion of this subset was used for developing the string number classifier.  \
`Exps_on_subset_2.ipynb` presents experiments conducted on this subset, including the plucking style classifier, string classifier, and pitch estimation. Corresponding features and labels are in `dataset2_pkl` and `dataset2_pkl_mono`. 

The two subsets were then combined to train and test another string classifier. The notes that can only be played on one string are filtered out from the dataset. This experiment is available in `String_number_combined.ipynb`. Corresponding features and labels are in `dataset1_2_pkl`. 


