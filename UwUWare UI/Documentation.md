# UwUWare UI
This documentation Is For UwUWare UI

## Creating a UwUWare UI Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/ToraScript/Script/refs/heads/main/test", true))()
```

## Creating a UwUWare UI Window
```lua
local Window = Library:CreateWindow"Window"
```

## Creating a Folder
```lua
local Folder = Window:AddFolder"Folder"
```

## Creating a Button
```lua
Folder:AddButton({text = "Button", flag = "button", callback = function()
-- Your Script Here
end})
```

## Creating a Toggle
```lua
Folder:AddToggle({text = "Toggle", flag = "toggle", state = false, callback = function(a)
-- Your Script Here
end})
```

## Creating a Dropdown
```lua
Folder:AddList({text = "List", flag = "list", value = "Value", values = {"Value1", "Value2", "Value3", "Value4"}, callback = function(a)
-- Your Script Here
end})
```

## Creating a Textbox
```lua
Folder:AddBox({text = "Box", flag = "box", value = "Value", callback = function(a)
-- Your Script Here
end})
```

## Creating a Slider
```lua
Folder:AddSlider({text = "Slider", flag = "slider", value = 100, min = 20, max = 200, float = 0.3, callback = function(a)
-- Your Script Here
end})
```

## Creating a Keybind
```lua
Folder:AddBind({text = "Bind", flag = "bind", key = "MouseButton1", callback = function()
-- Your Script Here
end})
```

## Creating a Colorpicker
```lua
Folder:AddColor({text = "Color", flag = "color", color = Color3.fromRGB(255, 65, 65), callback = function()
-- Your Script Here
end})
```

## Creating a Init (YOU NEED THIS OR ELSE IT WONT LOAD UP)
```lua
Library:Init()
```

## Flags
```lua
print("Toggle is currently:", Library.flags["toggle"])
print("Second toggle is currently:", Library.flags["toggle1"])
```
