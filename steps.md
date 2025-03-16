Here is the tuto url https://www.youtube.com/watch?v=tdU92hCgFU0


Here are the installation steps of browser-use 
Option 1: Local Installation

Read the quickstart guide or follow the steps below to get started.
Step 1: Clone the Repository

git clone https://github.com/browser-use/web-ui.git
cd web-ui

Step 2: Set Up Python Environment

We recommend using uv for managing the Python environment.

Using uv (recommended):

uv venv --python 3.11

Activate the virtual environment:

    Windows (Command Prompt):

.venv\Scripts\activate

    Windows (PowerShell):

.\.venv\Scripts\Activate.ps1

    macOS/Linux:

source .venv/bin/activate

Step 3: Install Dependencies

Install Python packages:

uv pip install -r requirements.txt

Install Playwright:

playwright install

Step 4: Configure Environment

    Create a copy of the example environment file:

    Windows (Command Prompt):

copy .env.example .env

    macOS/Linux/Windows (PowerShell):

cp .env.example .env

    Open .env in your preferred text editor and add your API keys and other settings



and u'll find the deep research feature in browser use ui


Here's how u run it 
Local Setup
Run the WebUI: After completing the installation steps above, start the application:

python webui.py --ip 127.0.0.1 --port 7788