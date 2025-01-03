# Fluent UI
This documentation Is For Fluent UI

## Creating Fluent UI Library
```lua
local Fluent = loadstring(game:HttpGet("https://raw.githubusercontent.com/RileyBeeRBLX1/UI-Library/refs/heads/main/Fluent%20UI/Library.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()
```

## Creating Fluent UI Window
```lua
local Window = Fluent:CreateWindow({
    Title = "Fluent " .. Fluent.Version,
    SubTitle = "by dawid",
    TabWidth = 160,
    Size = UDim2.fromOffset(580, 460),
    Acrylic = true, -- The blur may be detectable, setting this to false disables blur entirely
    Theme = "Dark",
    MinimizeKey = Enum.KeyCode.LeftControl -- Used when theres no MinimizeKeybind
})
```

## Creating a Tab
```lua
local Tabs = {
    Main = Window:AddTab({ Title = "Main", Icon = "" }),
}
```
**WITH SETTINGS**
```lua
local Tabs = {
    Main = Window:AddTab({ Title = "Main", Icon = "" }),
    Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}
```

## Creating a Section
```lua
local Section = Tabs.Main:AddSection("Section")
```

## Creating a Option
```lua
local Options = Fluent.Options
```

## Creating a Notification
```lua
Fluent:Notify({
  Title = "Notification",
  Content = "This is a notification",
  SubContent = "SubContent", -- Optional
  Duration = 5 -- Set to nil to make the notification not disappear
})
```

## Creating a Paragraph
```lua
Tabs.Main:AddParagraph({
  Title = "Paragraph",
  Content = "This is a paragraph.\nSecond line!"
})
```

## Creating a Dialog
```lua
Window:Dialog({
       Title = "Title",
       Content = "This is a dialog",
        Buttons = {
                    {
                        Title = "Confirm",
                        Callback = function()
                            print("Confirmed the dialog.")
                        end
                    },
                    {
                        Title = "Cancel",
                        Callback = function()
                            print("Cancelled the dialog.")
                        end
     }
   }
})
```

## Creating a Button
```lua
Tabs.Main:AddButton({
  Title = "Button",
  Description = "Very important button",
  Callback = function()
  -- Script Here
  end
})
```

## Creating a Toggle
```lua
Tabs.Main:AddToggle("Toggle", {
  Title = "Toggle", 
  Default = false,
  Callback = function(Value)
  -- Script Here
  end
})
```

## Creating a Slider
```lua
Tabs.Main:AddSlider("Slider", {
  Title = "Slider",
  Description = "This is an slider",
  Default = 1,
  Min = 10,
  Max = 20,
  Rounding = 1,
  Callback = function()
  -- Script Here
  end
})
```

## Creating a Dropdown
```lua
Tabs.Main:AddDropdown("Dropdown", {
  Title = "Dropdown",
  Values = {"One", "Two", "Three"},
  Multi = false,
  Default = "One",
  Callback = function()
  -- Script Here 
  end
})
```

## Creating a Multi-Dropdown
```lua
Tabs.Main:AddDropdown("MultiDropdown", {
  Title = "Dropdown",
  Description = "You can select multiple values.",
  Values = {"one", "two", "three", "four", "five", "six", "seven", "eight", "nine", "ten", "eleven", "twelve", "thirteen", "fourteen"},
  Multi = true,
  Default = {"seven", "twelve"},
  Callback = function()
  -- Script Here
  end
})
```

## Creating a Colorpicker
```lua
local Colorpicker = Tabs.Main:AddColorpicker("Colorpicker", {
   Title = "Colorpicker",
   Default = Color3.fromRGB(96, 205, 255)
   Callback = function()
   -- Script Here
  end
})
```

## Creating a Transparent Colorpicker
```lua
local TColorpicker = Tabs.Main:AddColorpicker("TransparencyColorpicker", {
    Title = "Colorpicker",
    Description = "but you can change the transparency.",
    Transparency = 0,
    Default = Color3.fromRGB(96, 205, 255)
    Callback = function()
    print(
            "TColorpicker changed:", TColorpicker.Value,
            "Transparency:", TColorpicker.Transparency
        )
   end
})
```

## Creating a Transparent Colorpicker
```lua
local Keybind = Tabs.Main:AddKeybind("Keybind", {
   Title = "KeyBind",
   Mode = "Toggle", -- Always, Toggle, Hold
   Default = "LeftControl", -- String as the name of the keybind (MB1, MB2 for mouse buttons)

        -- Occurs when the keybind is clicked, Value is `true`/`false`
Callback = function(Value)
print("Keybind clicked!", Value)
end,

        -- Occurs when the keybind itself is changed, `New` is a KeyCode Enum OR a UserInputType Enum
ChangedCallback = function(New)
print("Keybind changed!", New)
end
})
```

## Creating a Textbox
```lua
local Input = Tabs.Main:AddInput("Input", {
   Title = "Input",
   Default = "Default",
   Placeholder = "Placeholder",
   Numeric = false, -- Only allows numbers
   Finished = false, -- Only calls callback when you press enter
   Callback = function(Value)
    print("Input changed:", Value)
   end
})
```

## Selecting a Tab
```lua
Window:SelectTab(1)
```

## Creating a Label
```lua
Tabs.Main:AddParagraph({ Title = "Label", })
```

## Misc
```lua
-- Addons:
-- SaveManager (Allows you to have a configuration system)
-- InterfaceManager (Allows you to have a interface management system)

-- Hand the library over to our managers
SaveManager:SetLibrary(Fluent)
InterfaceManager:SetLibrary(Fluent)

-- Ignore keys that are used by ThemeManager.
-- (we dont want configs to save themes, do we?)
SaveManager:IgnoreThemeSettings()

-- You can add indexes of elements the save manager should ignore
SaveManager:SetIgnoreIndexes({})

-- use case for doing it this way:
-- a script hub could have themes in a global folder
-- and game configs in a separate folder per game
InterfaceManager:SetFolder("FluentScriptHub")
SaveManager:SetFolder("FluentScriptHub/specific-game")

InterfaceManager:BuildInterfaceSection(Tabs.Settings)
SaveManager:BuildConfigSection(Tabs.Settings)


Window:SelectTab(1)

Fluent:Notify({
    Title = "Fluent",
    Content = "The script has been loaded.",
    Duration = 8
})

-- You can use the SaveManager:LoadAutoloadConfig() to load a config
-- which has been marked to be one that auto loads!
SaveManager:LoadAutoloadConfig()
```
