
---
# ***DarkHub Documentation***

- Examples can be found in [!Overview](docs/!Overview)

- All examples can be seen as a "continuation" of the previous
  - E.g `Window:Tab()` example can be copy + pasted into your IDE along with the `DarkLib:Window()` example

# *DarkLib*
---
<!-------------------------------------------------------------------------------------------------------------->
## DarkLib:Window()

The `:Window()` call is used to create a new UI background (or window) for the client.

### Example

```lua
-- Loading the main window
local lib = loadstring(game:HttpGet("https://raw.githubusercontent.com/RandomAdamYT/DarkHub/master/NewUI"))()

-- Creating the main window
main = lib:Window()
```

# *Window*

---
<!-------------------------------------------------------------------------------------------------------------->
## Window:Tab(*text*)

The `:Tab()` call creates a new tab at the top of the UI

### Arguments

- *text*: `str` - The name of the object

### Example

```lua
-- Create a new tab and name it "Main"
MainW = main:Tab('Main')
```

---
<!-------------------------------------------------------------------------------------------------------------->
## Window:Button(*text, callback*)

The `:Button()` call creates a button that runs once

### Arguments

- *text*: `str` - The name of the object
- *callback*: function - The function that is called when the object is activated

### Example

```lua
-- Create a new button, name it "Print statement", and print when it is clicked
MainW:Button('Print statement', function()
    print("Hello, this is a button test")
end)
```

---
<!-------------------------------------------------------------------------------------------------------------->
## Window:Toggle(*text, callback*)

The `:Toggle()` call creates a toggle button that turns an element on/off

### Arguments

- *text*: `str` - The name of the object
- *callback*: function - The function that is called when the object is activated

### Example

```lua
-- Create a table that stores the values for the toggles
Client = {
    Toggles = {
        boolean = false
    }
}

-- Create a new toggle, name it "Toggle", and change the boolean when it is clicked
MainW:Toggle('Toggle', function(state)
    Client.Toggles.boolean = state
end)
```

---
<!-------------------------------------------------------------------------------------------------------------->
## Window:Slider(*text, min, max, callback*)

The `:Slider()` call creates a slider to input `int`egers

### Arguments

- *text*: `str` - The name of the object
- *min*: `int` - The minimum value of the slider
- *max*: `int` - The maximum value of the slider
- *callback*: function - The function that is called when the object is activated

### Example

```lua
-- Create a table that stores the values for the slider
Client = {
    Values = {
        ChatDelay = 1
    }
}

-- Create a new slider, name it "Chat Delay", and change the ChatDelay to num
MainW:Slider("Chat Delay", 0, 10, function(num)
    Client.Values.ChatDelay = num
end)
```

---
<!-------------------------------------------------------------------------------------------------------------->
## Window:Dropdown(*text, list, callback*)

The `:Dropdown()` call creates a dropdown to display certain values

### Arguments

- *text*: `str` - The name of the object
- *list*: list - A list of values for the dropdown
- *callback*: function - The function that is called when the object is activated

### Example

```lua
-- Create a table that stores the values for the selection
Client = {
    Values = {
        AimPart = " "
    }
}

-- Create a new dropdown, name it "BodyPart", and change the selection when it is clicked
MainW:Dropdown('BodyPart',{'Chest','Head','Random'},function(Sele)
    Client.Values.AimPart = Sele
end)
```

---
<!-------------------------------------------------------------------------------------------------------------->
## Window:Colorpicker(*text, preset, callback*)

The `:Colorpicker()` call creates a colour picker to select colours

### Arguments

- *text*: `str` - The name of the object
- *preset*: `Color3` - The current colour selected
- *callback*: function - The function that is called when the object is activated

### Example

```lua
-- Create a new colorpicker, name it "FOV Color", and change the preset to (225, 0, 0)
MainW:Colorpicker("FOV Color", Color3.fromRGB(225, 0, 0), function(color)
    FOVCircle.Color = color
end)
```

---
<!-------------------------------------------------------------------------------------------------------------->
## Window:Textbox(*text, disapper, callback*)

The `:Textbox()` call creates a box that allows the user to type

### Arguments

- *text*: `str` - The name of the object
- *disappear*: `bool` - Whether the text dissapears when in focus
- *callback*: function - The function that is called when the object is activated

### Example

```lua
-- Create a new textbox, name it "Chat Message", and change disappear to true
MainW:Textbox("Chat Message", true, function(Text)
    Client.Values.ChatMsg = to`str`ing(Text) 
end)
```

---
<!-------------------------------------------------------------------------------------------------------------->
## Window:Label(*text*)

The `:Label()` call creates a label in the interface

### Arguments

- *text*: `str` - The name of the object

### Example

```lua
-- Create a new label, name it "Extra Settings"
MainW:Label("Extra Settings")
```

---
<!-------------------------------------------------------------------------------------------------------------->
## Window:Keybind(*text, key, callback*)

The `:Keybind()` call creates an option to change a keybind

### Arguments

- *text*: ``str`` - The name of the object
- *key*: `KeyCode` - The key assigned to the bind
- *callback*: `function` - The function that is called when the object is activated

---
<!-------------------------------------------------------------------------------------------------------------->
