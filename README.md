# Digital-Clock
Simple digital clock using a Windows Forms application. Let's break down the key components and functionality:

### Namespace and Libraries
```csharp
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
```
- These lines import necessary libraries for handling Windows Forms, date/time operations, and graphical user interface elements.

### Form Class (`Form1`)
```csharp
public partial class Form1 : Form
{
    public Form1()
    {
        InitializeComponent();
    }
    
    // ... other methods and event handlers
}
```
- `Form1` is a class representing the main form of the application. It inherits from the `Form` class.
- The constructor `Form1()` initializes the form components.

### Components
- The form contains several `Label` controls (`lblTime`, `lblSecond`, `lblDate`, `lblDay`) which will display the current time, seconds, date, and day of the week respectively.

### `timer_Tick` Event Handler
```csharp
private void timer_Tick(object sender, EventArgs e)
{
    lblTime.Text = DateTime.Now.ToString("HH:mm");
    lblSecond.Text = DateTime.Now.ToString("ss");
    lblDate.Text = DateTime.Now.ToString("MMM dd yyyy");
    lblDay.Text = DateTime.Now.ToString("dddd");
    lblSecond.Location = new Point(lblTime.Location.X + lblTime.Width - 5, lblSecond.Location.Y);
}
```
- This event handler updates the labels with the current time, seconds, date, and day of the week.
- `DateTime.Now` provides the current date and time, and `ToString()` formats it as required.
- It also adjusts the position of the `lblSecond` label to make it visually appear next to the `lblTime` label.

### `Form1_Load_1` Event Handler
```csharp
private void Form1_Load_1(object sender, EventArgs e)
{
    timer.Start();
}
```
- This event handler is triggered when the form is loaded.
- It starts the timer (`timer`) which triggers the `timer_Tick` event at regular intervals to update the clock.

### Overall Functionality
- The code creates a simple digital clock displaying the current time, seconds, date, and day of the week using Windows Forms.
- It uses a timer to update the displayed information at regular intervals.

### Documentation
Documentation is crucial for code maintainability. Adding comments to the code explaining the purpose of each method, event handler, or complex logic can make it easier for others (and yourself in the future) to understand and modify the code.


<a href="https://www.flaticon.com/free-icons/digital-clock" title="digital clock icons">Digital clock icons created by Freepik - Flaticon</a>
