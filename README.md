Snipping Tool with OCR 📸✂️
A Python application that lets you capture a screenshot by drawing a rectangle on the screen, extract text using OCR, and copy it to your clipboard! 🚀
Features ✨

Capture a custom screen region by dragging the mouse 🖱️
Extract text from the captured image using Tesseract OCR 📝
Copy extracted text to the system clipboard 📋
Transparent overlay for intuitive snipping 🌫️
Crosshair-style selection with a green outline 🟢
Exit the app by pressing any key 🚪

Requirements 🛠️

Python 3.x 🐍
Required Python packages:pip install pillow pytesseract pyperclip PyQt5


Tesseract OCR installed on your system:
For Windows, install Tesseract and ensure it's at C:\Program Files\Tesseract-OCR\tesseract.exe (or update the path in ImageReader.__init__) 🖥️
For Linux/macOS, install Tesseract via your package manager (e.g., apt install tesseract-ocr or brew install tesseract) 🐧🍎



Usage 🎬

Run the script:python snipping_tool.py


The screen will dim, and a transparent overlay will appear 🌫️
Click and drag the mouse to select a rectangular area 🖌️
Release the mouse to capture the selected area ✅
The extracted text will be printed to the console and copied to the clipboard 🖨️📋
Press any key or release the mouse to exit the application 🚶‍♂️

How It Works 🧠

SnippingTool: A PyQt5-based widget that creates a full-screen overlay for capturing a user-defined rectangular area 📷
Takes a screenshot on initialization and saves it as screenshot.png 🖼️
Draws a green outline as the user drags the mouse to select an area 🟩
Crops the selected area and saves it as snip.png ✂️


ImageReader: Uses Tesseract OCR (via pytesseract) to extract text from snip.png 📖
The extracted text is copied to the clipboard using pyperclip 📋

Files Generated 📁

screenshot.png: Temporary full-screen screenshot 🖼️
snip.png: Cropped image of the selected area 🖌️

Limitations ⚠️

Hardcoded Tesseract path for Windows (C:\Program Files\Tesseract-OCR\tesseract.exe). Modify the path in ImageReader.__init__ for other systems or installations 🛠️
Currently supports English (ENG) for OCR. To use other languages, modify the lang parameter in ir.extract_text("snip.png", "ENG") 🌐
No error handling for missing Tesseract installation or invalid image files 🚫
Temporary files (screenshot.png, snip.png) are not automatically deleted 🗑️

Future Improvements 🔮

Add error handling for Tesseract installation and image processing 🛡️
Support configurable Tesseract paths and OCR languages ⚙️
Automatically clean up temporary files 🧹
Add a GUI for selecting OCR language or other options 🖥️
Support multi-monitor setups 🖥️🖥️

License 📜
This project is licensed under the MIT License. See the LICENSE file for details 🗳️

Happy snipping! 😄 Feel free to customize this README further for your project! 🌟
