# Material UI
This documentation Is For Material UI

## Creating a Material UI Library
```lua
local Material = loadstring(game:HttpGet("https://raw.githubusercontent.com/RileyBeeRBLX1/UI-Library/refs/heads/main/Material%20UI/Module.lua"))()
```

## Creating a Material UI Window
```lua
local Window = Material.Load({
	Title = "Material UI",
	Style = 3,
	SizeX = 500,
	SizeY = 350,
	Theme = "Dark",
})
```

## Creating a Tab
```lua
local Tab = Window.New({
	Title = "Tab"
})
```

## Creating a Button
```lua
local Button = Tab.Button({
	Text = "Button",
	Callback = function()
		print("hello")
	end,
})
```

## Creating a Toggle
```lua
local Toggle = Tab.Toggle({
	Text = "Toggle",
	Enabled = false,
	Callback = function(Value)
		print(Value)
	end,
})
```

## Creating a Slider
```lua
local Slider = Tab.Slider({
	Text = "Slider",
	Min = 200,
	Max = 400,
	Def = 300,
	Callback = function(Value)
		print(Value)
	end,
})
```

## Creating a Dropdown
```lua
local Dropdown = Tab.Dropdown({
	Text = "Dropdown",
	Options = {"One", "Two", "Three"},
	Callback = function(Value)
		print(Value)
	end,
})
```

## Creating a Colorpicker
```lua
local ColorPicker = Tab.ColorPicker({
	Text = "Color Picker",
	Default = Color3.fromRGB(0, 255, 110),
	Callback = function(Value)
		print("RGB:", Value.R * 255, Value.G * 255, Value.B * 255)
	end,
})
```

## Creating a Label
```lua
Tab.Label({
	Text = "This Is An Label"
})
```


## Creating a Text-Field
```lua
local TextField = Tab.TextField({
	Text = "Choose Number",
	Menu = {
		GB = function(self)
			self.SetText("GB")
		end,
		JP = function(self)
			self.SetText("JP")
		end,
		KO = function(self)
			self.SetText("KO")
		end
	},
	Callback = function(Value)
		print(Value)
	end
})
```
