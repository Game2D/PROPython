#================#
#                #
#   PROPython    #
#				 #
#================#
#				 #
# VERSION: 1.0.0 #
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

# Finds out the sum of all numbers. For sample summ([2, 5, 2])
summ(valuesL)

# Finds out the difference of all numbers. For sample subtraction([16, 10, 2])
subtraction(valuesL)

# Finds out the product of all numbers. For sample multiple([2, 5, 2])
multiple(valuesL)

# Finds out the quotient of all numbers. For sample division([16, 2, 4, 2])
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
