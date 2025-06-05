👥 Contributors
Abhinav Kumar [1DA21IS001]

P Bharath Kumar Reddy [1DA21IS034]

🧰 Python Libraries (Dependencies)
Listed in requirements.txt:

Package	Purpose
Flask	Web framework for handling HTTP routes
Flask-SocketIO	Enables real-time, bidirectional communication
requests	Handles HTTP requests to external websites
bs4 / beautifulsoup4	Parses HTML content for scraping
python-dotenv	Loads environment variables from .env file
python-box	Simplifies handling of deeply nested dictionaries

🧩 Runtime Requirements
Item	Details
Python	3.8+ (Ensure venv is available)
.env file	Optional — store API keys or config variables
Web Browser	Use browser on localhost to access chat interface

📁 Project Directory Structure
bash
Copy
Edit
sitebot/
├── app.py                  # Main application entry point
├── requirements.txt        # Python packages needed to run the app
├── .env                    # (optional) Environment variables
├── commands/               # All command logic
│   ├── __init__.py
│   ├── fact.py             # Returns random facts
│   ├── help.py             # Lists available commands
│   ├── paster.py           # Pastes text/image to external service
│   ├── shoti.py            # Short video fetcher
│   ├── test.py             # Command test/debug module
│   └── webshot.py          # Takes website screenshot
├── templates/              # HTML templates for Flask
│   └── index.html
└── static/                 # CSS/JS/image assets
    └── style.css
🛠️ Development Steps Followed
Modular Command Design: Each command is separated into its own Python module.

WebSocket Integration: Flask-SocketIO enables instant bot responses.

Frontend Setup: Simple Flask-based web UI using HTML/CSS.

Environment Management: Used .env + python-dotenv for config handling.

Command Routing: app.py routes user messages to appropriate modules.

Testing: Included test.py for validating functionality.

Isolated Environment: Used venv and requirements.txt for clean dev setup.

🚀 Getting Started
bash
Copy
Edit
# Clone the repo
git clone https://github.com/christhenoob13/sitebot
cd sitebot

# Set up virtual environment
python -m venv venv
source venv/bin/activate       # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the app
python app.py
Visit http://localhost:5000 in your browser to start chatting with SiteBot!

