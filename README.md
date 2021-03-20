# PROPython version 1.0.7

# Classes

Terminal()

Language()

Debug()

Time()

Base()

Dict()

List()

Math()

File()

PROGame()

# Class Terminal

	from PROPython import Terminal

	success = False

	terminal = Terminal() # Creating terminal

	print(terminal.get_args()) # Get what user entered

	if terminal.get_args = ['run']: # If user entered run
		print("Running") 
		success = True

	if success == False: # If not successs
		print("Avalible args:\n run")

# Now write in console this

	python my_app.py run
	
# And we see what is hatched

	Running
	
# If we write something else

	python my_app.py stop
	
# And we see what is hatched

	Avalible args:
	run


# Language

	from PROPython import Language

	lang = Language()
	
	lang.en() # English
	lang.ru() # Russian
	
# We will add more languages in new updates
	

# Debug

	from PROPython import Debug
	
	debug = Debug()
	
	debug.log("Hello, world!", sep=' ', end='?', file=None) # Work's like print
	
	debug.cmd(msg="Hello, world!") # Have 1 argument "msg"


# Time

	from PROPython import Time
	
	time = Time()
	
	time.delay(seconds=2) # Makes a delay


# Base

	from PROPython import Base
	
	base = Base()
	
	base.loading_animation() # Print loading animation in console
	
	base.writing_animation(text="my writing text!") # Write text
	
	base.__return__(object=[10, "67", "Hello"]) # Return's something
	

# Dict

	from PROPython import Dict
	
	dict = Dict()
	
	my_dict = {"HELLO":1, "A":9, "B":0, "V":5}
	
	dict.sort(dict=my_dict) # Sorting dict


# List

	from PROPython import List
	
	my_list = ["10", 10, "YAP"]
	
	list = List()
	
	list.enum(list=my_list) # Enumerate list
	
	print(lis.length(list=my_list)) # Returns list length
	
	
# Str

	from PROPython import Str
	
	_str = Str()
	
	string1 = "abcdefg123456"
	string2 = "abcd"
	letter = "a"
	
	_str.has_number_or_letter(string1) # Returns True
	_str.has_number(string2) # Returns False
	_str.has_letter(string2) # Returns True
	
	_str.computer_symbol(letter) # Returns computer symbol of letter
	string1 = _str.upper(string1) # Make string upper case
	string1 = _str.lower(string1) # Make string lower case
	
	
# Directory
	
	from PROPython import Directory
	
	directory = Directory()
	
	directory.create(path="my_directory_name") # Creates directory
	
	directory.delete(path="my_directory") # Deletes directory
	
	print(directory.files_list(path="my_directory_name")) # Returns what in directory
	
	print(directory.is_exists(path="my_directory")) # Returns True or False (In this case it will be return False)
	
	
# Math

	from PROPython import Math
	
	math = Math()
	
	print(math.pi) # Returns pi number
	print(math.euler_num) # Returns euler's number
	
	rand = math.random(start=1, stop=100, step=2) # Random number
	
	print(math.round(number=3.9))
	
	print(math.floor(number=3.9))
	
	print(math.ceil(number=3.9))
	
	print(math.exponents(number=9.5))
	
	print(math.square_root(number=3))
	
	print(math.sum([9, 2, 23.4])) # +
	
	print(math.difference([50, 40, -10, 2, 9.3])) # -
	
	print(math.composition([2, 5, -1, 0.5])) # *
	
	print(math.quotient([50, 5, 2, 2.3])) # /
	
	print(math.binary(number=9))
	
	print(math.degree(first=2, second=2))
	
	
# File

	from PROPython import File
	
	file = File(path="PROPython.txt")
	
	file.write("Some text")
	
	file.add("Some text2")
	
	file_read = file.read()
	file_size = file.size()
	
	file.rename("PROPython_List.txt")
	
	file.duplicate(value=1) # value - copy number
	
	file.clear_lines()
	
	file.write("> Hello, world!")
	
	file.close()
	
	file.delete()
	
# Now let's move on to the PROGame class (it uses the pygame library)
# To install the pygame you need to write "pip install pygame" in the command line
# Now there will be an explanation for all the files and also the code
	
	import pygame
	from PROPython import *
	from PROPython.keys import *

	window = PROGame() # We will using PROGame class

# Window
	# Creating window
	window.Application(width=500, height=500, window_name="PROGame window")

	# Fill your window
	window.fill(color=(23, 56, 77))

	# Icon
	# Instead My_Icon.png you need place your path to the icon image (.png, .jpg and others)
	window.icon(path="My_Icon.png")

# Drawing
	# Drawing cube
	window.draw_cube(color=(255, 0, 0), pos_x=50, pos_y=52, width=10, height=23)

	# Drawing circle
	window.draw_circle(color=(123, 76, 32), pos_x=50, pos_y=52, width=10, height=10)

	# Drawing line
	window.draw_line(color=(99, 44, 77), pos_x1=10, pos_y1=10, pos_x2=20, pos_y2=20, width=3)

	# Drawing polygon
	window.draw_polygon(color=(23, 23, 45), pos_x1=100, pos_y1=120, pos_x2=110, pos_y2=130, pos_x3=130, pos_y3=145, pos_x4=150, 		pos_y4=150)

# Sounds
	#Instead my_sound.mp3 you need place your path to the sound
	window.play_sound(path="my_sound.mp3")

# Functions
	def my_func_with_no_brackets():
		cmd("Hello button")

		# Clear all staff (buttons, text_boxes)
		window.clear()

		# It gets all text boxes text!
		cmd(window.get_TextBoxs_text()) 
# UI
	# Creating text
	window.create_text(text="My text", font=None, size=24, color=(255, 255, 255), pos_x=234, pos_y=234, smoothing=True)

	# Creating image
	Instead My_Image.png you need place your path to the image (.png, .jpg and others)
	window.create_image(path="My_Image.png", pos_x=300, pos_y=300)

	
	# When you call function you have not have brackets!
	window.create_button(active_color=(0, 0, 0), inactive_color=(0, 10, 0), width=100, height=25, x=400, y=400, text="My Button", size=25, font=None, text_color=(10, 10, 10), outline=None, command=my_func_with_no_brackets)

	# Creating text box
	window.create_text_box(width=100, height=25, x=450, y=450, active_color=(0, 255, 0), inactive_color=(255, 0, 0), 	border_width=2, text_color=(255, 255, 255), font=None, size=25, max_chars=30)

# Other
	# Player
	# Replace path_to_image/my_img.png to path and write "/" and your image name and (.png, .jpg and others)
	window.create_player(x=60, y=60, speed=2, image="path_to_image/my_img.png", control_type = 2)

# Particle System
	window.particle_system(x=50, y=50, speed=3, radius=10, color=(234, 56, 12))

# Show all
	# Main loop
	while window.run:
		# If "w" key pressed	
		if is_key_pressed(pygame.K_w): # It works with pygame
			window.run_particle_system() # Running particle system
			print("Yeah!")
			
		window.show(FPS=60, debug_mode=False)

# Now we will create Network! (It working on localhost)
# OK. Create new file and name it "server.py" or "s.py" or "_server.py"
# And write that
	
	from PROPython.server import * 
	from PROPython.Objects import Player

# Creating server
	server = Server(port=9999, max_connections=2, players_server=True, players_instance=[Player(x=50, y=100, speed=2, img="player.png", control_type=2), Player(x=50, y=100, speed=2, img="player.png", control_type=2)])
	
	server.start() # Starting server

# Now in console we will first run server.py (or what you called the server script)
	python server.py

# And we open new console and write "python main.py" (or "python m.py" or what you called)
	python main.py
	
# And in other console we need to write same
	python main.py

# Sockets
# Pygame
# PROPython
# PROGame
# © Game2D Studio
