# Keylogger Script

This Python script is a basic implementation of a keylogger that listens to keyboard events using the `pynput` library. The keystrokes are logged and sent to a remote server periodically.

## Features:
- **Keystroke Logging**: The script records all key presses (including modifier keys) and stores them in a string.
- **Data Transmission**: The collected data is sent to a server (via HTTP) at a specified IP address and port number.
- **Data Format**: The logged keystrokes are sent as a JSON payload with the key `"keyboardData"`.

## How It Works:
1. **Listening to Keyboard**: The script listens for key press events via the `pynput` keyboard listener. When a key is pressed, the corresponding character is added to a global string.
2. **Data Transmission**: Every 10 seconds, the logged data is sent to a remote server via an HTTP POST request.
