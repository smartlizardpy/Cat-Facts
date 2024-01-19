# Cat-Facts
This is a app made with Tkinter and Httplib2.This app was built using 
-
[Cat Facts API](https://catfact.ninja/)

You can use this snippet I made with the proper imports
```
import json
import httplib2
```
```
h = httplib2.Http()
resp, content = h.request("https://catfact.ninja/fact")
x = content
y = json.loads(x)
quote = y["fact"]

```

# With Tkinter
In this app i use tkinter.The snippet with a ``` def getFact():``` function and a button to change the text on the button press;

```
from tkinter import *
from tkinter import messagebox
import httplib2
import json
```
```
#for more go to:
#setup
root = Tk()
root.title = "Cat Facts"
root.geometry("400x100")
h = httplib2.Http()

T = Text(root, height=2, width=40)
S = Scrollbar(root)
T.config(yscrollcommand=S.set)
S.config(command=T.yview)
T.pack(side=LEFT, fill=Y)
S.pack(side=LEFT, fill=Y)



#function

def getFacts():
    resp, content = h.request("https://catfact.ninja/fact")
    # Some JSON:
    x = content
    # Parse x:
    y = json.loads(x)
    # The result is a Python dictionary:
    quote = y["fact"]

    T.delete(1.0, END)  # Clear the current text in the Text widget
    T.insert(END, quote)  # Insert the new quote into the Text widget

#button

B = Button(root, text="Fact", command=reload)
B.pack()

```
#How to use it.
-When you open the app you come a cross a text window, three buttons:Fact, Exit and Help.
*When you click fact it shows *obviously* the fact.
*when you click exit it  *obviously* exits the app
-When you click Help it comes to this part of the Readme file.


-By 0zan (a.k.a smartlizardpy)-
