# GPT-Based Smart Assistant

A simple Python application that listens to voice commands, processes them using OpenAI's GPT-4o model, and responds with both text and speech.

## Features

- **Voice input** via microphone using SpeechRecognition and PyAudio
- **Text-to-speech** output using `pyttsx3` and Windows SAPI5
- **ChatGPT backend** via OpenAI API (GPT-4o model)
- Browser control commands (open YouTube, Google, etc.)

## Prerequisites

- Python 3.13 or later
- Windows OS (application uses `sapi5` voice engine)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Bhanuprakash2580/GPT-Based-Smart-Assistant.git
   cd "GPT Based Smart Assistant"
   ```

2. (Optional) Create and activate a virtual environment:
   ```bash
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1  # PowerShell
   ```

3. Install required packages:
   ```bash
   python -m pip install -r requirements.txt
   ```

4. Provide your OpenAI API key:
   - Copy `apikey.example.py` to `apikey.py` and update the value, **or**
   - Set environment variable `OPENAI_API_KEY` and modify the code accordingly.

   ```python
   # apikey.py
   api_data = 'sk-your-api-key'
   ```

## Usage

Run the application:

```bash
python app.py
```

Speak commands into your microphone. The assistant will respond verbally and print text output. You can say things like "Open YouTube" or "Open Google", and it will launch your browser.

To exit, say "bye" or interrupt with `Ctrl+C`.

## Configuration

- Change `Model` variable in `app.py` to use a different OpenAI model.
- Customize speech engine settings or recognition language as needed.

## Security

- **Do not commit** `apikey.py` to source control. It is included in `.gitignore`.
- Use `apikey.example.py` as a template for collaborators.
- Rotate your API key if it ever gets exposed.

## License

This project is provided as-is under the MIT License.
