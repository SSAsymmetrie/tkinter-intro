#!/usr/bin/python
from Tkinter import *

def sel():
   selection = "Value = " + str(var.get())
   label.config(text = selection)

root = Tk()
var = DoubleVar()
scale = Scale( root, variable = var, font = ("bold",60), sliderlength = 50, orient = HORIZONTAL, showvalue = 0 )
scale.pack (anchor = CENTER)

button = Button(root, text="Determine number", bg="blue", fg="green", width = 30, command=sel)
button.pack (anchor = CENTER)

text = Text(root,)
text.insert(INSERT, "Good morning")

label = Label(root,relief=FLAT, width = 400)
label.pack()

root.mainloop()
