# PowerShell-Gemini-Chatbot
This is a PowerShell-based chatbot client for Google’s Gemini API. It supports:  Normal chat  File uploads  Clipboard uploads  Automatic chunking for long text  Batch mode uploads  Conversation memory (last 20 messages)


1. Save the Script
Save the script as:
Powershell_chatbot.ps1
You must save it with the .ps1 extension because this is a PowerShell script.

Recommended location:
C:\Users\<YourUsername>\Powershell_chatbot.ps1

2. Add Your API Key
Open the script and find this line:
$env:API_KEY = "YOUR_REAL_KEY_HERE"
Replace it with your actual Gemini API key

How to Run the Script
Method 1: Using the provided command (recommended)
Open Command Prompt, Run (Win+R), or PowerShell, then run:
**powershell -ExecutionPolicy Bypass -File "$env:USERPROFILE\Powershell_chatbot.ps1"**
This runs the script even if PowerShell script execution is restricted.

Method 2: From PowerShell directly
If you're already inside PowerShell:
powershell -ExecutionPolicy Bypass -File "$env:USERPROFILE\Powershell_chatbot.ps1"
or if you're inside the folder:
.\Powershell_chatbot.ps1

If PowerShell Blocks the Script
PowerShell may block unknown scripts by default.
To allow temporary execution only for this session:
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
Then run the script.

4. Using the Chatbot
When the script starts, you will see:
Gemini Chat Ready — type your question and press Enter.
Commands:
  /file <path>       - send file contents
  /clip              - send clipboard contents
  /batchfile <path>  - upload file chunks, reply once
  /batchclip         - upload clipboard, reply once
  EXIT               - quit

Examples:
Ask a question:
Hello!
Upload a file:
/file C:\notes\essay.txt
Send clipboard:
/clip
Exit:
EXIT

🧠 5. Chat Memory
The script remembers the last 20 messages in the conversation so you can have a continuous back-and-forth chat.
