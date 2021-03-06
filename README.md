<div align="center">
  <img height="60" src="https://user-images.githubusercontent.com/85709371/156916372-d8c1bbdd-5fe9-40d1-a250-5a1d4d454832.png">
  <img height="60" src="https://user-images.githubusercontent.com/85709371/156917513-f9f77e0b-03d2-41f9-b4ec-2dd92985547b.png">
</div>

# How to create Login Form using Python Tkinter?

### Contents:
1. Introduction
2. Example 1: Login Form using Python Tkinter
3. Summary

### Python Tkinter – Login Form
Login Form is one of the most used in GUI applications. Login Form helps users to login using user name and password. Once the credentials are validated, user can be given privileged access.

_**Example 1: Login Form using Python Tkinter**_

In this example, we write a program that opens a window with fields: username and password and a button to submit these values.

User can enter the details for username, password; and click on Login button.Once the button is clicked, a function is called to validate the credentials. Here, in this function, you have to write your business logic to validate the username and password.

For this example, in the credential validating function, we get the username and password entered by the user, and print it to the console.

### Prerequisites
- `Python 3`
- `Jupyter Notebook`
- `Tkinter`

## Python Program🧑🏻‍💻
```python
from tkinter import *
from functools import partial


def user_credential(username, password):
    print("username entered :", username.get())
    print("password entered :", password.get())

#window

tkWindow = Tk()
tkWindow.title("Login Form")
tkWindow.geometry("300x250")


#Creating layout of login form

Label(tkWindow, text="Please enter details below", width="300", bg="orange",fg="white").pack()

#username label and text entry box

usernameLabel = Label(tkWindow, text="Username *").place(x=20,y=40)
username = StringVar()
usernameEntry = Entry(tkWindow, textvariable=username).place(x=90,y=42)  

#password label and password entry box

passwordLabel = Label(tkWindow,text="Password *").place(x=20,y=80)  
password = StringVar()
passwordEntry = Entry(tkWindow, textvariable=password, show='*').place(x=90,y=82)  

user_credential = partial(user_credential, username, password)

#login button

loginButton = Button(tkWindow, text="Login", width=10, height=1, bg="orange", command=user_credential).place(x=105,y=130)  

tkWindow.mainloop()
```

## Output:

Following video demonstrates the output and usage of above Python program.

![Screenshot (147)](https://user-images.githubusercontent.com/85709371/147056687-d95000f2-2b88-4c91-bd46-5c1f57de9045.png)

`Note:` I have used Entry(.., show='*') for password, to show stars when user types the password.

## *Author Name*
[Vikrant](https://github.com/thevkrant)
