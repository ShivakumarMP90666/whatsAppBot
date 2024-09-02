Certainly! Here's the entire `README.md` content in a single block for easy copy-pasting:

```markdown
# WhatsApp Chatbot for Bulk Messaging

This project is a Python-based WhatsApp chatbot that automates the process of sending bulk messages, images, and polls to contacts listed in a Google Sheet. The bot utilizes Selenium to interact with WhatsApp Web and can be customized to send various types of content to different contacts.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
  - [Basic Message Sending](#basic-message-sending)
  - [Sending Messages with Images](#sending-messages-with-images)
  - [Sending Messages with Polls](#sending-messages-with-polls)
- [Configuration](#configuration)
- [Creating Custom `run.bat` Files](#creating-custom-runbat-files)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Bulk Messaging:** Automatically sends messages to multiple contacts.
- **Image Attachment:** Allows attaching images to messages.
- **Poll Attachment:** Supports adding polls to messages.
- **Google Sheets Integration:** Fetches contact details and messages directly from Google Sheets.
- **Customizable:** Use different batch files (`run.bat`) for different messaging conditions.

## Installation

### Prerequisites

- Python 3.7+
- Google Chrome browser
- [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/downloads) (Handled automatically by `webdriver-manager`)

### Step-by-Step Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/whatsapp-chatbot.git
   cd whatsapp-chatbot
   ```

2. **Install the Required Python Packages:**

   Use the following command to install the dependencies:
   
   ```bash
   pip install -r requirements.txt
   ```

3. **Update `requirements.txt`:**

   If necessary, update the libraries to the latest versions:
   
   ```bash
   pip install --upgrade -r requirements.txt
   ```

## Project Structure

```
project/
│
├── app/
│   └── app.py
├── requirements.txt
└── run.bat files (customizable batch files for various messaging scenarios)
```

- **app/app.py:** The main script that handles the WhatsApp messaging automation.
- **requirements.txt:** Lists all required Python libraries.
- **run.bat:** Batch files for running the script with different configurations.

## Usage

### Basic Message Sending

To send messages to the contacts listed in a Google Sheet:

1. Update the Google Sheet URL in the `app.py` file.
2. Run the following command:

   ```bash
   python app/app.py SheetName
   ```

### Sending Messages with Images

To send messages with an image attachment:

1. Place your image in a known location.
2. Use the following command:

   ```bash
   python app/app.py SheetName --image-path="path/to/your/image.jpg"
   ```

### Sending Messages with Polls

To send messages with a poll:

1. Create another sheet in your Google Sheets document for poll data.
2. Use the following command:

   ```bash
   python app/app.py SheetName --attach-poll="PollSheetName"
   ```

## Configuration

- **Google Sheets:** Ensure that the Google Sheet is publicly accessible and that the contact column is named "Contact" and the message column is named "Message".
- **Browser:** ChromeDriver must match the version of your Chrome browser. This is automatically managed by `webdriver-manager`.

## Creating Custom `run.bat` Files

You can create different `.bat` files to run the script with different configurations. Here are examples:

### run_message.bat

```bat
@echo off
python app/app.py SheetName
pause
```

### run_image.bat

```bat
@echo off
python app/app.py SheetName --image-path="path/to/your/image.jpg"
pause
```

### run_poll.bat

```bat
@echo off
python app/app.py SheetName --attach-poll="PollSheetName"
pause
```

## Troubleshooting

- **QR Code Scanning:** Ensure that you scan the QR code promptly when prompted.
- **Contact Format:** Ensure that the contact numbers are in the correct format (e.g., `+91xxxxxxxxxx` for India).
- **Browser Issues:** If ChromeDriver fails to start, ensure that it matches the version of your installed Chrome browser.

## Contributing

Contributions are welcome! Please submit a pull request with your improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```

