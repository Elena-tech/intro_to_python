# Setting Up Visual Studio Code (VSCode) for Python Development

This guide is designed for beginners to set up VSCode for Python development and work with popular libraries like `requests`, `urllib`, and `BeautifulSoup`. Follow these steps to start coding with ease.

---

## 1. Install Visual Studio Code (VSCode)

### Steps:
1. Go to the [VSCode website](https://code.visualstudio.com/).
2. Download the installer for your operating system (Windows, macOS, or Linux).
3. Run the installer and follow the instructions to complete the installation.

---

## 2. Install Python

### Steps:
1. Download Python from the official website: [Python.org](https://www.python.org/).
2. Select the latest stable version and download the installer for your operating system.
3. **Important:** During installation, check the box that says `Add Python to PATH`.
4. Follow the installation wizard to complete the setup.

### Verify Installation:
1. Open a terminal (Command Prompt, PowerShell, or Terminal on macOS/Linux).
2. Type `python --version` or `python3 --version` and press Enter.
   - You should see the Python version displayed.

---

## 3. Set Up VSCode for Python

### Install the Python Extension:
1. Open VSCode.
2. Go to the Extensions view by clicking the Extensions icon on the left sidebar or pressing `Ctrl+Shift+X` (`Cmd+Shift+X` on macOS).
3. Search for "Python" in the search bar.
4. Install the extension developed by Microsoft.

### Select Python Interpreter:
1. Press `Ctrl+Shift+P` (`Cmd+Shift+P` on macOS) to open the Command Palette.
2. Type "Python: Select Interpreter" and select it.
3. Choose the Python interpreter you installed earlier.

---

## 4. Create a Python Project

### Steps:
1. Open VSCode and create a new folder for your project.
   - Go to `File > Open Folder` and select your project folder.
2. Create a new Python file:
   - Click on `File > New File` and save it with a `.py` extension (e.g., `main.py`).

---

## 5. Install Python Libraries

### Install pip:
- `pip` is Python’s package manager, usually included with Python. Verify its installation:
  ```bash
  pip --version
  ```
  If not installed, run:
  ```bash
  python -m ensurepip
  ```

### Install Libraries:
1. Open a terminal in VSCode by clicking `Terminal > New Terminal`.
2. Use the following commands to install libraries:
   - `requests`:
     ```bash
     pip install requests
     ```
   - `BeautifulSoup` (from `bs4`):
     ```bash
     pip install beautifulsoup4
     ```
   - `urllib` is part of Python's standard library, so no installation is needed.

---

## 6. Example Python Code

Here’s an example script using `requests`, `urllib`, and `BeautifulSoup`:

```python
import requests
from bs4 import BeautifulSoup
import urllib.parse

# Example URL
url = "https://example.com"

# Fetch the webpage
response = requests.get(url)

# Check the status code
if response.status_code == 200:
    print("Page fetched successfully!")
else:
    print(f"Failed to fetch the page: {response.status_code}")

# Parse the HTML content
soup = BeautifulSoup(response.text, 'html.parser')

# Print the page title
print("Page Title:", soup.title.string)

# Example of URL encoding
query = {"search": "python tutorial"}
encoded_query = urllib.parse.urlencode(query)
print("Encoded URL Query:", encoded_query)
```

### Run the Script:
1. Save the file (e.g., `main.py`).
2. Open the terminal and run:
   ```bash
   python main.py
   ```

---

## 7. Debugging in VSCode

### Steps:
1. Click on the Debug icon in the left sidebar.
2. Click "Run and Debug" and choose "Python File".
3. Set breakpoints by clicking next to the line numbers in your code.
4. Use the Debug panel to control the execution.

---

## 8. Additional Tips

- **Formatting Code:** Install the "Prettier" or "Black" extension for automatic formatting.
- **Linting:** Use `flake8` for code style checks:
  ```bash
  pip install flake8
  ```
  Enable it in VSCode settings.
- **Virtual Environments:** Create a virtual environment for your projects:
  ```bash
  python -m venv venv
  source venv/bin/activate   # macOS/Linux
  venv\Scripts\activate     # Windows
  ```

---

Now you are ready to develop Python projects in VSCode! Start exploring and coding!

