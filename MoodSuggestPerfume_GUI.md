# Experiment to the Perfume Suggestions on Basis of Human Mood.

## Import Libraries


```python

import warnings

warnings.filterwarnings('ignore')

```

## Import Tkinter module 


```python

from tkinter import * 

from tkinter.ttk import *

```

# Experiment using Graphical User Interface (GUI) 

## Defining a Python function to Suggest


```python

def sel():
    
    selection = "You have to try " + str(v.get())
    
    label.config(text = selection)
    
```


## Creating parent Tkinter window 


```python

win = Tk() 

```

## Setting Title of window


```python

win.title("Mood Suggestion Perfume")

```




    ''



## Setting Background of window


```python

win.configure(background='#d2ffd2')

```


## Setting dimesntions of window


```python

window_height = 475

window_width = 470

screen_width = win.winfo_screenwidth()

screen_height = win.winfo_screenheight()

x_cordinate = int((screen_width/2) - (window_width/2))

y_cordinate = int((screen_height/2) - (window_height/2))

win.geometry("{}x{}+{}+{}".format(window_width,window_height, x_cordinate, y_cordinate))

```




    ''



## Setting Window style


```python

style = Style(win) 

style.configure("TRadiobutton", background = "#d2ffd2", foreground = "black", font = ("Helvetica", 14, "bold"))

```

# Requirnments to Suggest Mood


```python

options = {
           'Happy' : 'Dolce & Gabanna Light Blue',
           
           'Sad': 'Issey Miyake Leu de Issey',
           
           'Sexy' : 'Roberto Cavalli Gemma di Paradiso',
           
           'Lazy' : 'Guerlain Mon Guerlain',
           
           'Energetic' : 'YSL Libre',
           
           'Flirty' : 'YSL Mon Paris',
           
           'Bossy' : 'Burberry My Burberry Black',
           
           'Naughty' : 'Versace Crystal Noir',
           
           'Angelic' : 'Amouage Honour',
           
           'Beautiful' : 'Guerlain Mon Guerlain'
           }

```

## Making output Suggest label on window


```python

label = Label(win,text='How is Your Mood?',background = "#d2ffd2", foreground = "black",font=("Helvetica", 15,"bold"))

label.pack(side = TOP, ipady = 5)

label = Label(win,background = "#d2ffd2", foreground = "black",font=("Helvetica", 15,"bold"))

```

### We will use a Loop just to create multiple Radiobuttons instaed of creating each button separately


```python

v = StringVar(win, "1") 

for (txt, val) in options.items(): 
    
    Radiobutton(win, text=txt, variable=v, value=val,command=sel).pack(side = TOP, ipady = 5) 
    
label.pack(side = TOP, ipady = 5)

```

# Running complete program


```python

mainloop() 

```

## Output Samples


```python

from IPython.display import Image, display

x = Image(filename='png1.jpg')

y = Image(filename='png2.jpg')

z = Image(filename='png3.jpg')

display(x, y, z)

```


    
![jpeg](output_27_0.jpg)
    



    
![jpeg](output_27_1.jpg)
    



    
![jpeg](output_27_2.jpg)
    


# End here
