# Welcome Script Collection

## Overview
This repository contains three VBScript files that provide a personalized text-to-speech (TTS) welcome message when a user logs into Windows. The scripts retrieve the logged-in username, extract the first name, and use the Windows Speech API (SAPI) to greet the user. 

## Files Description
1. **`Welcomefirstname_werrorhandling.vbs`**  
   - Includes error handling to prevent script crashes.
   - Prompts the user to select a voice from the available installed voices.
   - If an error occurs, displays a message box with an error description.

2. **`Welcome firstname.vbs`**  
   - Retrieves the first name from the username.
   - Uses a single predefined welcome message.

3. **`Welcome Random.vbs`**  
   - Retrieves the first name from the username.
   - Randomly selects one of three predefined welcome messages for variety.

## Installation (Run on Startup)
To run the script automatically at startup, follow these steps:

### Method 1: Place in the Startup Folder (Recommended)
1. **Open the Startup Folder**:  
   Press `Win + R`, type:
   ```
   shell:startup
   ```
   and press `Enter`.

2. **Copy the Script**:  
   - Move or copy your desired `.vbs` script into the opened `Startup` folder.
   - This ensures that the script runs automatically when the user logs in.

### Method 2: Use Task Scheduler (For Admin Users)
If you want more control over execution (e.g., running with admin privileges):

1. **Open Task Scheduler**:  
   - Press `Win + S`, type `Task Scheduler`, and open it.

2. **Create a New Task**:  
   - Click on `Create Basic Task`.
   - Name it something like **Welcome Message**.
   - Click `Next`, and select `When I log on`.
   - Click `Next`, select `Start a program`, and browse to the `.vbs` file location.
   - Finish the setup.

3. **Optional**:  
   - If you need admin rights, edit the task properties and check `Run with highest privileges`.

## Troubleshooting
- **No Sound?**  
  Ensure that your speakers are on and SAPI voices are installed.
- **Error Message?**  
  Use the `Welcomefirstname_werrorhandling.vbs` version, which includes error handling.

## License
This script is free to use and modify.
