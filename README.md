# AI-Powered-Therapy-Bot-Using-OpenAI-GPT

## Overview

The **Mental Health Chatbot** is an empathetic virtual therapist designed to provide a safe space for individuals to express their feelings. It uses sentiment analysis and advanced conversational AI to provide a supportive and understanding environment. This chatbot is deployed using [Gradio](https://gradio.app/), making it accessible and easy to use.

## Features

- **Empathetic Responses**: Provides personalized, empathetic, and reflective responses.
- **Sentiment Analysis**: Analyzes the sentiment of the user's input (positive, neutral, negative) to tailor responses.
- **Crisis Detection**: Detects crisis-related keywords and prompts users to seek immediate professional help.
- **Interactive Interface**: Powered by Gradio, offering a clean, interactive chat experience.
- **Real-Time Processing**: Integrates with OpenAI's GPT-4 model for dynamic and human-like conversations.

## Demo

### Screenshot 1
![Mental Health Chatbot Interface](https://i.imgur.com/EJ0SXWh.png)

### Screenshot 2
![Chat History](https://i.imgur.com/ZroC2jo.png)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/mental-health-chatbot.git
    cd mental-health-chatbot
    ```

2. Install required dependencies:
    ```bash
    pip install openai==0.28
    pip install textblob
    pip install gradio
    ```

3. Set up your OpenAI API key:
    - Replace `"API KEY"` in the code with your actual OpenAI API key.

## How to Run

1. Open the `mental_health_chatbot.ipynb` file in Google Colab or Jupyter Notebook.

2. Run the cells to set up the chatbot.

3. Launch the Gradio interface:
    ```python
    interface.launch(share=True)
    ```

4. Use the provided link to interact with the chatbot.

## How It Works

1. **Sentiment Analysis**:
    - Sentiment of the user's input is analyzed using `TextBlob`.
    - Categories: Positive, Neutral, Negative.

2. **Crisis Detection**:
    - Scans for keywords like "suicide", "kill myself", and others.
    - Provides a warning message encouraging the user to seek help.

3. **ChatGPT Integration**:
    - Uses OpenAI's GPT-4 to generate empathetic and dynamic responses.
    - Responses are adjusted based on the detected sentiment.

4. **Interactive Chat**:
    - Maintains a chat history to provide context-aware responses.
    - User-friendly interface with Gradio.

## Code Overview

### Key Functions

- **`analyze_sentiment(text)`**:
  Analyzes sentiment using `TextBlob` and categorizes input as positive, neutral, or negative.

- **`detect_crisis(input_text)`**:
  Detects crisis-related keywords to provide immediate warnings.

- **`chat_with_gpt(prompt)`**:
  Sends user input to OpenAI's GPT-4 model and retrieves responses.

- **`chatbot_response(user_input, history)`**:
  Maintains chat history and generates a response using both sentiment analysis and GPT.

### Gradio Interface

The chatbot is deployed using the Gradio interface:
- **Inputs**: Text input from the user, chat history.
- **Outputs**: Chat history displayed interactively.

## Customization

- **Add More Crisis Keywords**:
  Edit the `crisis_keywords` list in the `detect_crisis()` function to include additional phrases.
  
- **Adjust Sentiment Sensitivity**:
  Modify the thresholds in the `analyze_sentiment()` function.

- **Change Model Parameters**:
  Adjust `temperature`, `max_tokens`, and other parameters in the `chat_with_gpt()` function for different response styles.

## Limitations

- This chatbot is **not a substitute for professional therapy**. It is designed to offer support and encourage seeking professional help when needed.

- While the chatbot detects crisis-related keywords, it cannot provide emergency assistance. Always reach out to emergency services or crisis hotlines in critical situations.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for new features, bug fixes, or improvements.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- [OpenAI](https://openai.com) for the powerful GPT model.
- [TextBlob](https://textblob.readthedocs.io/) for sentiment analysis.
- [Gradio](https://gradio.app/) for the interactive interface.
