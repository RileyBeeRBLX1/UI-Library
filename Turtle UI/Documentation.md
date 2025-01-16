# Turtle UI
This documentation Is For Turtle UI

## Creating a Turtle UI Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/RileyBeeRBLX1/UI-Library/refs/heads/main/Turtle%20UI/Library.lua"))()
```

## Creating a Turtle UI Window
```lua
local Window = Library:Window("Window")
```

## Creating a Button
```lua
Window:Button("Button", function()
-- Your script here
end)
```

## Creating a Toggle
```lua
Window:Toggle("Toggle", true, function(Value)
-- Your script here
end)
```

## Creating a Slider
```lua
Window:Slider("Slider", 0,100,20, function(Value)
-- Your script here
end)
```

## Creating a Textbox
```lua
Window:Box("Textbox", function(Value)
-- Your script here
end)
```

## Creating a Dropdown
```lua
local Dropdown = Window:Dropdown("Dropdown", {"One", "Two", "Three"}, function(Value)
-- Your script here
end)
```

## Creating a Colorpicker
```lua
Window:ColorPicker("Colorpicker", Color3.fromRGB(255, 255, 255), function(color)
-- Your script here
end)
```

## Creating a Label
```lua
Window:Label("This is An Label", Color3.fromRGB(127, 143, 166))
```

## Creating a Textbox
```lua
Tab:Textbox("Textbox", true, function(Value)
-- Your Script Here
end)
```

# UPDATE FUNCTION

## New Dropdown Button
```lua
Dropdown:Button("New Button")
```

## Remove Dropdown Button
```lua
Dropdown:Remove("Button")
```
