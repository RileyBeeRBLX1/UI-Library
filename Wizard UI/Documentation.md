# Wizard UI
This documentation Is Only For Wizard UI

## Creating a Wizard UI Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/wizard"))()
```

## Creating a Wizard UI Window
```lua
local PhantomForcesWindow = Library:NewWindow("Combat")
```

## Creating a Section
```lua
local KillingCheats = PhantomForcesWindow:NewSection("Kill Options")
```

## Creating a Button
```lua
KillingCheats:CreateButton("Button", function()
print("HI")
end)
```

## Creating a Toggle
```lua
KillingCheats:CreateToggle("Auto Ez", function(value)
print(value)
end)
```

## Creating a Textbox
```lua
KillingCheats:CreateTextbox("TextBox", function(text)
        print(text)
end)
```

## Creating a Dropdown
```lua
KillingCheats:CreateDropdown("DropDown", {"Hello", "World", "Hello World"}, 2, function(text)
print(text)
end)
```

## Creating a Slider
```lua
KillingCheats:CreateSlider("Slider", 0, 100, 15, false, function(value)
print(value)
end)
```

## Creating a Colorpicker
```lua
KillingCheats:CreateColorPicker("Picker", Color3.new(255, 255, 255), function(value)
print(value)
end)
```
