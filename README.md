## Command Generator - A powerful customizable command generation tool




Command Generator is a utility-type project implemented entirely in HTML. It does not require any special environment or dependencies — it can be launched and run directly in a web browser.

Define your commonly used command templates and the required variables. Change the variable values in real time, and all commands will be generated automatically. Click to copy them and paste them where they need to be used.

You can use it as your memo or notepad, especially when working with multiple tools. Let it automatically generate any text, commands, or scripts you need, instead of manually moving the cursor through large blocks of copied text to fill in IP addresses or paths.

It’s  powerful, but trust me — once you open it, you’ll immediately understand how to use it.




## Features

- 📋 **Command Management**
Create, edit, delete command templates  

- 📃 Script Mode
In addition to single commands, you can also create large code blocks for scripts.

- 📁 **Column Organization**
Organize and arrange your commands in columns in any way you like.

- 🔍 **Smart Search**
Search commands by title and description  

- 🏷️ **Tag System**
Add tags to your commands to quickly filter and find them.  

- 🎯 **Variable Management**
Define variables in commands using the `${{variable_name}}` format, with dynamic replacement and automatic insertion support  

- 📤 **Data Import & Export**
Support JSON format backups and migration; all data is stored locally with no network communication  

- 📚 **Custom Sorting**
Freely change the order of commands according to your preferences.

- ⚡ **Real-time Preview**
Command previews update instantly while editing variables


## ScreenShot


<img width="2875" height="1564" alt="image" src="https://github.com/user-attachments/assets/90dad8ba-385a-485e-ae0c-72f1a3e23092" />

<img width="2854" height="1523" alt="image" src="https://github.com/user-attachments/assets/93027cd7-b2c3-440d-b5a1-c366ad720fee" />

<img width="2887" height="1572" alt="image" src="https://github.com/user-attachments/assets/d8df909f-11f6-4407-b24e-03eb2c79dfc2" />

<img width="2863" height="1523" alt="image" src="https://github.com/user-attachments/assets/1c1ea44c-a5ae-41a9-81da-04e4fa6dd88d" />

<img width="2840" height="1545" alt="image" src="https://github.com/user-attachments/assets/0b349032-1320-4587-af6a-df8a74f9f8ed" />



## How to Start

1. Download the `command-generator.html` file

2. Open the file in any modern web browser

3. **Use it! It’s that simple!**


## Key Features


### Command Templates

Create command templates with variable placeholders that are replaced with actual values when generated. All new variable will create and add automaticlly. You can add multiple commands and separate them with line breaks. Each command will generate its own code block.

```bash
# Example command template

cd ${{PATH}} && git commit -m "${{MESSAGE}}"

```

### Multi-line Commands or Script

Support for multi-line commands using the `---script---` and `---end---` markers:
  
```bash
# Example script template
---script---

cd ${{PATH}}

git add .

git commit -m "${{MESSAGE}}"

git push

---end---
```

Those command will show on a single code block.




## Technologies Used

- HTML5

- CSS3 (Flexbox, CSS Variables, Media Queries)

- JavaScript (ES6+)

- LocalStorage for data persistence



## Localization

The application supports both English and Chinese:

1. Click on the language switcher in the bottom left corner

2. Select your preferred language

3. The interface will update to your selected language




## Data Persistence

All data is stored in your browser's LocalStorage, which means:

- Data persists between browser sessions

- Data is stored locally on your device

- No data is sent to any server

- Clearing your browser's localStorage will delete all saved commands and variables


## Changelog


### V0.4

- Added support for multiple languages such as English.
- Improved the UI for small-screen devices.

### V0.3

- Fixed some bugs.
- Added support for multiple commands and scripts.

### V0.2

- Added column and sorting features 
- Designed a more modern UI.

### V0.1

The basic functionality has been implemented.



## License


This project is open source and available under the MIT License.
