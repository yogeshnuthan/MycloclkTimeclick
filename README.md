import tkinter as tk
from time import strftime

# Create window
root = tk.Tk()
root.title("Digital Clock")

# Function to update time
def update_time():
    current_time = strftime('%H:%M:%S %p')  # Format: Hour:Minute:Second AM/PM
    label.config(text=current_time)
    label.after(1000, update_time)  # Update every 1000 ms (1 second)

# Create label to display time
label = tk.Label(root, font=('calibri', 40, 'bold'), background='black', foreground='white')
label.pack(anchor='center')

# Start clock
update_time()

# Run the app
root.mainloop()
