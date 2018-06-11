# Fresh

## Question 1
A chatbot is typically design as a smart model which receives input from a user (the user's messages or any other kind of input), and returns a response.

To make the smart model more life-like, a context is added to each message which provides the chatbot with information about the current conversation.

To complete the design of a chatbot, a database of responses is almost always needed. The database can be a static database, but it can also be a live-updated database.

## Question 2
Wen a user click on the "Next" button, a webhook linked to the Messenger API sends a request to the chatbot server asking for the response to give.

The request contains the last user's input, but may also contain the context of the conversation and other information.

## Question 3
I would build a recommendation system around news topics.

I would first put in place a simple NLP engine to extract topics from news stories. Then by extracting data from user interaction around news stories presented to them (likes, time spent on reading, asking for more...), I can do hierarchical clustering to group similar users in different clusters.

These two components (topic modeling, and clustering) will allow us to get topics for each cluster of users, and will make it easy for us to recommend news items to any new user.

## Question 4
As the Freshr database would need high availability on writes and read, but consistency isn't a *critical* feature, I would go for a NoSQL engine, like MongoDB.

Trading off a little bit of consistency for availability and partitioning (PAC Theorem) would seem like a good choice.

+ The kind of data we would store about users would be highly hierarchical (multiple nested objects) and would fit more as documents in mongodb than in a traditional RDBS like MariaDB or Postgres...

## Question 5
In order to run the notebook, you have to install jupyter, and then simply launch the file:
	
	jupyter notebook main.ipynb
