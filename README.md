# System-Commander-AI-Assistant-with-System-Control

🤖 System Commander: AI Assistant with System Control


Bridge conversational AI with real system operations • Military-grade security • Cross-platform compatibility

Developed during my internship at Indian Institute of Technology Jammu in collaboration with Techible and Institute Incubation and Innovation Council (I3C)

# 🔍 Overview
System Commander is an AI-powered assistant that executes system commands through natural language. It transforms requests like "Open Chrome and search for AI news" into actual system operations while maintaining enterprise-grade security protocols.


# ✨ Features
Natural Language Processing: Understands complex commands
System Operations:

Launch applications (Open Photoshop)

Perform web searches (Search for Python tutorials)

Read file contents (Show todo.txt)

Execute approved scripts (Run backup.py)

Security First:

Path allow-listing

30-second process timeouts

Output truncation

Explicit user confirmations

Cross-Platform: Windows, macOS, Linux support

Dual Interface: CLI + Web UI

# ⚙️ How It Works
System Architecture
Diagram
<img width="716" height="343" alt="image" src="https://github.com/user-attachments/assets/ee0e42d7-c06f-4466-85d8-afc34b9523d0" />










Technical Process
User Input: Natural language command

AI Processing: GPT-4o-mini interprets intent

Security Validation:

Path allow-list check

Operation risk assessment

Resource allocation

Tool Execution: OS-specific implementation

Output Delivery: Results returned to user

# 🛠️ Tech Stack
Component	Technology
AI Engine	OpenAI Assistants API (gpt-4o-mini)
Backend	Python 3.12
Interface	Gradio (Web UI) + CLI
Security	Custom validation layers + Dotenv
Operations	subprocess, webbrowser, os modules


# 🧪 Usage
Basic Commands
bash
# Open applications
"Launch Chrome browser"

# Web searches
"Search for machine learning trends"

# Read files
"Show project README.md"

# Execute scripts (must be in /scripts/)
"Run /scripts/backup.py"
Security Features
python
# Security core - Path validation
def run_script(script_path: str):
    allowed_paths = ["/scripts/", "./scripts/"]
    if not any(path in script_path for path in allowed_paths):
        return "❌ Access denied to path"
    
    # Execute with 30-second timeout
    result = subprocess.run(script_path, timeout=30, capture_output=True)
    return result.stdout
# 🔒 Security Architecture
Input Sanitization: Filters malicious commands

Path Allow-Listing: Restricted script execution

Resource Limits:

30-second process timeout

5000-character file read limit

Confirmation Protocol: User approval for high-risk operations

Environment Isolation: Separate execution threads

# 🌟 Internship Context
Developed during my internship at Indian Institute of Technology Jammu in collaboration with Techible and Institute Incubation and Innovation Council (I3C). Special thanks to:

Techible Infrastructure Team

I3C Incubation Program

# 🤝 Contributing
Fork the repository

Create your feature branch (git checkout -b feature/amazing-feature)

Commit your changes (git commit -m 'Add amazing feature')

Push to branch (git push origin feature/amazing-feature)

Open a pull request

📜 License
Distributed under the MIT License. See LICENSE for more information.
