### Chat Assistant
This repo mainly focuses on constructing a custom dataset of daily conversational dialogues and leveraging advanced neural networks to build a Customer Support Chat Assistant. The dataset is composed of pairs of questions and answers, formatted as text. The core of the project is the implementation of a sequence-to-sequence (Seq2Seq) model with attention mechanisms and beam search capability for decoding the output.

### Custom Dataset Construction
The dataset is designed to simulate real-life conversations. Each dialogue is a pair of sentences, with the first being the question and the second the corresponding answer. The dataset is preprocessed to include special tokens such as start and end tokens, which help the model understand the beginning and end of a sequence.

### Seq2Seq Model with Attention
The Seq2Seq model consists of two main parts: the encoder and the decoder. The encoder processes the input question and generates a context vector, which is then used by the decoder to generate the response.

1. **Encoder and Decoder**: The encoder is a neural network that processes the input sequence (question) and compresses the information into a context vector. This context vector encapsulates the meaning of the input sequence in a fixed-length representations then the decoder uses context vector to generate the output sequence (answer) one word at a time. 
2. **Attention Mechanism**: The attention mechanism allows the model to focus on different parts of the input sequence at each step of the decoding process. This is achieved by calculating attention weights, which are used to create a weighted sum of the encoder's hidden states. This weighted sum, combined with the final state of the encoder, forms a more informative context vector for the decoder.
