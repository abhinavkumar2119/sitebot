1. People contributed:
Abhinav Kumar [1DA21IS001]
P Bharath Kumar Reddy [1DA21IS034]

2. Python Libraries (from requirements.txt)
These are the core packages the project depends on:

Package	Purpose
Flask	Web framework for handling HTTP routes
Flask-SocketIO	Enables real-time bidirectional communication using WebSockets
requests	Handles HTTP requests to external websites
bs4 / beautifulsoup4	Parses HTML content (web scraping)
python-dotenv	Loads environment variables from .env file
python-box	Simplifies handling nested dictionaries

3. Runtime Requirements
To run properly, the project needs:

Item	Details
Python 3.8+	A modern Python version with venv support
.env file	For storing environment variables if used
Localhost browser	Used to interact with the Flask web interface

4. Project directory structure
  sitebot/
├── app.py                  # Main application entry point
├── requirements.txt        # List of required Python packages
├── .env                    # (optional) Environment variable definitions
├── commands/               # Folder containing command modules
│   ├── __init__.py         # (optional) Makes commands a Python package
│   ├── fact.py             # Command: provides random facts
│   ├── help.py             # Command: lists available commands
│   ├── paster.py           # Command: text/image paste
│   ├── shoti.py            # Command: short video fetcher
│   ├── test.py             # Command: for testing/debugging
│   └── webshot.py          # Command: website screenshot
├── templates/              # (Flask) HTML templates folder
│   └── index.html          # Web UI for interacting with the bot
└── static/                 # (Flask) Static assets like CSS/JS/images
    └── style.css           # Webpage styling


5. Any other step followed during the developments of the project
Modular Command Design – Each bot command was built as a separate Python file in the commands/ folder.

WebSocket Integration – Used Flask-SocketIO for real-time communication between user and bot.

Frontend Setup – A simple HTML/CSS chat interface was created for interacting with the bot.

Environment Setup – Used .env and python-dotenv for storing API keys or config.

Command Parsing Logic – app.py routes user messages to the correct command module.

Testing and Debugging – Included a test.py module for testing command responses.

Local Dev with Virtual Env – Used venv and requirements.txt for isolated development setup.
