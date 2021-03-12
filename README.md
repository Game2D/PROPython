#================#
#                #
#   PROPython    #
#				 #
#================#
#				 #
# VERSION: 1.0.1 #
#                #
#================#


# This function shows name of package
PackageName()

# Works like a print but only displays a message (int, float, string or do funtion and print result)
cmd(MESSAGE)

# You can make text in different colors instead of color ID you can write Python colors
cmdColor(MESSAGE, colorID)

# Saving the file. FILENAME - file name. STRING - what you want to save to a file (String).
saveF(FILENAME, STRING)

# Deletting file. FILEPATH - the path to the file you want to delete. (For example - "C:/MY_WORK/Python/my_file.py")
deleteF(FILEPATH)

# Displays an error. ERRORmessage - error.
cmdError(ERRORmessage)

# This function creates a file. FILENAME - the name of the file you want to create
createF(FILENAME)

# This function deletes all lines of the file. FILENAME - the name of the file
deleteAllFLines(FILENAME)

# Creates an array that cannot be used.
createArray(ARRAY)

# Makes a string uppercase.
Upper(STRING)

# Makes a string lowercase.
Lower(STRING)

# Returns the element
Return(returnWhat)

# Creates a copy of the file (.txt, .py). FILENAME - file name. NUMBERvalue is the number of file copies. (For example FileDuplicate("MyFile.txt", 2))
FileDuplicate(FILENAME, NUMBERvalue)

# Makes to string.
toStr(WHAT)

# Makes to int.
toInt(WHAT)

# Makes to float.
toFloat(WHAT)

# This function makes a time delay.
TimeToSleep(TIME)

# Loading animation.
LoadingAnimation()

# Text writing animation
WritingAnimation(TEXT)

# Rounding a number
Round(NUMBER)

# Floor the number
Floor(NUMBER)

# Ceil the number
Ceil(NUMBER)

# Enumerate writes the index and value that the list has. whatToEnum - list
Enumerate(whatToEnum)

# List length.
ListLength(LIST)

# This function from string makes to computer encoding.
computerSymbol(STRING)

# This function raises 2 numbers to the degree
toDegree(FIRST, SECOND)

# This thing works with dict. SortDict does everything in sequence.
SortDict(DICT)

# Finds out the sum of all numbers. For example summ([2, 5, 2])
summ(valuesL)

# Finds out the difference of all numbers. For example subtraction([16, 10, 2])
subtraction(valuesL)

# Finds out the product of all numbers. For example multiple([2, 5, 2])
multiple(valuesL)

# Finds out the quotient of all numbers. For example division([16, 2, 4, 2])
division(valuesL)

# Pi number
NumberOfPi()

# Euler's Number
EulersNumber()

# Exponents
Exponents(NUMBER)

# Square root
SquareRoot(NUMBER)

# IsPathExist - returns True or False.
IsPathExist(PATH)

# Create dirictory
CreateDirictory(PATH)

# Delete dicrectory
DeleteDicrectory(PATH)

# Delete directory file
DeleteDirectoryFile(PATH)

# Get file size
GetFileSize(PATH)

# File rename
FileRename(OLDNAME, NEWNAME)

# Lists which files are in the directory
FolderFilesList(PATH)

# Is in string letter
isInStringLetter(STRING):

# Is in string number
isInStringNumber(STRING):

# is in string number or letter
isInStringNumberOrLetter(STRING)

# Displays a random number. START - start number. END - finile number. STEP - the step with what will be the random
RandomNumber(START, STOP, STEP)

# Now let's move on to the PROGame class (it uses the pygame library)
# To install the pygame you need to write pip install pygame in the command line
# Now there will be an explanation for all the files and also the code

from PROPython import *

window = PROGame() # We will using PROGame class

# Window
window.Window(width=500, height=500, window_name="PROGame window") # Creating window
window.fill(color=(23, 56, 77)) # Fill your window
window.icon(path="My_Icon.png") # Instead My_Icon.png you need place your path to the icon image (.png, .jpg and others)

# Drawing
window.draw_cube(color=(255, 0, 0), pos_x=50, pos_y=52, width=10, height=23) # Drawing cube
window.draw_circle(color=(123, 76, 32), pos_x=50, pos_y=52, width=10, height=10) # Drawing circle
window.draw_line(color=(99, 44, 77), pos_x1=10, pos_y1=10, pos_x2=20, pos_y2=20, width=3) # Drawing line
window.draw_polygon(color=(23, 23, 45), pos_x1=100, pos_y1=120, pos_x2=110, pos_y2=130, pos_x3=130, pos_y3=145, pos_x4=150, pos_y4=150) # Drawing polygon

# Sounds
window.play_sound(path="my_sound.mp3") # Instead my_sound.mp3 you need place your path to the sound

# Functions
def my_func_with_no_brackets():
	cmd("Hello button")
	window.clear() # Clear all staff (buttons, text_boxes)
	cmd(window.get_TextBoxs_text()) # It gets all text boxes text!

# UI
window.create_text(text="My text", font=None, size=24, color=(255, 255, 255), pos_x=234, pos_y=234, smoothing=True) # Creating text
window.create_image(path="My_Image.png", pos_x=300, pos_y=300) # Instead My_Image.png you need place your path to the image (.png, .jpg and others)
window.create_button(active_color=(0, 0, 0), inactive_color=(0, 10, 0), width=100, height=25, x=400, y=400, text="My Button", size=25, font=None, text_color=(10, 10, 10), outline=None, command=my_func_with_no_brackets) # When you call function you have not have brackets!
window.create_text_box(width=100, height=25, x=450, y=450, active_color=(0, 255, 0), inactive_color=(255, 0, 0), border_width=2, text_color=(255, 255, 255), font=None, size=25, max_chars=30) # Creating text box

# Other
window.create_player(x=60, y=60, speed=2, image="path_to_image/my_img.png", control_type = 2) # Replace path_to_image/my_img.png to path and write "/" and your image name and (.png, .jpg and others)


window.Show(FPS=60, debug_mode=False) # Show all


# Now we will create Network! (It working on localhost)
# OK. Create new file and name it "server.py" or "s.py" or "_server.py"
# And write that
from PROPython.server import *
from PROPython.Objects import Player

server = Server(port=9999, max_connections=2, players_server=True, players_instance=[Player(x=50, y=100, speed=2, img="player.png", control_type=2), Player(x=50, y=100, speed=2, img="player.png", control_type=2)]) # Creating server
server.start() # Starting server

# And then in our main script or what you called we will write this

from PROPython import *

window = PROGame() # We will using PROGame class

# Window
window.Window(width=500, height=500, window_name="PROGame window") # Creating window
window.fill(color=(23, 56, 77)) # Fill your window
window.icon(path="My_Icon.png") # Instead My_Icon.png you need place your path to the icon image (.png, .jpg and others)

# Drawing
window.draw_cube(color=(255, 0, 0), pos_x=50, pos_y=52, width=10, height=23) # Drawing cube
window.draw_circle(color=(123, 76, 32), pos_x=50, pos_y=52, width=10, height=10) # Drawing circle
window.draw_line(color=(99, 44, 77), pos_x1=10, pos_y1=10, pos_x2=20, pos_y2=20, width=3) # Drawing line
window.draw_polygon(color=(23, 23, 45), pos_x1=100, pos_y1=120, pos_x2=110, pos_y2=130, pos_x3=130, pos_y3=145, pos_x4=150, pos_y4=150) # Drawing polygon

# Sounds
window.play_sound(path="my_sound.mp3") # Instead my_sound.mp3 you need place your path to the sound

# Functions
def my_func_with_no_brackets():
	cmd("Hello button")
	window.clear() # Clear all staff (buttons, text_boxes)
	cmd(window.get_TextBoxs_text()) # It gets all text boxes text!
	window.create_network() # Creating network

# UI
window.create_text(text="My text", font=None, size=24, color=(255, 255, 255), pos_x=234, pos_y=234, smoothing=True) # Creating text
window.create_image(path="My_Image.png", pos_x=300, pos_y=300) # Instead My_Image.png you need place your path to the image (.png, .jpg and others)
window.create_button(active_color=(0, 0, 0), inactive_color=(0, 10, 0), width=100, height=25, x=400, y=400, text="My Button", size=25, font=None, text_color=(10, 10, 10), outline=None, command=my_func_with_no_brackets) # When you call function you have not have brackets!
window.create_text_box(width=100, height=25, x=450, y=450, active_color=(0, 255, 0), inactive_color=(255, 0, 0), border_width=2, text_color=(255, 255, 255), font=None, size=25, max_chars=30) # Creating text box

# Other
window.create_player(x=60, y=60, speed=2, image="path_to_image/my_img.png", control_type = 2) # Replace path_to_image/my_img.png to path and write "/" and your image name and (.png, .jpg and others)


window.Show(FPS=60, debug_mode=False) # Show all

# Now in console we will first run server.py (or what you called the server script)

python server.py

# And we open new console and write "python main.py" (or "python m.py" or what you called)

python main.py

# And that is all!

# Game2D Studios
# PROPython
# PROGame
# Sockets
# 2021 version