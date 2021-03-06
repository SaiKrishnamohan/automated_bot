# automated_bot

# Introduction

Question Answering (QA) is a field within natural language processing focused on designing systems that can answer questions. Among the more famous question answering systems is Watson, the IBM computer that competed (and won) on Jeopardy!. A question answering system of Watson’s accuracy requires enormous complexity and vast amounts of data, but in this problem, we’ll design a very simple question answering system based on inverse document frequency.

Our question answering system will perform two tasks: document retrieval and passage retrieval. Our system will have access to a corpus of text documents. When presented with a query (a question in English asked by the user), document retrieval will first identify which document(s) are most relevant to the query. Once the top documents are found, the top document(s) will be subdivided into passages (in this case, sentences) so that the most relevant passage to the question can be determined.

How do we find the most relevant documents and passages? To find the most relevant documents, we’ll use tf-idf to rank documents based both on term frequency for words in the query as well as inverse document frequency for words in the query. Once we’ve found the most relevant documents, there many possible metrics for scoring passages, but we’ll use a combination of inverse document frequency and a query term density measure (described in the Specification).

# Setting up

1. Clone Repository.
2. Create a virtualev and activate it.
3. Install all the modules in reqiurements.txt using "pip3 install -r requirements.txt".
4. Run the program:
                  "python3 questions.py corpus"
5. Now ask the bot any related questions on "Machine Learning, Artificial Intelligence, Neural Network, Probabiltity, NLP, Python".
6. Examples:

            $ python3 questions.py corpus
            Query: What are the types of supervised learning?
            Types of supervised learning algorithms include Active learning , classification and regression.
            
            $ python3 questions.py corpus
            Query: When was Python 3.0 released?
            Python 3.0 was released on 3 December 2008.
            
            $ python3 questions.py corpus
            Query: How do neurons connect in a neural network?
            Neurons of one layer connect only to neurons of the immediately preceding and immediately following layers.
            
