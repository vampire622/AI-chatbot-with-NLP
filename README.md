import nltk
import random
import string
from nltk.chat.util import Chat, reflections

# Sample conversation pairs (pattern, response)
pairs = [
    [
        r"hi|hello|hey",
        ["Hello!", "Hi there!", "Hey! How can I help you?"]
    ],
    [
        r"what is your name ?",
        ["I am a CodTech AI Bot.", "You can call me CodBot."]
    ],
    [
        r"how are you ?",
        ["I'm good, thank you!", "Doing great! How can I assist you today?"]
    ],
    [
        r"what can you do ?",
        ["I can answer simple questions and have a friendly chat with you."]
    ],
    [
        r"who created you ?",
        ["I was created as a project by a CODTECH intern."]
    ],
    [
        r"(.*) your name ?",
        ["You can call me CodBot."]
    ],
    [
        r"quit|bye",
        ["Bye! Have a nice day.", "Goodbye!"]
    ]
]

# Create and run chatbot
def codtech_chatbot():
    print("Hi, I'm CodBot! Type 'bye' or 'quit' to exit.")
    chat = Chat(pairs, reflections)
    chat.converse()

# Run the chatbot
codtech_chatbot()
