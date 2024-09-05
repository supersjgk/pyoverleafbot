# Overleaf Automation Bot to Appear Active (pyoverleafbot)

### Overview
pyoverleafbot is built to help users appear active on collaborative Overleaf projects. It automates iinteractions with Overleaf.

### Tech Stack
- Python
- Selenium

### What can this be used for?
- **For PhD Students:** Helps manage stress
- **Coffee Break:** Set up the bot to run during breaks to keep your presence active.
- **Scheduled Runs:** Schedule the bot to run at specific times to maintain activity on projects.

### Why use Selenium rather than simple pyautogui?
- Selenium is an automation tool
- Selenium can interact directly with web applications in any browser
- Selenium provides high level interaction with the web elements
- Selenium can be used for web scraping
- Selenium scripts can be used in Headless Mode

### Implementations
- Platforms:
    - [x] Windows
        - Robust Login:
            - [x] Windows Credential Manager + Store session information for faster login
            - [ ] Gmail
        - Broswers:
            - [x] Chrome
            - [ ] Others
        - Scheduling (in progress):
            - [ ] Scheduled Runs when power on (logged in/logged out)
            - [ ] Scheduled Runs when power off
        - Functionalities:
            - [x] Fully automated
            - [x] Manage credentials securely
            - [x] Select project you want to work on
            - [x] Appear active
            - [ ] Headless Mode
    - [ ] Linux (in progress)
    - [ ] Mac (who uses Mac?)

### One time setup
- Prerequisites: Windows with Python and Chrome browser installed.
- Clone the repository: `git clone https://github.com/supersjgk/pyoverleafbot`
- `cd pyoverleafbot`
- Install the dependencies: `pip install -r requirements.txt`
- `cd pyoverleafbot`
- Set Credentials in Windows Credential Manager by running: `python credential_manager.py set OverleafBot`
- Run the script: 
    - The Bot displays the available overleaf projects and prompts you to select: `python script.py` 
    - If you know the Overleaf Project ID: `python script.py --project_id <Project ID>`
    - If you want to appear active for x minutes (default 5 minutes), use the argument `--duration <x>`
    - The bot repeatedly selects a random line (every 5 to 10 seconds) in the project to appear active. To override default values, use the arguments: `--min_change_time <min_seconds> --max_change_time <max_seconds>`