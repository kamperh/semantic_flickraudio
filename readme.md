Semantic Keyword Spotting Labels for the Flickr Audio Captions Corpus
=====================================================================

Overview
--------
This corpus was collected to investigate how a model trained on images paired
with untranscribed speech could be used to perform semantic keyword spotting (a
new speech retrieval task). The data set and associated task is described in:

- H. Kamper, S. Settle, G. Shakhnarovich, and K. Livescu, "Semantic keyword
  spotting by learning from images and speech," 2017.

If you use this data, please cite the above work, as well as the
[ASRU'15](http://people.csail.mit.edu/dharwath/papers/Harwath_ASRU-15.pdf)
paper from the group at MIT that collected the original Flickr Audio Captions
Corpus (see below).


Semantic keyword spotting
-------------------------
In standard keyword spotting, the task is to retrieve all utterances in a
search collection containing spoken instances of a written query keyword. In
*semantic keyword spotting*, instead of matching keywords exactly, the task is
to retrieve all utterances that would be relevant if you searched for that
keyword, irrespective of whether that keyword occurs in the utterance or not.
For instance, given they query 'sidewalk', a model should return not only
utterances containing the word exactly, but also speech like 'an old couple
crossing a street'.


The corpus
----------
The file [keywords.txt](data/keywords.txt) lists the 67 keywords used in the
task. The semantic labelling of utterances using these keywords are given in
two files.

The CSV file
[semantic\_flickraudio\_labels.csv](data/semantic_flickraudio_labels.csv) gives
hard annotations for keywords that are relevant for specific utterances. The
CSV file
[semantic\_flickraudio\_counts.csv](data/semantic_flickraudio_counts.csv) gives
the actual annotator counts. In this file, `white=3|grass=1|dogs=5` for
instance indicates that three out of five annotators marked as relevant the
keyword 'white', one 'grass', and all five 'dogs'.

We only provide the semantic labels, without the associated audio or images.
The original Flickr Audio Captions Corpus can be obtained
[here](https://groups.csail.mit.edu/sls/downloads/flickraudio/), while the
original Flickr8k image corpus can be obtained
[here](http://nlp.cs.illinois.edu/HockenmaierGroup/Framing_Image_Description/KCCA.html).
Please cite these studies as well when using our corpus.

Semantic labels are only available for 1000 test utterances in the corpus, one
for each unique test image in Flickr8k.


License
-------
The data is distributed under the Creative Commons Attribution-ShareAlike
license ([CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)).
