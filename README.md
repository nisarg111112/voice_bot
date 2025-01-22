# Multilingual Voice Assistant (Test Version)

This is a test version of a voice assistant application that supports multiple languages (English, Hindi, and Marathi). Please follow the setup instructions carefully before testing.

## Prerequisites

- Python 3.8 or higher
- Working microphone
- Working speakers/audio output
- Internet connection
- Required API keys (see Setup section)

## Setup Instructions

1. **Extract the Files**
   - Extract the zip file to your preferred location
   - Maintain the original file structure

2. **Install Dependencies**
   pip install -r requirements.txt

3. **API Keys Setup**
   - Open `config.py`
   - Replace the following placeholder API keys with your own:
     ```python
     OPENCAGE_API_KEY = "your_opencage_api_key"
     GOOGLE_API_KEY = "your_google_api_key"
     GOOGLE_CX = "your_google_cx"
     ```
   
   To obtain API keys:
   - OpenCage API: Register at https://opencagedata.com/
   - Google API & CX: Set up at https://console.cloud.google.com/
     - Enable Custom Search API
     - Create credentials
     - Set up Custom Search Engine to get CX

## File Structure
```
voice-assistant/
├── config.py           # Configuration and API keys
├── google_search.py    # Google search functionality
├── main.py            # Main application entry point
├── maps.py            # Maps and location services
├── music_player.py    # Music playback functionality
├── reminder.py        # Reminder functionality
├── speech.py          # Speech recognition and synthesis
├── utils.py           # Utility functions
├── weather.py         # Weather information services
├── requirements.txt   # Package dependencies
└── README.md          # This file
```

## Running the Application

1. Navigate to the project directory:
   cd voice-assistant

2. Run the main script:
   python main.py

3. Select your preferred language when prompted:
   - Say "English" for English
   - Say "Hindi" for Hindi
   - Say "Marathi" for Marathi

## Testing Features

### 1. Location Services
- Test Command: "show map" or "find location"
- Expected: Should ask for location and open in browser
- Test with various city names

### 2. Weather Information
- Test Command: "weather" or "temperature"
- Expected: Should ask for city name and provide weather details
- Test with different cities

### 3. Web Search
- Test Command: "question" or "search"
- Expected: Should ask for query and provide search results
- Test with various types of questions

### 4. YouTube Search
- Test Command: "open youtube" or "youtube"
- Expected: Should open YouTube in browser with search results
- Test with different search terms

### 5. Wikipedia Search
- Test Command: "wikipedia" or "search wikipedia"
- Expected: Should open Wikipedia page in browser
- Test with various topics

### 6. Camera
- Test Command: "open camera" or "camera"
- Expected: Should open camera feed
- Press 'q' to close camera window

## Language Support

### English Commands
- Weather: "what's the weather", "temperature"
- Maps: "show map", "find location"
- Search: "question", "search"
- YouTube: "open youtube", "youtube"
- Camera: "open camera", "camera"
- Exit: "exit", "stop"

### Hindi Commands
- Weather: "मौसम", "तापमान"
- Maps: "नक्शा दिखाओ", "location बताओ"
- Search: "सवाल", "search karo"
- YouTube: "youtube खोलो", "यूट्यूब"
- Camera: "कैमरा खोलो", "camera"
- Exit: "बंद करो", "exit"

### Marathi Commands
- Weather: "हवामान", "तापमान"
- Maps: "नकाशा दाखवा", "location शोधा"
- Search: "प्रश्न", "शोध"
- YouTube: "youtube उघडा", "यूट्यूब"
- Camera: "कॅमेरा उघडा", "camera"
- Exit: "बंद करा", "थांबा"

## Known Issues
1. Speech recognition might need multiple attempts in noisy environments
2. Some APIs might have rate limits with free tier keys
3. Camera function requires 'q' key to close (cannot be closed by voice)

## Troubleshooting

1. **No Sound Output**
   - Check speaker connections
   - Verify pygame is installed correctly
   - Check system sound settings

2. **Microphone Issues**
   - Ensure microphone is connected and selected as default input device
   - Check microphone permissions in system settings

3. **API Errors**
   - Verify all API keys are correctly entered in config.py
   - Check internet connection
   - Ensure API services are active and within usage limits

## Testing Notes

- Test each feature in all three languages
- Try variations of commands (both listed and similar phrases)
- Test with different noise levels
- Test with various accents and speaking speeds
- Document any unexpected behavior or errors

## Feedback and Issues

While testing, please note:
- Any crashes or error messages
- Features that don't work as expected
- Language recognition accuracy
- Command recognition accuracy
- Response time and accuracy
- Any suggestions for improvement

Please include the following in your feedback:
1. Operating System and version
2. Python version
3. Steps to reproduce any issues
4. Error messages (if any)
5. Expected vs actual behavior
