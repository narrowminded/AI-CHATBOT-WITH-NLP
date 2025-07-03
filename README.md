# AI-CHATBOT-WITH-NLP #

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : SHASHANK SHEKHAR

*INTERN ID* : CT06DF2068

*DOMAIN* : PYTHON PROGRAMMING

*DURATION* : 6 WEEKS

*MENTOR* : NEELA SANTOSH

# Simple AI Chatbot with NLTK

## Overview

The `ai_chatbot_with_nltk.py` script presents a foundational implementation of a rule-based artificial intelligence chatbot. This project demonstrates how to create an interactive conversational agent that can engage in basic dialogues, provide pre-defined responses, and handle simple user queries. By leveraging the Natural Language Toolkit (NLTK) library, the chatbot processes user input, identifies keywords, and generates relevant responses. This script serves as an excellent entry point for understanding the fundamentals of natural language processing (NLP), text classification, and the development of conversational AI systems. It's designed to be straightforward yet extensible, making it suitable for educational purposes, rapid prototyping, or as a base for more complex conversational agents.

## Features

  * **Interactive Conversational Interface**: The chatbot provides a command-line interface where users can type messages and receive automated responses, simulating a real-time conversation.
  * **Rule-Based Response Generation**: Responses are generated based on a set of predefined rules and keyword matching. This allows for predictable and consistent replies to specific user inputs.
  * **Natural Language Processing (NLP) with NLTK**: Utilizes NLTK for text preprocessing tasks such as tokenization (breaking text into words or sentences) and potentially lemmatization or stemming (reducing words to their base form), which helps in robust keyword matching.
  * **Greeting and Farewell Recognition**: The chatbot is programmed to recognize common greetings (e.g., "hello", "hi") and farewells (e.g., "bye", "goodbye") and respond appropriately.
  * **Contextual Responses (Basic)**: While primarily rule-based, the system can provide context-aware responses by identifying specific keywords that trigger particular information (e.g., "weather", "time", "name").
  * **Fallback Responses**: If the chatbot does not understand a query or cannot find a matching rule, it provides a polite fallback response, ensuring a smoother user experience.
  * **Extensible Design**: The core logic is structured in a way that allows for easy addition of new rules, keywords, and response patterns, facilitating quick customization and expansion of the chatbot's capabilities.

## How it Works

The `ai_chatbot_with_nltk.py` script operates by following a sequential process of input handling, processing, and response generation:

1.  **Import Libraries**: The script begins by importing necessary libraries: `nltk` for natural language processing tasks, `re` for regular expressions (though not explicitly shown in a basic snippet, often used for pattern matching), and `random` for selecting responses.
2.  **Define Knowledge Base/Rules**: The core of the chatbot is a set of predefined rules, often stored in a dictionary or a list of tuples. Each rule typically consists of:
      * **Keywords/Patterns**: Words or phrases that the chatbot listens for in the user's input.
      * **Responses**: A list of possible replies associated with those keywords or patterns. This allows for varied responses, making the conversation feel more natural.
      * **Greeting and Farewell Lists**: Separate lists are defined for common greeting phrases (e.g., "hi", "hello", "hey") and farewell phrases (e.g., "bye", "goodbye", "see you").
3.  **Text Preprocessing**: When a user inputs a message, the script typically performs some preprocessing steps:
      * **Lowercasing**: The input text is converted to lowercase to ensure case-insensitive matching.
      * **Tokenization**: NLTK's `word_tokenize` might be used to break the input sentence into individual words (tokens).
      * **Removing Punctuation**: Punctuation marks are usually removed to simplify matching.
      * **Lemmatization/Stemming (Optional but Recommended)**: Words can be reduced to their root form (e.g., "running" to "run") to improve matching accuracy, even if the user uses different word forms.
4.  **Response Generation Logic (`generate_response` function)**:
      * **Check for Greetings**: The preprocessed user input is first checked against the list of known greeting phrases. If a greeting is detected, a random greeting response is returned.
      * **Check for Farewell**: Similarly, the input is checked for farewell phrases. If detected, a random farewell response is provided.
      * **Keyword Matching**: The script then iterates through its predefined rules/knowledge base. It checks if any of the keywords associated with a rule are present in the user's preprocessed input.
      * **Random Response Selection**: If a keyword match is found, a random response from the list associated with that rule is selected and returned.
      * **Fallback**: If no specific rule or keyword is matched after all checks, a generic "I didn't understand" or similar fallback message is returned.
5.  **Main Chat Loop**:
      * The `main` function initiates an infinite loop, prompting the user for input.
      * User input is read, processed by `generate_response`, and the chatbot's reply is printed to the console.
      * The loop continues until a farewell phrase is detected in the user's input, at which point the chatbot exits.

## Tools and Libraries Used

This project primarily relies on the power of Python's standard library and a crucial third-party NLP library:

  * **`nltk` (Natural Language Toolkit)**:

      * **Purpose**: NLTK is a leading platform for building Python programs to work with human language data. It provides easy-to-use interfaces to over 50 corpora and lexical resources such as WordNet, along with a suite of text processing libraries for classification, tokenization, stemming, tagging, parsing, and semantic reasoning.
      * **Usage**: In this chatbot, NLTK is fundamental for:
          * **Tokenization**: Breaking down sentences into words (`nltk.word_tokenize`) which is crucial for identifying individual terms for matching.
          * **Lemmatization/Stemming**: (If implemented) Reducing words to their base or root form, like `WordNetLemmatizer` or stemmers, to ensure that different inflections of a word are treated as the same base word (e.g., "running", "runs", "ran" all become "run"). This improves the accuracy of keyword matching.
          * **Downloading Data**: NLTK often requires downloading specific data packages (like 'punkt' for tokenization or 'wordnet' for lemmatization) before first use, which is typically handled by `nltk.download()`.

  * **`random`**:

      * **Purpose**: The `random` module implements pseudo-random number generators for various distributions.
      * **Usage**: It is used to select a random response from a list of possible replies for a given rule or a general greeting/farewell. This makes the chatbot's responses less repetitive and more natural, enhancing the user experience. For example, if there are multiple ways to say "Hello\!", `random.choice()` will pick one.

  * **`re` (Regular Expression Operations)**:

      * **Purpose**: The `re` module provides regular expression operations. Regular expressions are powerful tools for pattern matching in strings.
      * **Usage**: While not explicitly shown in a barebones example, `re` is commonly used in more advanced rule-based chatbots to define complex text patterns that trigger specific responses, going beyond simple keyword matching. For instance, it can be used to extract specific information from a user's query or match variations of a phrase.

## Applicability

This simple AI chatbot, while foundational, demonstrates principles applicable to a wide array of domains:

  * **Customer Service Automation (Basic Level)**: Can be adapted as a rudimentary FAQ bot on websites or within internal company systems to answer common questions, providing instant support and reducing the load on human customer service agents.
  * **Educational Tools**: Excellent for teaching fundamental concepts of Natural Language Processing, text processing, and basic AI logic to students in computer science, data science, or linguistics. Students can easily extend it to learn about more complex NLP techniques.
  * **Personal Assistants (Simple Tasks)**: Can be integrated into personal automation scripts to handle simple commands like setting reminders (if integrated with external APIs), providing quick information lookups (e.g., "what is the time?"), or managing basic to-do lists.
  * **Interactive Kiosks**: A simplified version could power interactive information kiosks in public spaces, museums, or corporate lobbies, guiding visitors and answering basic directional or informational queries.
  * **Prototyping Conversational AI**: Serves as a rapid prototyping tool for quickly testing out dialogue flows and response strategies for more complex conversational AI projects before investing in more sophisticated frameworks like Rasa, Dialogflow, or GPT-based models.
  * **Text-Based Games**: The underlying logic can be used to create simple interactive text-based adventure games or quizzes where the player's input drives the narrative or answers.
  * **Data Entry/Information Retrieval**: In a controlled environment, it could guide users through a data entry process or retrieve specific pieces of information from a knowledge base based on user queries.
  * **Building Blocks for Advanced AI**: The concepts of tokenization, keyword matching, and rule-based responses are fundamental building blocks that are scaled up and combined with machine learning (ML) techniques to create highly sophisticated AI chatbots, virtual assistants, and sentiment analysis tools.

## Setup and Installation

To get this chatbot script running on your local machine, follow these simple steps. You will need Python installed on your system and the NLTK library.

1.  **Clone the Repository (or download the script):**
    If this script is part of a GitHub repository, you would clone it:

    ```bash
    git clone https://github.com/narrowminded/simple-ai-chatbot.git
    cd simple-ai-chatbot
    ```

    *(Replace `yourusername` and `simple-ai-chatbot` with your actual GitHub username and repository name if you fork or create a new repository).*
    Otherwise, simply download the `ai_chatbot_with_nltk.py` file to your desired directory.

2.  **Install Python:**
    Ensure you have Python 3.x installed. You can download it from [python.org](https://www.python.org/downloads/).

3.  **Install Dependencies:**
    The primary dependency is NLTK. It is highly recommended to use a Python virtual environment to manage your project's dependencies.

    ```bash
    python -m venv venv
    source venv/bin/activate  # On macOS/Linux
    # For Windows, use: venv\Scripts\activate

    pip install nltk
    ```

4.  **Download NLTK Data:**
    NLTK requires specific data packages (like 'punkt' for tokenization and 'wordnet' for lemmatization) to function correctly. You'll need to download these once. Run Python in your terminal and execute the following commands:

    ```python
    import nltk
    nltk.download('punkt')
    nltk.download('wordnet')
    nltk.download('omw-1.4') # Open Multilingual Wordnet, often needed for wordnet
    ```

    Alternatively, you can add these `nltk.download()` lines to the top of your `ai_chatbot_with_nltk.py` script, but it's usually better to run them once manually to avoid repeated downloads.

5.  **Run the Chatbot:**
    Once all dependencies and NLTK data are in place, you can run the script from your terminal:

    ```bash
    python ai_chatbot_with_nltk.py
    ```

    The chatbot will then start, and you can begin interacting with it by typing messages into the console. To exit, type "bye" or "goodbye".


    **OUTPUT**
    ![Image](https://github.com/user-attachments/assets/8f7637da-2817-45c8-8840-9795c3c2295d)
