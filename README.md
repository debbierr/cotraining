# Inferring aspect-specific opinion structure in product reviews using co-training
This is an algorithm for aspect-based sentiment analysis using co-training, a semi-supervised machine learning algorithm that partitions the machine learning features into two sufficient and uncorrelated "views" and then self-learns.

### Required data sets

The application uses data provided by third parties.  To use this project, you'll need to download and unzip:

http://www.cs.uic.edu/~liub/FBS/CustomerReviewData.zip (Hu and Liu, KDD-2004)

http://metashare.ilsp.gr:8080/repository/browse/semeval-2014-absa-test-data-gold-annotations/b98d11cec18211e38229842b2b6a04d77591d40acd7542b7af823a54fb03a155/ (Ganu et al., 2009)

Many thanks to the authors and annotators of these two data sets.

### Executable version

The executable version of this project is in the bin directory.

Command line arguments can be inspected by running the command:  
`java -jar processreviews-sept2014.jar help`

The Stanford CoreNLP models are also required (stanford-corenlp-3.3.1-models.jar) and should be put in the bin directory (if running from the command line) and the lib directory (if using the source code itself).  This can be downloaded from http://search.maven.org/#browse%7C304725258

### Source code

ProcessReviews.java is the main class.

To use the source code, you'll have to edit a couple of things to start:
- in jwnl14_file_properties.xml, you'll need to update the *dictionary_path* parameter
- in *ProcessReviews.java*, you'll have to update the *defaultRootDir* variable to point to the required data sets

You can use the *exportjar.jardesc* file in Eclipse to package up a new executable jar file.

### Citing

If using this code, please cite the paper:

    @inproceedings{carter:aspectspecificcotraining,
     author = {Carter, Dave and Inkpen, Diana},
     title = {Inferring Aspect-Specific Opinion Structure in Product Reviews using Co-training},
     booktitle = {Proceedings of CICLing-2015},
     series = {Lecture Notes in Computer Science 9042},
     year = {2015},
     isbn = {978-3-319-18117-2},
     location = {Cairo, Egypt},
     pages = {225--240},
     numpages = {16},
     url = {http://dx.doi.org/10.1007/978-3-319-18117-2_17},
     doi = {10.1007/978-3-319-18117-2_17},
     publisher = {Springer-Verlag},
     address = {Berlin, Heidelberg},
    } 

