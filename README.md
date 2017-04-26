# Tic-Tac-Toe-Steedley
#Gui
from tkinter import *

import tkinter.messagebox
tk = Tk()
tk.title("TIC TAC And The TOE")

click = True

def checker(buttons):
	global click
	if buttons["text"] == " " and click == True:
		buttons["text"] = "X"
		click = False
	elif buttons ["text"] == " " and click == False:
		buttons["text"] = "O"
		click = True

	elif(button1["text"] == "X" and button2["text"] == "X" and button3["text"] == "X" or
	     button4["text"] == "X" and button5["text"] == "X" and button6["text"] == "X" or
	     button7["text"] == "X" and button8["text"] == "X" and button9["text"] == "X" or
	     button3["text"] == "X" and button5["text"] == "X" and button7["text"] == "X" or
	     button1["text"] == "X" and button5["text"] == "X" and button9["text"] == "X" or
	     button1["text"] == "X" and button4["text"] == "X" and button7["text"] == "X" or
	     button2["text"] == "X" and button5["text"] == "X" and button8["text"] == "X" or
	     button3["text"] == "X" and button6["text"] == "X" and button9["text"] == "X" ):
	     tkinter.messagebox.showinfo("WINNER X", "YOU JUST WON!!!!")

	elif(button1["text"] == "O" and button2["text"] == "O" and button3["text"] == "O" or
	     button4["text"] == "O" and button5["text"] == "O" and button6["text"] == "O" or
	     button7["text"] == "O" and button8["text"] == "O" and button9["text"] == "O" or
	     button3["text"] == "O" and button5["text"] == "O" and button7["text"] == "O" or
	     button1["text"] == "O" and button5["text"] == "O" and button9["text"] == "O" or
	     button1["text"] == "O" and button4["text"] == "O" and button7["text"] == "O" or
	     button2["text"] == "O" and button5["text"] == "O" and button8["text"] == "O" or
	     button3["text"] == "O" and button6["text"] == "O" and button9["text"] == "O" ):
	     tkinter.messagebox.showinfo("WINNER O","YOU JUST WON!!!!!")

buttons=StringVar()

button1 = Button(tk , text=" ",font=('Times 20 bold'), height = 5, width = 9, command = lambda:checker(button1))
button1.grid(row = 1, column = 0, sticky = S+N+E+W)
button2 = Button(tk , text=" ",font=('Times 20 bold'), height = 5, width = 9, command = lambda:checker(button2))
button2.grid(row = 1, column = 1, sticky = S+N+E+W)
button3 = Button(tk , text=" ",font=('Times 20 bold'), height = 5, width = 9, command = lambda:checker(button3))
button3.grid(row = 1, column = 2, sticky = S+N+E+W)
button4 = Button(tk , text=" ",font=('Times 20 bold'), height = 5, width = 9, command = lambda:checker(button4))
button4.grid(row = 2, column = 0, sticky = S+N+E+W)
button5 = Button(tk , text=" ",font=('Times 20 bold'), height = 5, width = 9, command = lambda:checker(button5))
button5.grid(row = 2, column = 1, sticky = S+N+E+W)
button6 = Button(tk , text=" ",font=('Times 20 bold'), height = 5, width = 9, command = lambda:checker(button6))
button6.grid(row = 2, column = 2, sticky = S+N+E+W)
button7 = Button(tk , text=" ",font=('Times 20 bold'), height = 5, width = 9, command = lambda:checker(button7))
button7.grid(row = 3, column = 0, sticky = S+N+E+W)
button8 = Button(tk , text=" ",font=('Times 20 bold'), height = 5, width = 9, command = lambda:checker(button8))
button8.grid(row = 3, column = 1, sticky = S+N+E+W)
button9 = Button(tk , text=" ",font=('Times 20 bold'), height = 5, width = 9, command = lambda:checker(button9))
button9.grid(row = 3, column = 2, sticky = S+N+E+W)

tk.mainloop()


#1: Use the code from tkinter import*
   # - The tkinter module contains the tk toolkit

#2: Use the code import tkinter.messagebox
   # - This simply opens a meesage box with whatever you code into it

#3: Next you have to create a tk = Tk() root widget
    #- Which is a window with a little bar and other decoration provided by the window manager. The root widget has to be created before #any other widgets and there can only be one root widget.

#4:Next make a name/title foryour game simply using tk.title("")
