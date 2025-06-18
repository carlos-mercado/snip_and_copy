🖼️ Snip & Copy Tool
A simple Python-based screen snipping tool with built-in Optical Character Recognition (OCR). Select an area of your screen, and the text within it will be automatically extracted and copied to your clipboard.

✨ Features
Fullscreen transparent snipping overlay

Rectangle selection with visual feedback

Image cropping and saving

OCR (via Tesseract) on the snipped region

Automatically copies extracted text to clipboard

📦 Requirements
Python 3.6+

Tesseract-OCR installed on your machine
(default path assumed: C:\Program Files\Tesseract-OCR\tesseract.exe)

Python dependencies:

PyQt5

pytesseract

Pillow

pyperclip

You can install all dependencies with:

bash
Copy
Edit
pip install PyQt5 pytesseract Pillow pyperclip
🛠 Setup
Install Tesseract
Download from here and install it.
Make sure it's installed in the default location or adjust the path in the script.

Run the Tool

bash
Copy
Edit
python main.py
🖱️ How to Use
When launched, the app overlays your screen with a transparent window.

Click and drag to select the area you want to capture.

Release the mouse to snip and extract text.

The extracted text will be printed in the console and copied to your clipboard automatically.

Press any key to exit at any time.

📁 File Output
A full screenshot is saved as: screenshot.png

The cropped snip is saved as: snip.png

🧠 Behind the Scenes
Uses QPainter and mouse events to handle selection UI.

Saves a screenshot and crops it based on selection coordinates.

Feeds the cropped image to pytesseract for OCR.

Copies the result to clipboard via pyperclip.

📸 Example
Coming soon: GIF or screenshot demo

✅ Todo / Improvements
Configurable OCR language

Support for multi-monitor setups

Customizable output paths

GUI feedback (toast or popup) after copying text

📜 License
MIT License — free to use and modify.
