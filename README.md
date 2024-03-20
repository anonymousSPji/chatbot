# Google GenerativeAI Chatbot README

This project utilizes the Google GenerativeAI library to create a chatbot powered by advanced AI models. The chatbot engages in conversations based on the input provided by the user.

## Introduction

The Google GenerativeAI Chatbot leverages cutting-edge AI models to generate human-like responses in conversations. It utilizes a combination of temperature, top-p, and top-k parameters to control the diversity and quality of generated responses. Additionally, safety settings are implemented to ensure that generated content adheres to predefined guidelines regarding harmful or inappropriate content.

## Features

- Engages in conversations with users based on provided prompts.
- Controls the diversity and quality of generated responses using configurable parameters.
- Implements safety settings to block harmful or inappropriate content.

## Requirements

- Python 3.x
- Google GenerativeAI library
- API key for accessing the GenerativeAI service

## Setup

1. Install the Google GenerativeAI library:

    ```
    pip install google-generativeai
    ```

2. Obtain an API key from Google Cloud Platform for accessing the GenerativeAI service.

3. Configure the API key:

    ```python
    import google.generativeai as genai
    
    genai.configure(api_key="YOUR_API_KEY")
    ```

## Usage

1. Create an instance of the GenerativeModel with desired configuration:

    ```python
    model = genai.GenerativeModel(model_name="gemini-1.0-pro",
                                  generation_config=generation_config,
                                  safety_settings=safety_settings)
    ```

2. Start a conversation:

    ```python
    convo = model.start_chat(history=[])
    ```

3. Enter your prompt when prompted:

    ```python
    user_input = input("Enter your prompt: ")
    convo.send_message(user_input)
    ```

4. View the generated response:

    ```python
    print(convo.last.text)
    ```

## Contributing

Contributions are welcome! If you encounter any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
