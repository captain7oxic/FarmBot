# FarmBot

Introduction 



In India , agriculture is the major sector which contributes to 17-18% of country's GDP , and employes around 50% of Indian work force.
Agriculture, with its allied sectors, is the largest source of livelihoods in India. 70 percent of its rural households still depend primarily on agriculture for their livelihood, with 82 percent of farmers being small and marginal [FAO],and are not aware of better production practices and modern agricultural trends. Rural and remote areas do not have access to information and a lot of money and effort is spent on gathering knowledge and contacting experts or officials . Also it is observed that people in these areas and those who practice agriculture are often slow in adapting to new technology. This lack of resources results in lower yields , increased wastage of valuable manpower and market ineffieciencies. This could have been solved when they had an reliable source of information ,which can help in taking better agricultural decisions. Agricultural sector has shown growth in recent years.The rural telephone subscription has increased to 525.82 million by May-2020 [TRAI].However ,for the first time we see that with close to 227 Milion internet users in rural India, which is approximately 10% more than those in urban [IAMAI]. Which provides a good ground to spread agricultural related information through smartphones.



Technology used

Python will be used all over the course of project from deployement to development.

Rasa is an open source machine learning Framework, for automated text and voice based conversations.
Understand messages , hold conversations and connect to messaging channels and API. Being open source there is no third party involved , and we can build and host rasa Rasa internally in our server with complete control over it.The LSTM neural network which Rasa Core uses for action prediction can be easily exchanged for any other type of Neural Network.

Rasa comes with 2 components

Rasa NLU - a library for natural language understanding (NLU), which does the classification of intent and extractthe entity from user input and helps bot understand what user is saying.

Rasa core  -  a chatbot framework with machine learing dialoguemanagement takes the structured input from the NLU and predicts the next best best action using a probablistic model like LSTM neural network.

Twilio - With the help of twilio we can easily integrate our chatbot with Whatsapp business API. this way we can start connecting with existing users .

Bot Father can be used to integrate the bot with telegram messaging app.


All chatbots, regardless of source and nature, work on similar principles. They all work on Natural Language Understanding. Then once they understand what the users means, they go ahead and act on it depending on how they are made and what they are made to do. The crux of their working falls on intent <link> and entity <link> extraction. So, what are intents? Simply put, intents are the intentions of the end-user, these intentions or intents are conveyed by the user to your bot. Understanding which intention user had, is equivalent to understanding what is asked and that is the whole business of the product. 

Intents are classified in two categories 

Casual Intents 

Meaningful Intents 

They are: 

Casual Intents: These are the intents that are used to generate “small talk”. These intents are the opener or closer of a conversation. The Greetings like “hi” and “hello” are the opening or closing statements in a conversation. These intents should direct your bot to respond with a small talj reply like “Hello, what can I do for you today?” or” Bye, Thanks for talking!”. The casual intents also comprise of Affirmative and Negative intents for utterances like “Ok” and “yes please”. Having General affirmative and negative intents help you handle all the information in a confirmedly satisfied manner. 

Meaningful Intents: These are the intents that directly, map to the purpose of that bot. They tell you which if the actual functions your bot exists for, are needed by the user. The meaningful intents of your bot are more important because the small talk is the same for most bots, the differentiating factor is these intents. They define what your bit is actually doing.  

 

LUIS, short for Language Understanding is a bot making service and framework designed by Microsoft. It is a cloud-based service that applies custom machine-learning to a user’s conversational, natural language text to predict overall meaning, and pull-out relevant, detailed information. A LUIS app contains a domain-specific natural language model you design. Hence it was possible to use this for my project. What gave this tool a great advantage is that it can be used hand-in-hand with other great tools Microsoft provides likes the Bing Spell Check and Correction, Azure search, Bing Speech API, their Azure Bot Service, etc. The only issues faced here were that the code had to be in C#, and more importantly, it had to be hosted on a Microsoft Server and the data would be given to Microsoft, which was very much a deal broker. Not to mention the pricing issues that come along with it. 

 

The Rasa Stack 

The cool thing about Rasa is that every part of the stack is fully customizable and easily interchangeable. It is possible, and sometimes recommended to use Rasa Core or Rasa NLU separately. The LSTM (Long Short-Term Memory Networks) neural network which Rasa Core uses for action prediction can be easily exchanged for any other type of Neural Network.





General Description

The target audience of the product are farmers , gardeners , cattleman and environmental enthusiasts .

Product perspective -  The product is supposed to be easy to use and easily available to farmers who do not have a good knowledge base in technology.It is required to answer queries related to crops, plant diseases , better practices of production, weather related information, product reviews,  market prices and news related to agriculture . The bot will be able to hold and manage complex conversations , and answer complex questions better than traditional FAQ bots.

Functional Requirements - 

Users must be able to query the bot without knowledge of any technology used in production.


Non Functional requirement -
The bot can run on the messaging apps integrated with the bot i.e Whatsapp or telegram , be it any platform android or ios.
We can build a dedicated web application or mobile application,  where we can host the bot. 

Proposed solution - 

Our solution is Farm-Bot , a conversational AI or a AI enabled bot which will be able to provide better answers to daily agricultural queries of farmers. Our bot will be intelligent enough to answer questions with relevant text information and links , and unlike other bots will be able to hold complex conversations.Conversations are rarely just one question and one answer.This handling of contextual dialogues is done with deep learning instead of hand-crafted rules.It will be done with the halp of Rasa stack, which comprises of Rasa NLU and Rasa core.
Rasa as they define it is a ""Build great conversational AI in-house
 Open source machine learning tools for developers and product teams to expand bots
 beyond answering simple questions."[Rasa docs]
The other competent frameworks which are proprietary software ,have a lot of data sharing issues, as in you need to share your data with them. This is where Rasa comes in play. It is an open source Conversational AI framework. It doesn’t have any pre-built, ready-made and downloadable models on a server that you can integrate via an application programming interface. This gives us complete control over all the components in your chatbot. The way rasa works helps making complex , domain specific chatbots , with a knowledge base easier.

Rasa Stack - 

The interesting thing about Rasa is that every component of the stack is fully customizable and easily interchangeable, increasing utility. It is possible to use Rasa core and Rasa NLU separately, and do not depend on each other. When using Rasa NLU, you can choose among several backend NLP (Natural Language Processing) libraries. The LSTM neural network which Rasa Core uses for action prediction can be easily exchanged for any other type of Neural Network, if you know how to implement them in Keras.

Rasa Core -   A dialogue management solution tries to build a probability model which decides the set of actions to perform based on the previous set of user inputs.


Rasa NLU - A natural language understanding solution which takes the user input and tries to infer the intent and extract the available entities.


Domain - The domain specifies the field your bot excells in , i.e the type of knowledge base given to the bot to make it purpose specific .It can be a weather bot , a FAQ bot , A cab - booking bot , in our case it is an Agricultural FAQ bot . 
Domain also species the following -

1.Which of the intents you want your bot to make replies.
2.Which slots are to be kept in track .
3.The possible actions which a bot can take .

Slots - The part of conversations you wanna keep in track . That is a user is quering about "Rice" . The tracker has an attribute like tracker.get_slot(“Crop-Name”) which will return “Rice”


Actions -Actions are the things your bot can actually do. They are invoked by calling the action.run() method. For example, an action can:

1. Give responses to user.
2. Query a database . 
3. Make an API call .

Training Data Formats - 
Rasa Open Source uses YAML as a unified and extendable way to manage all training data, including NLU data, stories and rules.

Stories -
Stories are a type of training data used to train your assistant's dialogue management model. Stories can be used to train models that are able to generalize to unseen conversation paths.

NLU trainig Data - 
NLU training data consists of example user utterances categorized by intent. Training examples can also include entities. Entities are structured pieces of information that can be extracted from a user's message.

Rules - Rules are a type of training data used to train your assistant's dialogue management model. Rules describe short pieces of conversations that should always follow the same path.


all this data is fed to nueral nets , to be specific a type of Recurrent neural network called LSTM.

Recurrent Neural Networks (RNN) - Recurrent Neural Networks (RNNs) add an extra flavour to basic neural networks. A vanilla neural network takes in a fixed size input vector which limits its usage in situations that involve a ‘series’ type input with no predetermined size. Also the traditional feed forward neural networks meaning that data moves through them in only one direction. An individual node might be connected to several nodes in the layer beneath it, from which it receives data, and several nodes in the layer above it, to which it sends data.

Recurrent neural network remembers the past and it’s decisions are influenced by what it has learnt from the past user input and the training data. RNNs can take multiple input vectors and produce multiple output vectors and the output(s) are influenced not just by weights applied on inputs like a regular NN, but also by a “hidden” state vector representing the context based on prior input(s)/output(s). So, the same input could produce a different output depending on previous inputs in the series. 

LSTM - long -short term memory netowrks are a special kind of RNN , capable of learning order dependence in sequence prediction problems.
This is a behavior required in complex problem domains like machine translation, speech recognition, and more.

LSTMs are explicitly designed to avoid the long-term dependency problem. Remembering information for long periods of time is practically their default behavior, not something they struggle to learn.
The LSTM does have the ability to remove or add information to the cell state, carefully regulated by structures called gates.


 


 
 
