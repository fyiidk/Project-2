# Project-2
#This project 2 for programming tech.
# Make a Tntro
import sys
from tkinter import *
import tkinter as tk
# Create window for the program
# Insert Title for the program
# import Tkinter as tk
#define functions
usd= IntVar()
cad= IntVar()
def calculate1():
    try:
        value = float(usd.get())
        cad.set(value * 1.33)
    except ValueError:
        pass
#Import tkinter, establish window size and title.
Pro_2 = Tk()
Pro_2.geometry("600x400+200+200")
Pro_2.title('Currency Converter')

# Make the heading
msg_1= "Welcome to Currency Converter."
msg_2= "Convert from US Dollars to Canadian Dollars."
usd_3= "USD"
cad_4= "CAD"
msg_3= "is equivalent to"
#Make the labels
Label(Pro_2,text= msg_1, bg='#FFFFAA', font='Times 16').grid(row = 0, column = 0, sticky = W)
Label(Pro_2,text= msg_2,font='Times 12').grid(row = 3, column = 0, sticky = W)
Label(Pro_2,text= usd_3,font='Times 12').grid(row = 4, column = 2, sticky = W)
Label(Pro_2,text= msg_3,font='Times 12').grid(row = 5, column = 1, sticky = W)
Label(Pro_2,text= cad_4,font='Times 12').grid(row = 5, column = 2, sticky = W)
Label(Pro_2,text= cad,font='Times 12').grid(row = 5, column = 1, sticky = W)

#Make an entry
usd_entry= Entry(Pro_2,width=7,textvariable=usd)
usd_entry.grid(column = 1, row = 4, sticky = W)

#Make an button
Button(Pro_2, text="Calculate", command=calculate1).grid(column=1, row=11, sticky=W)
usd_entry.focus()
usd_entry.bind('<Return>', calculate1)
Pro_2.mainloop()

