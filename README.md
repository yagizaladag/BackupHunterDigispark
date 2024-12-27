# DigisparkBackupMailer

A simple and effective solution to automatically collect backup files from all users on a system using the Digispark microcontroller. The backup files are then sent to a predefined email address for safekeeping.

**Disclaimer:** This project is for educational and testing purposes only. It should not be used for malicious intent or unauthorized access. Always ensure you have explicit permission before running any security or automation tools on any system.

## Features

- **Backup Collection:** Automatically copies files from all user directories to a designated backup folder.
- **Email Sending:** Sends the backup files via email to a static email address.
- **Platform:** Powered by the Digispark USB microcontroller.
- **Lightweight:** Runs efficiently on small embedded devices like Digispark.

## Requirements

- **Digispark USB Development Board:** Ensure you have the Digispark board connected and properly configured.
- **DigiKeyboard Library:** Used to simulate keyboard input.
- **Microsoft Outlook:** Configured on the system for email sending (customizable for different email clients).
- **Windows Operating System:** Designed for use on Windows platforms.

## Setup and Usage

### 1. Clone or Download the Repository

```bash
git clone https://github.com/yourusername/DigisparkBackupMailer.git
2. Install DigiKeyboard Library
Open Arduino IDE.
Go to Sketch > Include Library > Manage Libraries.
Search for DigiKeyboard and install it.
3. Upload the Code to Digispark
Open the DigisparkBackupMailer project in the Arduino IDE.
Select the Digispark (Default - 16.5mhz) board from Tools > Board.
Click Upload to flash the code onto your Digispark board.
4. Run the Code
Insert the Digispark device into a Windows machine. The script will automatically execute, copy backup files, and send them via email.
Code Explanation
Backup Process
The code begins by running a command to copy all user directories (C:\Users*) to a local backup folder (C:\Backup). The xcopy command is used with flags to ensure all hidden files and permissions are maintained during the copy process.

Email Sending
After completing the backup, the code opens Microsoft Outlook, creates a new email, and attaches the backup files. The email is sent to the static address defined in the script (e.g., yagiz_aladag@hotmail.com).

Keyboard Simulation
The Digispark microcontroller emulates keyboard strokes to interact with the system's command line and Outlook. This is accomplished using the DigiKeyboard library, which simulates keypress events.

Warnings
Permission
This code should only be used on machines where you have explicit permission to perform such operations. Unauthorized access to systems or data is illegal and unethical.

Security
This project is intended for educational purposes only and should not be used in real-world malicious activities. Use it responsibly.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Author
Yagiz Aladag
Email: yagiz_aladag@hotmail.com

Final Note
The DigisparkBackupMailer project demonstrates how embedded devices like Digispark can be used to automate simple tasks. Be mindful of privacy and legality when experimenting with such projects.



arduino
