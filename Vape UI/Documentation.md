# Vape UI
This documentation Is For Vape UI

## Creating a Vape UI Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/RileyBeeRBLX1/UI-Library/refs/heads/main/Vape%20UI/Library.lua"))()
```

## Creating a Vape UI Window
```lua
local Window = Library:Window("PREVIEW",Color3.fromRGB(44, 120, 224), Enum.KeyCode.RightControl)
```

## Creating a Tab
```lua
local Tab = Window:Tab("Tab")
```

## Creating a Section
```lua
local Section = Tab:Section("Section")
```

## Creating a Notification
```lua
Library:Notification("Notification", "Hello!", "Hi!")
```

## Creating a Button
```lua
Tab:Button("Button", function()
-- Your Script Here
end)
```

## Creating a Toggle
```lua
Tab:Toggle("Toggle",false, function(Value)
-- Your Script Here
end)
```

## Creating a Slider
```lua
Tab:Slider("Slider", 0,100,30, function(Value)
-- Your Script Here
end)
```

## Creating a Dropdown
```lua
Tab:Dropdown("Dropdown", {"Option 1","Option 2","Option 3","Option 4","Option 5"}, function(Value)
-- Your Script Here
end)
```

## Creating a Textbox
```lua
Tab:Textbox("Textbox", true, function(Value)
-- Your Script Here
end)
```

## Creating a Colorpicker
```lua
Tab:Colorpicker("Colorpicker", Color3.fromRGB(255,0,0), function(Value)
-- Your Script Here
end)
```

## Creating a Keybind
```lua
Tab:Bind("Bind", Enum.KeyCode.RightShift, function()
-- Your Script Here
end)
```
