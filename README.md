# Quiz-creator
Creates a functioning quiz 
# Ivan Salazar
# 7/27/22
# Quiz that askes the user multiple choice questions, three choices. Gives freedback on whether it is correct or incorrec




# Created the frames for the gui interface
y=0
from tkinter import * #importing the library
from tkinter import *
from tkinter import ttk
n= ttk.Notebook()
f1= ttk.Frame(n)#creating an instance of window 
f2= ttk.Frame(n)
f3= ttk.Frame(n)
f4= ttk.Frame(n)
f5= ttk.Frame(n)
f6= ttk.Frame(n)

window= ttk.Frame(n)

    



# Defines the main function for the quiz
def main(x):
    global total
    n.add(f1, text="One")
    n.add(f2, text="Two")
    n.add(f3, text="Three")
    n.add(f4, text="Four")
    n.add(f5, text="Five")
    n.add(f6, text="Six")
   
    

    total= ttk.Label(window, text="0")#label of window 


# The label and buttons for the first question and command for which is the right answer
    Label(f1, text="What is Tkinter?").grid(row=2,column=2)
    Button(f1, text="Guided User Interface", command=correct).grid(row=3,column=1)
    Button(f1, text="Variable", command=incorrect).grid(row=3,column=2)
    Button(f1, text="Function", command=incorrect).grid(row=3,column=3)

# Label and buttons for the second question,  along with correct answer command

    Label(f2, text="What is a Variable?").grid(row=2,column=2)
    Button(f2, text=" A value that stays the same",command=incorrect2).grid(row=3,column=1)
    Button(f2, text="A value that can be changed", command=correct2).grid(row=3,column=2)
    Button(f2, text="Neither", command=incorrect2).grid(row=3,column=3)

# Label and buttons for the third question, along with correct answer command
    Label(f3, text="What does the 'Print' command do?").grid(row=2,column=2)
    Button(f3, text="Create a window",command=incorrect3).grid(row=3,column=1)
    Button(f3, text="Show a message", command=correct3).grid(row=3,column=2)
    Button(f3, text="Print to the printer", command=incorrect3).grid(row=3,column=3)
    
# Label and buttons for the third question, along with correct answer command
    Label(f4, text="What is the moniter?").grid(row=2,column=2)
    Button(f4, text="A display that shows what the computer is doing",command=correct4).grid(row=3,column=1)
    Button(f4, text="A circut board", command=incorrect4).grid(row=3,column=2)
    Button(f4, text="A Program", command=incorrect4).grid(row=3,column=3)

# Label and buttons for the third question, along with correct answer command
    Label(f5, text="What does the 'from ____ import' command do?").grid(row=2,column=2)
    Button(f5, text="Import an image",command=incorrect5).grid(row=3,column=1)
    Button(f5, text="Import text", command=incorrect5).grid(row=3,column=2)
    Button(f5, text="Import a module", command=correct5).grid(row=3,column=3)

# Label and buttons for the third question, along with correct answer command
    Label(f6, text="Which of these is a Boolean Value?").grid(row=2,column=2)
    Button(f6, text="Enter",command=incorrect6).grid(row=3,column=1)
    Button(f6, text="Esc", command=incorrect6).grid(row=3,column=2)
    Button(f6, text="True", command=correct6).grid(row=3,column=3)
    Button(f6, text= "Quit quiz",command=close).grid(row=3,column=4)


 #Returns correct or incorrects if the selected option matches  
    return total

# Correct and incorrect definition match ups

def correct():
    global total
    Label(f1, text="Correct").grid(row=1,column=2)#Defines answer as correct or incorrect and exact place 
    counter()
def incorrect():
    Label(f1, text="Incorrect").grid(row=1,column=2)#Defines answer as correct or incorrect and exact place 

def correct2():
    global total
    Label(f2, text="Correct").grid(row=1,column=2)#Defines answer as correct or incorrect and exact place 
    counter()

def incorrect2():
    Label(f2, text="Incorrect").grid(row=1,column=2)#Defines answer as correct or incorrect and exact place 

def correct3():
    global total
    Label(f3, text="Correct").grid(row=1,column=2)#Defines answer as correct or incorrect and exact place 
    counter()

def incorrect3():
    Label(f3, text="Incorrect").grid(row=1,column=2)#Defines answer as correct or incorrect and exact place 

def correct4():
    global total
    Label(f4, text="Correct").grid(row=1,column=2)
    counter()

def incorrect4():
    Label(f4, text="Incorrect").grid(row=1,column=2)

def correct5():
    global total
    Label(f5, text="Correct").grid(row=1,column=2)
    counter()

def incorrect5():
    Label(f5, text="Incorrect").grid(row=1,column=2)

def correct6():
    global total
    Label(f6, text="Correct").grid(row=1,column=2)
    counter()

def incorrect6():
    Label(f6, text="Incorrect").grid(row=1,column=2)




def counter():
    global total
    total['text'] = str(int(total['text']) + 1)
def close(): # closes "Destroys" the quiz when button is pressed
   n.destroy()
   





main(y)# calls main funcion



n.pack()

n.mainloop()

