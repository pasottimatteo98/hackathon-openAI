# Hackathon-openAI

- Hackathon link: https://lablab.ai/event/openai-hackathon
- Team Link: https://lablab.ai/event/openai-hackathon/milanesiimbruttiti

# Teacher AI

A Streamlit application that generates elementary school lessons using OpenAI's GPT model and provides vocal explanations through text-to-speech.

![Demo GIF](https://media.giphy.com/media/YT8NIA8fU2pz6Gf2kR/giphy.gif)

## Description

Teacher AI is an application that supports teachers in preparing lessons for elementary school. The application generates educational explanations on various topics using OpenAI's Davinci model (GPT-3) and plays them vocally for a more engaging learning experience.

Currently supports three subjects:
- English
- Math
- Science

## Installation

### Prerequisites

- Python 3.7+
- An OpenAI API key

### Installation Procedure

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/teacher-ai.git
   cd teacher-ai
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Install system dependencies:
   ```bash
   apt-get install libespeak1   # For Debian/Ubuntu systems
   ```

4. Configure the OpenAI API key:
   - Create a `.env` file in the main directory
   - Add your API key in the format:
     ```
     openai_key = "your-openai-api-key"
     ```

## Usage

1. Start the Streamlit application:
   ```bash
   cd App
   python run.py
   ```
   or directly with Streamlit:
   ```bash
   cd App
   streamlit run app.py
   ```

2. Access the web interface at the address indicated in the terminal (usually http://localhost:8501)

3. Select the desired subject from the dropdown menu

4. The application will display the weekly curriculum and generate an explanation for each topic, as well as play audio of the explanation

## Project Structure

```
.
├── App
│   ├── app.py                    # Main Streamlit application
│   ├── openai_utils
│   │   └── openaiAPI.py          # Wrapper for OpenAI API
│   ├── read.py                   # Text-to-speech functionality
│   └── run.py                    # Startup script
├── Example
│   ├── artsyllabus.txt           # Art curriculum (not implemented)
│   ├── englishsyllabus.txt       # English curriculum
│   ├── lesson_examplesyllabus.txt # Example lesson format
│   ├── mathsyllabus.txt          # Math curriculum
│   └── sciencesyllabus.txt       # Science curriculum
├── .env                          # Environment variables file (to be created)
├── .gitignore                    # Git configuration file
├── .streamlit
│   └── config.toml               # Streamlit theme configuration
├── LICENSE                       # MIT License
├── packages.txt                  # Required system packages
├── README.md                     # This file
└── requirements.txt              # Python dependencies
```

## Technologies Used

- [Streamlit](https://streamlit.io/) - Framework for creating web apps with Python
- [OpenAI API](https://beta.openai.com/) - API for accessing GPT models
- [pyttsx3](https://pypi.org/project/pyttsx3/) - Text-to-speech library for Python
- [python-dotenv](https://pypi.org/project/python-dotenv/) - Environment variable management

## Contributing

Contributions are welcome! Please open an issue or a pull request.


## Hackathon

This project was developed during the [OpenAI Hackathon](https://lablab.ai/event/openai-hackathon) by the [MilanesiImbruttiti](https://lablab.ai/event/openai-hackathon/milanesiimbruttiti) team.
