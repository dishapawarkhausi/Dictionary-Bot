# Dictionary Bot

A comprehensive dictionary application that provides word definitions, translations, pronunciations, and more in multiple languages.

## Features

- **Word Definitions**: Get detailed definitions with part of speech categorization
- **Translations**: Translate words between multiple languages
- **Pronunciation**: Listen to the pronunciation of words and their translations
- **Speech Recognition**: Search for words using your voice
- **Multiple Language Support**: Support for English and many other languages including Hindi, Spanish, French, etc.
- **Content Filtering**: Ensures all definitions are appropriate and educational

## Supported Languages

- English
- Spanish
- French
- German
- Italian
- Portuguese
- Russian
- Japanese
- Korean
- Chinese (Simplified)
- Hindi
- Bengali
- Telugu
- Tamil
- Marathi
- Gujarati
- Kannada
- Malayalam
- Punjabi
- Urdu

## Setup Instructions

### Prerequisites

- Python 3.6 or higher
- Flask
- Internet connection for API access

### Installation (Local)

1. Clone the repository:
   ```bash
   git clone https://github.com/dishapawarkhausi/dictionary-bot.git
   cd dictionary-bot
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   python app.py
   ```

4. Open your browser and navigate to:
   ```
   http://localhost:5000
   ```

## Deployment on Render

### Steps to Deploy

1. Push your project to a GitHub repository.
2. Go to [Render](https://render.com/) and log in.
3. Click on "New Web Service."
4. Connect your GitHub repository.
5. Select the branch you want to deploy.
6. In the **Build Command**, enter:
   ```bash
   pip install -r requirements.txt
   ```
7. In the **Start Command**, enter:
   ```bash
   gunicorn app:app
   ```
8. Set the **Environment Variables** (if required, e.g., API keys).
9. Click "Deploy" and wait for Render to build and deploy your project.

### Accessing the Application

Once deployed, you will get a public URL from Render, such as:
```
https://dictionary-bot.onrender.com
```

## Usage

1. **Search for a Word**:
   - Type a word in the search box
   - Select the target language from the dropdown
   - Click the search button or press Enter

2. **Listen to Pronunciation**:
   - Click the "Listen to Original" button to hear the original word
   - Click the speaker icon next to the translation to hear the translated word

3. **Voice Search**:
   - Click the microphone icon
   - Speak the word you want to search for
   - The application will automatically search for the word

4. **View Different Information**:
   - Use the tabs to switch between Definitions, Examples, Synonyms, and Antonyms

## API Integration

The Dictionary Bot uses multiple APIs to provide comprehensive information:

1. **Free Dictionary API**: Primary source for English definitions
2. **WordsAPI** (optional): Additional source for English definitions (requires API key)
3. **Urban Dictionary API**: Fallback source for slang terms (with content filtering)
4. **Google Translate API**: For translations between languages
5. **gTTS (Google Text-to-Speech)**: For pronunciation

## Content Filtering

The application uses the `better_profanity` library to ensure all definitions and examples are appropriate and educational. This filtering system:

- Removes definitions containing profanity or inappropriate content
- Ensures examples are suitable for all users
- Prioritizes formal, educational definitions over slang

## Project Structure

```
dictionary-bot/
├── app.py                 # Main Flask application
├── requirements.txt       # Python dependencies
├── frontend/              # Frontend files
│   ├── index.html         # Main HTML file
│   ├── styles.css         # CSS styles
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Free Dictionary API
- Google Translate
- Urban Dictionary API
- WordsAPI
- better_profanity library for content filtering
