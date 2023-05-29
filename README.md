import random

# Define the possible user inputs and corresponding bot responses
responses = {
    "hello": "Hello! How can I assist you today?",
    "how are you?": "I'm good, thank you. How about you?",
    "what's your name?": "My name is ChatBot.",
    "default": "I'm sorry, but I don't understand. Can you please rephrase?"
}

# Function to generate bot response based on user input
def generate_response(user_input):
    # Convert the user input to lowercase for case-insensitive matching
    user_input = user_input.lower()
    
    # Check if the user input matches any predefined responses
    for key in responses:
        if user_input in key:
            return responses[key]
    
    # If no matching response is found, return the default response
    return responses["default"]

# Main loop for user interaction
while True:
    user_input = input("User: ")
    bot_response = generate_response(user_input)
    print("Bot: " + bot_response)
