# Fake-news-detection-using-LSTM-in-deep-learning
#### Date:June30 -2025
- **Data collection:**
Dataset collected from kaggle ,dataset names Fake.csv,True.csv 
[Dataset link:](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)

- **Dataset description:**
Fake and True csv files contains 20k+ values it contains columns title,explain_texts,subject,date ...

- **Data handle:**
pandas to read the csv files and create new column to assign `label: 0-fake,1-real`

- **Data clean:**
NLTK to clean the texts. It had text to lower, remove stopwords,non wordcharactors ... and cleaned text to store in new column.

- **Data spliting:**
data to be split by training 75% data ,testing 25% data and merge the files.It contains equal label values for both 0(Fake),1(Real).

- **Text preprocessing:**
Tensorflow-keras:
1.`Tokenizer` - It is split the text to tokens and assign index numerical values and pickle to save tokens.
2.`Text to sequence` ,text to be sequences of numerical values.(collection of numerical values)
3.`ped_sequences` - It is padding to align all numerical values to same length.( it was align same length and add dummy value
zero.) 

- **LSTM architecture:**
1.`Embedding` - It had input_dimension(maximum vocabulary words) , output_dimension (dimension of embedding vectors),input_length(max length of input)
2.`BidirectionalLSTM` - [Long Short-Term Memory] one of Recurrent Neural Network(RNN).It was processing the text into forward and backward,return_sequences=True this to be moves sequences of inputs to next layers.
3.`Dense` it was a fully connected layer and output active 1 neuran.

- **Early stopping:**
callbacks to stop early training to prevent overfitting.

- **Model save:**
Model training and then save in hierarchical format.

- **Result:**
model increase it's accuracy at above epoch 5.
![output](https://github.com/user-attachments/assets/1891ac6f-2aef-48d0-a82d-6582751970e7)

`Accuracy: 0.9735
Test Accuracy: 0.9734`

- **Prediction:**
prediction greater than 0.5 -Real
otherwise Fake.


 




