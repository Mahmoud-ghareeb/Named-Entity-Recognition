# Named Entity Recognition (NER) Using LSTM

Named Entity Recognition (NER) is a fundamental task in the field of Natural Language Processing (NLP). It pertains to the identification and classification of named entities, such as names of persons, organizations, locations, and more, within a given text.


## Highlights:

- **Bidirectional LSTM**: Bidirectional LSTM's inherent ability to remember long-term dependencies from the bast and future makes it an excellent choice for NER tasks. It can identify and predict named entities across sentences of different lengths.

- **Data Management with `tf.data.Dataset.from_generator`**: 
    - Instead of loading the entire dataset into memory, I used TensorFlow's `from_generator` method.

- **TimeDistributed Layer**:
    - Our model architecture includes the `TimeDistributed` layer. This layer applies a dense operation to each time sequence step individually. It's a critical component for sequence tagging tasks such as NER, where the aim is to predict a tag for every individual word in the input.


## Conclusion:

The LSTM-based approach to Named Entity Recognition effectively demonstrates the capability and adaptability of recurrent networks for this NLP task. By leveraging `tf.data.Dataset.from_generator`, our solution can efficiently handle vast amounts of data without any memory constraints. Furthermore, the `TimeDistributed` layer enables granular per-token predictions, rendering our model both robust and versatile.

