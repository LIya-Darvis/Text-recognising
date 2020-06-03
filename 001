##---------------------------------------##
# Creating main window using TKinter
##---------------------------------------##

from tkinter import *   # import the whole module

from PIL import Image
import pytesseract
import cv2
import os


root = Tk()

myLabel0 = Label(root, text="\nВставьте ссылку на изображение\n")
myLabel0.pack()


##---------------------------------------##
# Download image using requests
##---------------------------------------##


# create custom string
e = Entry(root, width=50, borderwidth=8)
e.pack()

def myDownload():
    from urllib.request import urlopen
    with open(r"c:\Users\Администратор\Desktop\CVN\Translator\images\full_image.png", 'wb') as img:
        img.write(urlopen(e.get()).read())


##---------------------------------------##
# Get text from image using PyTesseract
##---------------------------------------##


def myRecognise():

    import pytesseract as tess
    tess.pytesseract.tesseract_cmd = r'c:\Users\Администратор\Desktop\CVN\Tesseract\tesseract.exe'
    from PIL import Image

    img = Image.open(r"c:\Users\Администратор\Desktop\CVN\Translator\images\full_image.png")
    text = tess.image_to_string(img)

    print(text)

    mylabel2 = Label(root, text=text)
    mylabel2.pack()


##---------------------------------------##
# Deleting images using
##---------------------------------------##


def myDelete():
    import os
    os.remove(r"c:\Users\Администратор\Desktop\CVN\Translator\images\full_image.png")


##---------------------------------------##
# All in all
##---------------------------------------##


# create download button
myButton0 = Button(root, text="Скачать", command=myDownload)
myButton0.pack()

# create recognising button
myButton1 = Button(root, text="Распознать текст", command=myRecognise)
myButton1.pack()

# create delete button
myButton2 = Button(root, text="Удалить", command=myDelete)
myButton2.pack()



# this is the end of program
root.mainloop()
