# Redz Library
This documentation is for the stable release of Redz Library.

## Booting the Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/realredz/RedzLibV5/refs/heads/main/Source.lua""))()
```



## Creating a Window
```lua
local Window = Library:MakeWindow({
  Title = "REDz HUB",
  SubTitle = "by realredz",
  SaveFolder = "redzUI"
})
```

## Creating a Minimize UI
```lua
Window:AddMinimizeButton({
    Button = { Image = "rbxassetid://", BackgroundTransparency = 0 },
    Corner = { CornerRadius = UDim.new(0, 6) }
})
```

## Creating a Tab
```lua
local Tab = Window:MakeTab({"Tab 1", "cool"})
```
## Creating a Section
```lua
local Section = Tab:AddSection({"Section"})
```


## Creating a Button
```lua
local Button = Tab:AddButton({"Button", function()
-- Your script here
end})
```

## Creating a Toggle
```lua
local Toggle = Tab:AddToggle({
  Name = "Toggle",
  Default = false
  Callback = function()

  end
})
```


## Creating a Slider
```lua
local Slider = Tab:AddSlider({
  Name = "Slider",
  Min = 0,
  Max = 200,
  Increase = 1,
  Default = 16,
  Callback = function(value)
    game:GetService("Players").LocalPlayer.Character.Humanoid.WalkSpeed = value
  end
})
```

### Creating a Dropdown
```lua
local Dropdown = Tab:AddDropdown({
  Name = "Dropdown",
  Description = "A dropdown",
  Options = {"One", "Two", "Three"},
  Default = "One",
  Flag = "Dropdown",
  Callback = function(Value)
  -- Your script here
 end
})
```

## Creating a Textbox
```lua
local Textbox = Tab:AddTextBox({
  Name = "Textbox",
  Description = "this is a Text box",
  Default = "Text",
  Callback = function(Value)
  -- Your Script Here
  end
})
```

## Creating a Dialog
```lua
local Dialog = Window:Dialog({
    Title = "Dialog",
    Text = "This is a Dialog",
    Options = {
      {"Confirm", function()
        
      end},
      {"Maybe", function()
        
      end},
      {"Cancel", function()
        
      end}
    }
  })
```

## Creating a Paragraph
```lua
local Paragraph = Tab:AddParagraph({"Paragraph", "This is a Paragraph"})
```

## Selecting a Tab
```lua
Window:SelectTab(Tab2)
```

### Creating a Discord Server Invite
```lua
Tab:AddDiscordInvite({
  Name = "redz Hub | Community",
  Logo = "rbxassetid://15298567397",
  Invite = "https://discord.gg/7aR7kNVt4g"
})
```
