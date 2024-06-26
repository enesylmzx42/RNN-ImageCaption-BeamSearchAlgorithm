# Image Captioning

Image captioning is a fascinating process where a machine-learning model crafts textual descriptions or captions for images. It merges computer vision techniques to grasp image content with natural language processing (NLP) techniques for generating coherent and descriptive text.

## Used Concepts and Technologies

- NLP
- RNN
- LSTM - GRU
- Beam Search Algorithm
- Greedy Decoder
- Tensorflow
- Keras
- EfficientNetV2B3
- Streamlit



## Dataset 

The Flickr8k dataset comprises 8,000 images, each paired with five diverse captions offering clear descriptions of prominent entities and events. These images were meticulously selected from six different Flickr groups, deliberately avoiding well-known people or locations. Instead, they depict a wide array of scenes and situations.

## Model Architecture
- The chosen architecture for this project is an Encoder-Decoder model.
- The Encoder network functions as a feature extractor, leveraging a pretrained image model backbone (EfficientNetV2B3 was utilized, although any similar model would suffice).
- Meanwhile, the Decoder network comprises one or more RNN layers (such as GRU or LSTM).
- The final step involves combining the outputs of both networks to generate probabilities for the next token in the caption.

## Inference Methods
There are two algorithms supported for caption generation:

### Greedy Decoding with Temperature Adjustment
This approach involves the model greedily selecting the most probable word at each time step, with the softmax output scaled by a temperature parameter. Adjusting this temperature allows for controlling the randomness of word selection during generation. Lower temperatures (e.g., 0.1) produce more focused and deterministic text, while higher temperatures (e.g., 1.0) yield more random and diverse outputs.

### Beam Search with Beam Width Specification
Beam search is a search algorithm that concurrently explores multiple possible sequences. The beam width parameter determines the number of sequences the model considers at each step. A higher beam width can result in more diverse captions but increases computational complexity.

<br>
<br>

# Screenshots
![www](https://github.com/enesylmzx42/RNN-ImageCaption/assets/117593621/8a8fd106-6c0a-4f15-b6c6-a9138c32805a)
<br>

![Screenshot_2](https://github.com/enesylmzx42/RNN-ImageCaption/assets/117593621/d368ef36-622b-4cb9-9118-20e9b8b69669)






