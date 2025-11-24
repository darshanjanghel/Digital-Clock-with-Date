 🕰️ Simple Digital Clock with Tkinter

This is a straightforward Python script that creates a real-time digital clock using the `tkinter` library.

-----

### ⚙️ Requirements

  * **Python 3.x**
  * The **`tkinter`** library (usually included with standard Python installations).

-----

### 🚀 How to Run

1.  **Save the code:** Ensure the provided Python code is saved as a file named `practical.py`.

2.  **Run from the terminal:** Open your terminal or command prompt and execute the script:

    ```bash
    python practical.py
    ```

-----

### ✨ Features

  * Displays the **current time** and **date**.
  * The display updates every **1 second** in real-time.
  * Uses a simple GUI interface built with **Tkinter**.

-----

### 🎨 Customization: Changing Appearance

You can easily change the look of the clock by modifying the `label` definition in the `practical.py` file:

```python
label = tk.Label(root, font=('calibri', 50, 'bold'),
                 background='yellow', foreground='black')
```

| Property | Value Type | Description | Example Change |
| :--- | :--- | :--- | :--- |
| `font` | Tuple (Name, Size, Style) | Changes the typeface, size, and weight of the text. | `font=('consolas', 40, 'italic')` |
| `background` | Color Name or Hex Code | Sets the clock's background color. | `background='#000000'` (Black) |
| `foreground` | Color Name or Hex Code | Sets the color of the text (time/date). | `foreground='cyan'` |

-----

### 📅 Time Format Options

The time and date format is controlled by the `strftime` function within the `time()` function:

```python
def time():
    # Current format: HH:MM:SS AM/PM \n MM/DD/YY
    string = strftime('%H:%M:%S %p \n %D')
    label.config(text=string)
    label.after(1000, time)
```

Here are some common format codes you can use to adjust the `string` variable:

| Code | Output | Description |
| :--- | :--- | :--- |
| `%I` | 01 to 12 | Hour as a 12-hour number. |
| `%H` | 00 to 23 | Hour as a 24-hour number. |
| `%M` | 00 to 59 | Minute as a number. |
| `%S` | 00 to 59 | Second as a number. |
| `%p` | AM/PM | Locale's equivalent of AM or PM. |
| `%a` | Mon, Tue, etc. | Weekday as a short name. |
| `%B` | January, February, etc. | Month as a full name. |
| `%d` | 01 to 31 | Day of the month. |
| `%Y` | 2023, 2024, etc. | Year with century. |

#### **Example: Changing to 12-Hour Format with Full Date**

To change the script to display **12-hour time** and the **full date (Month Name, Day, Year)**, you would change the `string` line to:

```python
string = strftime('%I:%M:%S %p \n %B %d, %Y')
```

