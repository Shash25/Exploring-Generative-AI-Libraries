Objectives
After completing this lab, you will be able to:

Gain an understanding of generative AI and its impact across various domains.
Familiarize yourself with different types of models in generative AI.
Acquire the skills to build and interact with a chatbot using transformers.
What is generative AI?
Imagine presenting a computer with a vast array of paintings. After analyzing them, it tries to craft a unique painting of its own. This capability is termed generative AI. Essentially, the computer derives inspiration from the provided content and uses it to create something new.

Real-world impact of generative AI
Generative AI is transforming multiple industries. Its applications span:

1. Art and creativity
Generative art: Artists employing generative AI algorithms can create stunning artworks by learning from existing masterpieces and producing unique pieces inspired by them. These AI-generated artworks have gained recognition in the art world.
Music Composition: Projects in the realm of generative AI have been employed to compose music. They learn from a vast data set of musical compositions and can generate original pieces in various styles, from classical to jazz, revolutionizing the music industry.
2. Natural language processing (NLP)
Content generation: Tools like generative pre-trained transformer (GPT) have demonstrated their ability to generate coherent and context-aware text. They can assist content creators by generating articles, stories, or marketing copy, making them valuable tools in content creation.
Chatbots and virtual assistants: Generative AI powers many of today's chatbots and virtual assistants. These AI-driven conversational agents understand and generate human-like responses, enhancing user experiences.
Code Writing: Generative AI models can also produce code snippets based on descriptions or requirements, streamlining software development.
3. Computer vision
Image synthesis: Models like data analysis learning with language model for generation and exploration, frequencly known as DALL-E, can generate images from textual descriptions. This technology finds applications in graphic design, advertising, and creating visual content for marketing.
Deepfake detection: With the advancement in generative AI techniques, the generation of deep fake content is also on the rise. Consequently, generative AI now plays a role in developing tools and techniques to detect and combat the spread of misinformation through manipulated videos.
4. Virtual avatars
Entertainment: Generative AI is utilized to craft virtual avatars for gaming and entertainment. These avatars mimic human expressions and emotions, bolstering user engagement in virtual environments.
Marketing: Virtual influencers, propelled by generative AI, are on the rise in digital marketing. Brands are harnessing these virtual personas to endorse their products and services.
Neural structures behind generative AI
Before we had the powerful transformers, which are like super-fast readers and understand lots of words at once, there were other methods used for making computers generate text. These methods were like the building blocks that led to the amazing capabilities we have today.

Large language models (LLMs)
Large language models are like supercharged brains. They are massive computer programs with lots of "neurons" that learn from huge amounts of text. These models are trained to do tasks like understanding and generating text, and they're used in many applications. However, there's a limitation: these models are not very good at understanding the bigger context or the meaning of words. They work well for simple predictions but struggle with more complex text.

Text generation before transformers
1. N-gram language models
N-gram models are like language detectives. They predict what words come next in a sentence based on the words that came before. For example, if you say "The sky is," these models guess that the next word might be "blue."

2. Recurrent neural networks (RNN)
Recurrent neural networks (RNNs) are specially designed to handle sequential data, making them a powerful tool for applications like language modeling and time series forecasting. The essence of their design lies in maintaining a 'memory' or 'hidden state' throughout the sequence by employing loops. This enables RNNs to recognize and capture the temporal dependencies inherent in sequential data.

Hidden state: Often referred to as the network's 'memory', the hidden state is a dynamic storage of information about previous sequence inputs. With each new input, this hidden state is updated, factoring in both the new input and its previous value.
Temporal dependency: Loops in RNNs enable information transfer across sequence steps.
Image
Image Source
Illustration of RNN's operation: Consider a simple sequence, such as the sentence: "I love RNNs". The RNN interprets this sentence word by word. Beginning with the word "I", the RNN ingests it, generates an output, and updates its hidden state. Moving on to "love", the RNN processes it alongside the updated hidden state which already holds insights about the word "I". The hidden state is updated again post this. This pattern of processing and updating continues until the last word. By the end of the sequence, the hidden state ideally encapsulates insights from the entire sentence.

3. Long short-term memory (LSTM) and gated recurrent units (GRUs)
Long short-term memory (LSTM) and gated recurrent units (GRUs) are advanced variations of recurrent neural networks (RNNs), designed to address the limitations of traditional RNNs and enhance their ability to model sequential data effectively. They processed sequences one element at a time and maintained an internal state to remember past elements. While they were effective for a variety of tasks, they struggled with long sequences and long-term dependencies.

4. Seq2seq models with attention
Sequence-to-sequence (seq2seq) models, often built with RNNs or LSTMs, were designed to handle tasks like translation where an input sequence is transformed into an output sequence.
The attention mechanism was introduced to allow the model to "focus" on relevant parts of the input sequence when generating the output, significantly improving performance on tasks like machine translation.
While these methods provided significant advancements in text generation tasks, the introduction of transformers led to a paradigm shift. Transformers, with their self-attention mechanism, proved to be highly efficient at capturing contextual information across long sequences, setting new benchmarks in various NLP tasks.

Transformers
Proposed in a paper titled "Attention Is All You Need" by Vaswani et al. in 2017, the transformer architecture replaced sequential processing with parallel processing. The key component behind its success? The attention mechanism, more precisely, self-attention.

Key steps include:

Tokenization: The first step is breaking down a sentence into tokens (words or subwords).
Embedding: Each token is represented as a vector, capturing its meaning.
Self-attention: The model computes scores determining the importance of every other word for a particular word in the sequence. These scores are used to weight the input tokens and produce a new representation of the sequence. For instance, in the sentence "He gave her a gift because she'd helped him", understanding who "her" refers to requires the model to pay attention to other words in the sentence. The transformer does this for every word, considering the entire context, which is particularly powerful for understanding meaning.
Feed-forward neural networks: After attention, each position is passed through a feed-forward network separately.
Output sequence: The model produces an output sequence, which can be used for various tasks, like classification, translation, or text generation.
Layering: Importantly, transformers are deep models with multiple layers of attention and feed-forward networks, allowing them to learn complex patterns.
The architecture's flexibility has allowed transformers to be used beyond NLP, finding applications in image and video processing too. In NLP, transformer-based models like BERT, GPT, and their variants have set state-of-the-art results in various tasks, from text classification to translation.
