# ECBM4040 Final Project: Composing Music With Recurrent Neural Networks

![title page](https://github.com/ecbme4040/e4040-2020fall-Project-MYEY-wy2346-qy2231/blob/main/image/title%20pic.png)

### Author: 
Wenjun Yang (wy2347) || Qihang Yang(qy2231)


# Project Description:
Our project aims at reconstructing the architecture of the Bi-axial LSTM model, and composing music based on the model. The code of the original paper is written in theano,  while we managed to understand the practical implementation and build our model in tensorflow and keras according to the description in the original paper. After epochs of training, we manage to have some satisfying results. Our music now has a sense of chords.


# How to see the result and better leverage our model
To see a thorough workthrough of our project, please go to **Report.ipynb** where we provide detailed explaination of our idea, model and implementation. For the music we have generated, you can easily find them under **samples** directory.

Due to limitation of storage space of github, unfortunately, the model file can't be pushed into github, however you may find the saved model file in following link. You can build a model and load the weight, so that you can immediately generate music yourself.

All the function we defined are located in utils folder, and organized into 3 scripts, prep.py for all functions we need in data preparation, model.py for the model and custom loss function we use and visualizeMIDI.py for music visualization.

Link to saved model:
https://drive.google.com/file/d/1SFWloQ0ukVv9Lr7ieN98HmfeFsEEWxJz/view?usp=sharing

Note: Download it and save it back to the folder specified above, then you can easily proceed to the next step. 
We are opening view access to everyone with lionmail, if you have trouble downloading that, please feel free to contact us.

# Directory Walk-through
The main jupyter notebook is Report.ipynb. The pdf version of general report is named as E4040.2020Fall.MYEY.report.wy2347.qy2231.pdf.
You can find the dataset we use under data folder and the samples we generate under samples folder.
The functions we defined are under utils folder.
* prep.py: contains all the function related to data preprocessing and postprocessing. For example, there we have functions that transform MIDI file to state matrix and tranform state matrix back to MIDI file, besides, there are input data generator and anything related to extract input data from state matrix.
* model.py: where we define the architecture of our model along with the predict and compose function.
* visualizeMIDI.py: everything that related to MIDI file visualization, from serializing a MIDI file, transforming the sequence into pandas dataframe and outputing figures.

# Organization of this directory
```
./
├── E4040.2020Fall.MYEY.report.wy2347.qy2231.pdf
├── README.md
├── Report.ipynb
├── data
│   ├── midifile.zip
│   └── music
├── image
│   ├── Data Prep.png
│   ├── architecture.png
│   ├── model.png
│   ├── title pic.png
│   └── workflow.png
├── samples
└── utils
    ├── model.py
    ├── prep.py
    └── visualizeMIDI.py
```