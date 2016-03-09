#!/usr/bin/python

from Tkinter import *

def sel():
   selection = "Value = " + str(var.get())
   label.config(text = selection)
   canvas = Canvas( bg="white", height=250, width=300, relief = GROOVE, bd = 2 )
   canvas.pack (side = BOTTOM)
   coord = 10, 50, 240, 210
   arc = canvas.create_arc(coord, start=20, extent = str(var.get()), fill="yellow" )



root = Tk()
var = DoubleVar()
scale = Scale( root, variable = var, font = ("bold",20), sliderlength = 10, orient = HORIZONTAL, showvalue = 0, label = "move" )
scale.pack (side = TOP)

button = Button(root, text="Determine number of the slider", bg="blue", fg="green", width = 30, command=sel, height = 25)
button.pack (side = TOP)


label = Label(root,relief=SUNKEN, width = 20, height = 10, bg = "red", underline = 0)
label.pack()

label2 = Message( root, text = "Here is a yellow graph based on the number shown", relief=RAISED, fg = "blue", bg = "orange", width = 30 )
label2.pack ()


root.mainloop() 
