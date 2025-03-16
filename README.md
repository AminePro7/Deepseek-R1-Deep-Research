# 🔍 Deepseek-R1 Deep Research

[![GitHub stars](https://img.shields.io/github/stars/AminePro7/Deepseek-R1-Deep-Research?style=social)](https://github.com/AminePro7/Deepseek-R1-Deep-Research/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/AminePro7/Deepseek-R1-Deep-Research?style=social)](https://github.com/AminePro7/Deepseek-R1-Deep-Research/network/members)
[![GitHub issues](https://img.shields.io/github/issues/AminePro7/Deepseek-R1-Deep-Research)](https://github.com/AminePro7/Deepseek-R1-Deep-Research/issues)
[![License](https://img.shields.io/github/license/AminePro7/Deepseek-R1-Deep-Research)](https://github.com/AminePro7/Deepseek-R1-Deep-Research/blob/main/LICENSE)
[![Twitter Follow](https://img.shields.io/twitter/follow/AminePro7?style=social)](https://twitter.com/AminePro7)

## 📋 Overview

This project integrates Deepseek-R1 with browser-use web-ui to enable AI-powered deep research capabilities. It allows AI agents to browse the web, conduct research, and perform complex tasks with persistent browser sessions and high-definition screen recording.

![Agent History](web-ui/agent_history.gif)

## ✨ Features

- 🧠 **Deepseek-R1 Integration**: Leverage Deepseek-R1's powerful reasoning capabilities for deep research tasks
- 🌐 **Browser Automation**: AI agents can navigate websites, fill forms, and interact with web content
- 💾 **Persistent Sessions**: Keep browser windows open between AI tasks to maintain context and history
- 🖥️ **Custom Browser Support**: Use your own browser with existing logins and configurations
- 📊 **High-Definition Recording**: Capture detailed screen recordings of AI interactions
- 🔄 **Multiple LLM Support**: Compatible with various models including OpenAI, Anthropic, Google, and more

## 🚀 Installation

### Prerequisites
- Python 3.11 or higher
- Git (for cloning the repository)

### Option 1: Local Installation

#### Step 1: Clone the Repository
```bash
git clone https://github.com/AminePro7/Deepseek-R1-Deep-Research.git
cd Deepseek-R1-Deep-Research
```

#### Step 2: Set Up Python Environment
We recommend using [uv](https://docs.astral.sh/uv/) for managing the Python environment.

```bash
uv venv --python 3.11
```

Activate the virtual environment:
- Windows (Command Prompt):
```cmd
.venv\Scripts\activate
```
- Windows (PowerShell):
```powershell
.\.venv\Scripts\Activate.ps1
```
- macOS/Linux:
```bash
source .venv/bin/activate
```

#### Step 3: Install Dependencies
Install Python packages:
```bash
uv pip install -r web-ui/requirements.txt
```

Install Playwright:
```bash
playwright install
```

#### Step 4: Configure Environment
1. Create a copy of the example environment file:
```bash
cp web-ui/.env.example web-ui/.env
```
2. Open `web-ui/.env` in your preferred text editor and add your API keys and other settings

### Option 2: Docker Installation

#### Prerequisites
- Docker and Docker Compose installed

#### Installation Steps
1. Clone the repository:
```bash
git clone https://github.com/AminePro7/Deepseek-R1-Deep-Research.git
cd Deepseek-R1-Deep-Research
```

2. Create and configure environment file:
```bash
cp web-ui/.env.example web-ui/.env
```

3. Run with Docker:
```bash
# Build and start the container with default settings
cd web-ui
docker compose up --build
```

```bash
# Or run with persistent browser
CHROME_PERSISTENT_SESSION=true docker compose up --build
```

4. Access the Application:
- Web Interface: Open `http://localhost:7788` in your browser
- VNC Viewer (for watching browser interactions): Open `http://localhost:6080/vnc.html`
  - Default VNC password: "vncpassword"

## 💻 Usage

### Local Setup
1. Run the WebUI:
```bash
cd web-ui
python webui.py --ip 127.0.0.1 --port 7788
```

2. WebUI options:
   - `--ip`: The IP address to bind the WebUI to. Default is `127.0.0.1`.
   - `--port`: The port to bind the WebUI to. Default is `7788`.
   - `--theme`: The theme for the user interface. Default is `Ocean`.
   - `--dark-mode`: Enables dark mode for the user interface.

3. Access the WebUI: Open your web browser and navigate to `http://127.0.0.1:7788`.

### Using Your Own Browser (Optional)
1. Set `CHROME_PATH` to the executable path of your browser and `CHROME_USER_DATA` to the user data directory in the `.env` file.
2. Close all Chrome windows
3. Open the WebUI in a non-Chrome browser
4. Check the "Use Own Browser" option within the Browser Settings.

### Keep Browser Open (Optional)
- Set `CHROME_PERSISTENT_SESSION=true` in the `.env` file.

## 🔧 Configuration

### Environment Variables
All configuration is done through the `.env` file. Key variables include:

```
# LLM API Keys
OPENAI_API_KEY=your_key_here
ANTHROPIC_API_KEY=your_key_here
GOOGLE_API_KEY=your_key_here
DEEPSEEK_API_KEY=your_key_here

# Browser Settings
CHROME_PERSISTENT_SESSION=true   # Set to true to keep browser open between AI tasks
RESOLUTION=1920x1080x24         # Custom resolution format
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgements

- [browser-use](https://github.com/browser-use/browser-use) - The foundation for this project
- [Deepseek-R1](https://github.com/deepseek-ai/DeepSeek-Coder) - For the powerful AI reasoning capabilities
- [WarmShao](https://github.com/warmshao) - For contributions to the browser-use project

## 📬 Contact

AminePro7 - [@AminePro7](https://twitter.com/AminePro7)

Project Link: [https://github.com/AminePro7/Deepseek-R1-Deep-Research](https://github.com/AminePro7/Deepseek-R1-Deep-Research) 