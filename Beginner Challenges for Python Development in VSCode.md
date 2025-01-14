# Beginner Challenges for Python Development in VSCode

These challenges are designed for beginners to practice their Python development skills while using VSCode. Each challenge builds on the previous ones, introducing new concepts step-by-step.

---

## Challenge 1: Install and Verify Python Setup

### Task:
1. Verify your Python installation by running:
   ```bash
   python --version
   ```
2. Open VSCode and create a new folder called `PythonChallenges`.
3. Create a new Python file named `challenge1.py` and add the following code:
   ```python
   print("Hello, Python World!")
   ```
4. Run the file in the terminal.

### Goal:
Ensure you can run a basic Python script in VSCode.

---

## Challenge 2: Install and Use Libraries

### Task:
1. Open your terminal in VSCode and install the `requests` library:
   ```bash
   pip install requests
   ```
2. Create a new Python file named `challenge2.py`.
3. Write a script to fetch data from a public API. Use the following code as a template:
   ```python
   import requests

   response = requests.get("https://api.github.com")
   if response.status_code == 200:
       print("API fetched successfully!")
       print("Response:", response.json())
   else:
       print(f"Failed to fetch API: {response.status_code}")
   ```
4. Run the script and observe the output.

### Goal:
Understand how to install and use external libraries like `requests`.

---

## Challenge 3: Parse HTML with BeautifulSoup

### Task:
1. Install `beautifulsoup4`:
   ```bash
   pip install beautifulsoup4
   ```
2. Create a new Python file named `challenge3.py`.
3. Write a script to scrape and print the title of a webpage:
   ```python
   import requests
   from bs4 import BeautifulSoup

   url = "https://example.com"
   response = requests.get(url)

   if response.status_code == 200:
       soup = BeautifulSoup(response.text, 'html.parser')
       print("Page Title:", soup.title.string)
   else:
       print("Failed to fetch the page")
   ```
4. Run the script and verify the output.

### Goal:
Learn how to use `BeautifulSoup` to parse HTML content.

---

## Challenge 4: URL Manipulation with urllib

### Task:
1. Create a new Python file named `challenge4.py`.
2. Write a script to encode a query into a URL:
   ```python
   import urllib.parse

   query = {"search": "python challenges", "page": 1}
   encoded_query = urllib.parse.urlencode(query)
   print("Encoded Query:", encoded_query)
   ```
3. Run the script and verify the encoded query string.

### Goal:
Understand how to use `urllib` for URL encoding.

---

## Challenge 5: Debugging in VSCode

### Task:
1. Create a new Python file named `challenge5.py`.
2. Copy and paste the following code into the file:
   ```python
   def divide_numbers(a, b):
       return a / b

   result = divide_numbers(10, 0)
   print("Result:", result)
   ```
3. Set a breakpoint on the line `return a / b`.
4. Run the debugger and analyze the error.
5. Fix the script to handle division by zero:
   ```python
   def divide_numbers(a, b):
       try:
           return a / b
       except ZeroDivisionError:
           return "Division by zero is not allowed"

   result = divide_numbers(10, 0)
   print("Result:", result)
   ```
6. Debug again to confirm the fix.

### Goal:
Learn how to use VSCode's debugging tools and handle exceptions in Python.

---

## Challenge 6: Create a Virtual Environment

### Task:
1. Open your terminal in VSCode.
2. Create a virtual environment named `venv`:
   ```bash
   python -m venv venv
   ```
3. Activate the virtual environment:
   - **Windows:**
     ```bash
     venv\Scripts\activate
     ```
   - **macOS/Linux:**
     ```bash
     source venv/bin/activate
     ```
4. Install `requests` in the virtual environment:
   ```bash
   pip install requests
   ```
5. Verify the installation by running:
   ```bash
   pip list
   ```

### Goal:
Learn how to create and use virtual environments in Python.

---

## Challenge 7: Combine Everything

### Task:
1. Create a new Python file named `challenge7.py`.
2. Write a script that:
   - Fetches HTML from `https://example.com` using `requests`.
   - Parses the page title using `BeautifulSoup`.
   - Encodes a URL query using `urllib.parse`.
   ```python
   import requests
   from bs4 import BeautifulSoup
   import urllib.parse

   url = "https://example.com"
   response = requests.get(url)

   if response.status_code == 200:
       soup = BeautifulSoup(response.text, 'html.parser')
       print("Page Title:", soup.title.string)

       query = {"search": "example", "page": 1}
       encoded_query = urllib.parse.urlencode(query)
       print("Encoded Query:", encoded_query)
   else:
       print("Failed to fetch the page")
   ```
3. Run the script and verify the output.

### Goal:
Combine your knowledge of `requests`, `BeautifulSoup`, and `urllib` into a single project.

---

Happy Coding!

