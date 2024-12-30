# Kavo UI
This documentation Is For Kavo UI

## Creating a Kavo UI Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/RileyBeeRBLX1/UI-Library/refs/heads/main/Kavo%20UI/KavoLibrary.lua"))()
```

## Creating a Kavo UI Window
```lua
local Window = Library.CreateLib("TITLE", "DarkTheme")
```

## Creating a Tab
```lua
local Tab = Window:NewTab("Tab")
```

## Creating a Section
```lua
local Section = Tab:NewSection("Section Name")
```

## Creating a Button
```lua
Section:NewButton("ButtonText", "ButtonInfo", function()
    print("Clicked")
end)
```

## Creating a Toggle
```lua
Section:NewToggle("ToggleText", "ToggleInfo", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
```

## Creating a Slider
```lua
Section:NewSlider("SliderText", "SliderInfo", 500, 0, function(s)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)
```

## Creating a Textbox
```lua
Section:NewTextBox("TextboxText", "TextboxInfo", function(txt)
	print(txt)
end)
```

## Creating a Keybind
```lua
Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.F, function()
	print("You just clicked the bind")
end)
```

## Creating a Toggle UI Keybind
```lua
Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.F, function()
	Library:ToggleUI()
end)
```

## Creating a Dropdown
```lua
Section:NewDropdown("DropdownText", "DropdownInf", {"Option 1", "Option 2", "Option 3"}, function(currentOption)
    print(currentOption)
end)
```

## Creating a Colorpicker
```lua
Section:NewColorPicker("Color Text", "Color Info", Color3.fromRGB(0,0,0), function(color)
    print(color)
    -- Second argument is the default color
end)
```

# Applying Custom Themes / Colors

Make new table, here you are going to put your colors, as shown below.

```lua
local colors = {
    SchemeColor = Color3.fromRGB(0,255,255),
    Background = Color3.fromRGB(0, 0, 0),
    Header = Color3.fromRGB(0, 0, 0),
    TextColor = Color3.fromRGB(255,255,255),
    ElementColor = Color3.fromRGB(20, 20, 20)
}
```

Applying it: Change your window code little bit.

```lua
local Window = Library.CreateLib("TITLE", colors)
```

# Want to add fully customizable UI?

Add this code in your section. This will create color pickers.
Make sure you have added table with all the values of UI. then apply it to window. Like shown above.

```lua
for theme, color in pairs(themes) do
    Section:NewColorPicker(theme, "Change your "..theme, color, function(color3)
        Library:ChangeColor(theme, color3)
    end)
end
```
