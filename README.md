# CIS245-Assignment10-File_Processing
 
#program works with user input for file processing

import os #import the os library
#These are the inputs of data to be put into the file
input('Name: ')  
input('address: ')
input('phone_number: ')

filePath = input('Enter a file dir: ')  #user input for file dir
fileName = input('Enter a file name: ') #user input for file name
completePath = filePath + fileName  #complete path to file

#This opens or creates a file to write the data to underneath from user input
with open(completePath, 'w') as fileHandle:
	print('{Name},{address},{phone_number}')

#This opens and reads the data inputed by user in the file
with open(completePath, 'r') as fileHandle:
	data = fileHandle.read()
	print(data)
