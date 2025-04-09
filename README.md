# Tkinter Widget Examples

This project demonstrates the usage of various Tkinter widgets, including labels, buttons, entries, textboxes, spinboxes, scales, checkbuttons, radiobuttons, and listboxes. When you run the program, you will see various widgets like labels, buttons, entries, and more. These widgets are interactive, and you can perform actions like entering text, selecting options, and interacting with the UI elements.

## Code Explanation

### 1. **Creating the Window**
   ```python
   window = Tk()
   window.title("Widget Examples")
   window.minsize(width=500, height=500)
   ```
   - **Explanation:** A Tkinter window is created and configured with a title ("Widget Examples") and a minimum size of 500x500 pixels.

### 2. **Labels**
   ```python
   label = Label(text="This is old text")
   label.config(text="This is new text")
   label.pack()
   ```
   - **Explanation:** A `Label` widget is created with the initial text "This is old text". The text is updated to "This is new text" using the `config` method. The label is added to the window using the `pack` method.

### 3. **Buttons**
   ```python
   def action():
     print("Do something")

   button = Button(text="Click Me", command=action)
   button.pack()
   ```
   - **Explanation:** A `Button` widget is created with the text "Click Me". When the button is clicked, it triggers the `action()` function, which prints "Do something". The button is added to the window using the `pack` method.

### 4. **Entries**
   ```python
   entry = Entry(width=30)
   entry.insert(END, string="Some text to begin with.")
   print(entry.get())
   entry.pack()
   ```
   - **Explanation:** An `Entry` widget is created with a width of 30 characters. It is pre-filled with the text "Some text to begin with". The `get()` method is used to retrieve the text entered by the user. The entry is then added to the window using the `pack` method.

### 5. **Textboxes**
   ```python
   text = Text(height=5, width=30)
   text.focus()
   text.insert(END, "Example of multi-line text entry.")
   print(text.get("1.0", END))
   text.pack()
   ```
   - **Explanation:** A `Text` widget is created with a height of 5 lines and a width of 30 characters. The `focus()` method places the cursor in the textbox. The `insert()` method is used to pre-fill the textbox with the text "Example of multi-line text entry.". The `get("1.0", END)` method retrieves the content of the textbox. The text widget is added to the window using the `pack` method.

### 6. **Spinbox**
   ```python
   def spinbox_used():
     print(spinbox.get())

   spinbox = Spinbox(from_=0, to=10, width=5, command=spinbox_used)
   spinbox.pack()
   ```
   - **Explanation:** A `Spinbox` widget is created with a range of values from 0 to 10. The `get()` method is used to retrieve the selected value. The command argument is used to call the `spinbox_used()` function when the value in the spinbox changes. The spinbox is added to the window using the `pack` method.

### 7. **Scale**
   ```python
   def scale_used(value):
     print(value)

   scale = Scale(from_=0, to=100, command=scale_used)
   scale.pack()
   ```
   - **Explanation:** A `Scale` widget is created with a range of values from 0 to 100. The `command` argument is used to call the `scale_used()` function when the value of the scale changes. The `scale_used()` function prints the current value of the scale. The scale is added to the window using the `pack` method.

### 8. **Checkbutton**
   ```python
   def checkbutton_used():
     print(checked_state.get())

   checked_state = IntVar()
   checkbutton = Checkbutton(text="Is On?", variable=checked_state, command=checkbutton_used)
   checked_state.get()
   checkbutton.pack()
   ```
   - **Explanation:** A `Checkbutton` widget is created with the text "Is On?". It is linked to an `IntVar` variable (`checked_state`), which stores the state of the checkbox. When the state changes, the `checkbutton_used()` function is called, which prints the state (1 for checked, 0 for unchecked). The checkbox is added to the window using the `pack` method.

### 9. **Radiobutton**
   ```python
   def radio_used():
     print(radio_state.get())

   radio_state = IntVar()
   radiobutton1 = Radiobutton(text="Option1", value=1, variable=radio_state, command=radio_used)
   radiobutton2 = Radiobutton(text="Option2", value=2, variable=radio_state, command=radio_used)
   radiobutton1.pack()
   radiobutton2.pack()
   ```
   - **Explanation:** A `Radiobutton` widget is created with two options ("Option1" and "Option2"). The `IntVar` variable `radio_state` is used to store the selected option. The `command` argument calls the `radio_used()` function when the selected option changes. The current selected value is printed using `radio_state.get()`. Both radiobuttons are added to the window using the `pack` method.

### 10. **Listbox**
   ```python
   def listbox_used(event):
     print(listbox.get(listbox.curselection()))

   listbox = Listbox(height=4)
   fruits = ["Apple", "Pear", "Orange", "Banana"]
   for item in fruits:
     listbox.insert(fruits.index(item), item)

   listbox.bind("<<ListboxSelect>>", listbox_used)
   listbox.pack()
   ```
   - **Explanation:** A `Listbox` widget is created with a height of 4. A list of fruits is inserted into the listbox. The `bind()` method is used to bind the event `<<ListboxSelect>>`, which is triggered when an item is selected in the listbox. The `listbox_used()` function retrieves and prints the selected item using `listbox.curselection()`. The listbox is added to the window using the `pack` method.

## Installation

To run this project, you need to have Python and Tkinter installed on your machine.

1. Clone this repository:
   ```bash
   git clone https://github.com/ulquiorraexe/tkinter-widget-examples.git
2. Navigate to the project directory:
   ```bash
   cd tkinter-widget-examples
3. Install Tkinter (if nnot already installed):
   ```bash
   pip install tk
4. Run the program:
   ```bash
   python main.py

## Notes

- Make sure to run the program in a Python environment where Tkinter is installed.
- The widgets shown in this project are part of the Tkinter library, which is included in the standard Python installation.

## License

This project does not have a license.
