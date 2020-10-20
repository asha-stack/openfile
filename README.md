# openfile
tkinter (Gui App)

import tkinter as tk
from tkinter import filedialog
import os

root = tk.Tk()

def addApp():
    filename= filedialog.askopenfilename(initialdir="/", title="Select File", 
    filetypes=(("executables","*.exe"), ("all files", "*.*")))


canvas = tk.Canvas(root, heigh=700, width=700, bg='#263D42')
canvas.pack()

# centering the frame widget
frame= tk.Frame(root, bg="white")
frame.place(relwidth=0.8, relheight=0.8, 
                     relx=0.1, rely=0.1) 

OpenFile= tk.Button(root, text='Open File', padx=10, pady=5, fg='white', bg='#263D42', command= addApp)
OpenFile.pack()

root.mainloop()
