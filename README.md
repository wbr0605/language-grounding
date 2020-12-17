# Awesome Language Grounding

A curated list of resources for language grounding research.

## Contributing
Please feel free to email Borui Wang (borui.wang@yale.edu).

## Table of Contents

- [Surveys](#surveys)
- [Courses](#courses)
- [Papers](#papers)
  - [Language Grounding to Vision](#vision)
  - [Language Grounding to Robotics](#robotics)
- [Datasets](#datasets)

## Surveys

* Cross-Language Information Retrieval [[book](http://www.iro.umontreal.ca/~nie/IFT6255/Books/CLIR.pdf)]


[**Experience Grounds Language**](https://arxiv.org/pdf/2004.10151.pdf) [[Paper](https://arxiv.org/pdf/2004.10151.pdf)]

Yonatan Bisk, Ari Holtzman, Jesse Thomason, Jacob Andreas, Yoshua Bengio, Joyce Chai, Mirella Lapata, Angeliki Lazaridou, Jonathan May, Aleksandr Nisnevich, Nicolas Pinto, Joseph Turian (EMNLP 2020)

This survey posits that the present success of representation learning approaches trained on large, text-only corpora requires the parallel tradition of research on the broader physical and social context of language to address the deeper questions of communication.


## Courses

[**Carnegie Mellon University 10-808: Language Grounding to Vision and Control (Fall 2017)**](https://katefvision.github.io/LanguageGrounding/) [[Course Link](https://katefvision.github.io/LanguageGrounding/)]

Instructor: Prof. Katerina Fragkiadaki

This is a seminar course that visits recent progress on the problem of language acquisition through pairing of multiple modalities (vision, haptics, audio etc), as well as active interaction with the world. The central questions/topics covered are: How can language help accelerate learning of an autonomous agent? How humans acquire language and why? Inductive biases for strong generalization. Architectures for agent capable of compositional grounding of language. State representation of video visual scenes and imaginations from story reading. Language for high level planning and control. Neural-symbolic architectures for hierarchical symbolic grounding.


[**University of Texas at Austin CS 395T: Grounded Natural Language Processing (Spring 2021)**](https://www.cs.utexas.edu/~mooney/gnlp/) [[Course Link](https://www.cs.utexas.edu/~mooney/gnlp/)]

Instructor: Prof. Raymond J. Mooney

This course is a graduate research seminar in grounded natural language processing (GNLP), a subarea of AI that studies the connection between natural language and perception and action in the world. It makes connections between natural language processing (NLP) and computer vision, robotics, and computer graphics. Almost all work in the area uses machine learning to learn the connection between language and perception and/or action from some form of multi-modal training data.


## Papers
### Language Grounding to Vision

[**Illustrative Language Understanding:
Large-Scale Visual Grounding with Image Search**](https://www.aclweb.org/anthology/P18-1085.pdf) [[Paper](https://www.aclweb.org/anthology/P18-1085.pdf)]

Jamie Ryan Kiros, William Chan, Geoffrey E. Hinton (ACL 2018)

This paper introduces Picturebook, a large-scale lookup operation to ground language via ‘snapshots’ of our physical world accessed through image search.

[**Learning Visually Grounded Sentence Representations**](https://arxiv.org/pdf/1707.06320.pdf) [[Paper](https://arxiv.org/pdf/1707.06320.pdf)]

Douwe Kiela, Alexis Conneau, Allan Jabri, Maximilian Nickel (NAACL 2018)

This paper investigates grounded sentence representations, where they train a sentence encoder to predict the image features of a given caption. They examine the quality of the learned representations on a variety of standard sentence representation quality benchmarks, showing improved performance for grounded models over non-grounded ones. 

[**Grounding language acquisition by training semantic parsers using captioned videos**](https://www.aclweb.org/anthology/D18-1285.pdf) [[Paper](https://www.aclweb.org/anthology/D18-1285.pdf)]

Candace Ross, Andrei Barbu, Yevgeni Berzak, Battushig Myanganbayar, Boris Katz (EMNLP 2018)

This paper develops a semantic parser that is trained in a grounded setting using pairs of videos captioned with sentences. This setting is both data-efficient, requiring little annotation, and similar to the experience of children where they observe their environment and listen to speakers. The semantic parser recovers the meaning of English sentences despite not having access to any annotated sentences. It does so despite the ambiguity inherent in vision where a sentence may refer to any combination of objects, object properties, relations or actions taken by any agent in a video. For this task, the authors collected a new dataset for grounded language acquisition. Learning a grounded semantic parser — turning sentences into logical forms using captioned videos — can significantly expand the range of data that parsers can be trained on, lower the effort of training a semantic parser, and ultimately lead to a better understanding of child language acquisition. 

[**Visually Grounded Neural Syntax Acquisition**](https://arxiv.org/abs/1906.02890) [[Paper](https://arxiv.org/abs/1906.02890)]

Haoyue Shi, Jiayuan Mao, Kevin Gimpel, Karen Livescu (ACL 2019)

This paper presents the Visually Grounded Neural Syntax Learner (VG-NSL), an approach for learning syntactic representations and structures without any explicit supervision. The model learns by looking at natural images and reading paired captions. VG-NSL generates constituency parse trees of texts, recursively composes representations for constituents, and matches them with images.

[**Incorporating Visual Semantics into Sentence Representations within a Grounded Space**](https://www.aclweb.org/anthology/D19-1064.pdf) [[Paper](https://www.aclweb.org/anthology/D19-1064.pdf)]

Patrick Bordes, Eloi Zablocki, Laure Soulier, Benjamin Piwowarski, Patrick Gallinari (EMNLP 2019)

This paper proposes to transfer visual information to textual representations by learning an intermediate representation space: the grounded space. They further propose two new complementary objectives ensuring that (1) sentences associated with the same visual content are close in the grounded space and (2) similarities between related elements are preserved across modalities. They show that this model outperforms the previous state-of-the-art on classification and semantic relatedness tasks.


[**GQA: A New Dataset for Real-World Visual Reasoning and Compositional Question Answering**](https://arxiv.org/pdf/1902.09506.pdf) [[Paper](https://arxiv.org/pdf/1902.09506.pdf)]

Drew A. Hudson, Christopher D. Manning (CVPR 2019)

This paper introduces GQA, a new dataset for real-world visual reasoning and compositional question answering, seeking to address key shortcomings of previous VQA datasets. They have developed a strong and robust question engine that leverages scene graph structures to create 22M diverse reasoning questions, all come with functional programs that represent their semantics. They use the programs to gain tight control over the answer distribution and present a new tunable smoothing technique to mitigate question biases.

[**VideoBERT: A Joint Model for Video and Language Representation Learning**](https://arxiv.org/pdf/1904.01766.pdf) [[Paper](https://arxiv.org/pdf/1904.01766.pdf)]

Chen Sun, Austin Myers, Carl Vondrick, Kevin Murphy, Cordelia Schmid

This paper proposes a joint visual-linguistic model to learn high-level features without any explicit supervision. They build upon the BERT model to learn bidirectional joint distributions over sequences of visual and linguistic tokens, derived from vector quantization of video data and off-the-shelf speech recognition outputs, respectively. They use VideoBERT in numerous tasks, including action classification and video captioning. They show that it can be applied directly to open-vocabulary classification, and confirm that large amounts of training data and cross-modal information are critical to performance. Furthermore, They outperform the state-of-the-art on video captioning, and quantitative results verify that the model learns high-level semantic features.



### Language Grounding to Robotics

[**ALFRED: A Benchmark for Interpreting Grounded Instructions for Everyday Tasks**](https://arxiv.org/pdf/1912.01734.pdf) [[Paper](https://arxiv.org/pdf/1912.01734.pdf)] [[Project Page](https://askforalfred.com/)]

Mohit Shridhar, Jesse Thomason, Daniel Gordon, Yonatan Bisk, Winson Han, Roozbeh Mottaghi, Luke Zettlemoyer, Dieter Fox (CVPR 2020)

This paper presents ALFRED (Action Learning From Realistic Environments and Directives), a benchmark for learning a mapping from natural language instructions and egocentric vision to sequences of actions for household tasks. ALFRED includes long, compositional tasks with non-reversible state changes to shrink the gap between research benchmarks and real-world applications. ALFRED consists of expert demonstrations in interactive visual environments for 25k natural language directives. 

## Datasets

* GQA from Stanford University [[Dataset](https://cs.stanford.edu/people/dorarad/gqa/vis.html)]
* Visual Commensen Reasoning (VCR) from University of Washington and AI2 [[Dataset](https://visualcommonsense.com/)]
* MS COCO [[Dataset](https://cocodataset.org/#home)]
* Visual Genome from Stanford [[Dataset](https://visualgenome.org/)]
* ALFRED from University of Washington [[Dataset](https://askforalfred.com/)]
