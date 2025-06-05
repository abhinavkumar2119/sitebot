# Chatbot


## Contributors

- Abhinav Kumar [1DA21IS001]  
- P Bharath Kumar Reddy [1DA21IS034]

---

## 2. 📦 Project Dependencies / Requirements

Listed in `requirements.txt`:

bs4
Flask
Flask-SocketIO
requests
python-dotenv
python-box

pgsql
Copy
Edit

| Dependency      | Description                                         |
|-----------------|-----------------------------------------------------|
| Flask           | Web framework used to build the main app            |
| Flask-SocketIO  | Enables real-time communication over WebSocket      |
| requests        | Makes HTTP requests to third-party APIs              |
| beautifulsoup4  | Parses HTML content (web scraping)                   |
| python-dotenv   | Loads environment variables from `.env` file         |
| python-box      | Enables dot notation and cleaner nested dictionary access |

### Runtime Requirements

- **Python version:** 3.8 or above  
- **.env file (optional):** For storing secrets/configs  
- **Browser:** Required to access the web UI at `localhost:5000`

---

## 3. 🗂 Project Directory Structure

sitebot/
├── app.py # Main application file
├── requirements.txt # Lists Python dependencies
├── .env # (optional) Environment configuration file
├── commands/ # Command-specific Python modules
│ ├── init.py
│ ├── fact.py # Returns random facts
│ ├── help.py # Lists all commands
│ ├── paster.py # Uploads text/images
│ ├── shoti.py # Handles short video content
│ ├── test.py # For debugging/testing
│ └── webshot.py # Screenshots of webpages
├── templates/ # HTML template folder (Flask)
│ └── index.html
└── static/ # CSS or JavaScript assets
└── style.css

markdown
Copy
Edit

---

## 4. ⚙️ Other Steps Followed During Development

- **Modular Command Handling:** Each command is a separate Python script inside `commands/` for clean separation of features.  
- **WebSocket Communication:** Uses Flask-SocketIO for real-time updates between user and bot.  
- **Command Routing Logic:** The `app.py` script dynamically maps user inputs to command modules.  
- **Frontend Chat UI:** Built using basic HTML/CSS served through Flask (`templates/index.html` and `static/style.css`).  
- **Testing Support:** `commands/test.py` added for testing functionality in isolation.  
- **Environment Config:** Optional `.env` file support handled via `python-dotenv`.  
- **Isolated Dev Setup:** Virtual environment and `requirements.txt` ensure consistent local setup.  
