[![New Project - 2024-11-18T015818 370](https://github.com/user-attachments/assets/5f51b216-518c-4ad3-a3e4-5ea4fee17085)](https://discord.gg/hVDgUm8WGr)

# 📌 Getting Started With CentrlV2
### Lets Start With Initliazing CentrlV2.
```lua
local centrl = loadstring(game:HttpGet("https://raw.githubusercontent.com/yarrosvault/CentrlV2/refs/heads/main/centrl",true))()
```
### Now Lets Set Up The Loader
```lua
centrl:load({
	Logo = '14258098097', -- ID Only (required, optional soon)
	ConfigEnabled = {
		Enabled = true, -- If Config Saving is desired leave true
		Cfolder = 'Centrlontop', -- Folder Name
		Cfile = 'Config' -- Config File Name (credits to rayfield for layout (not skidded)
	},
	Theme = {
		Accent = Color3.fromRGB(234, 9, 215), -- Accent color
		Hitbox =  Color3.fromRGB(234, 9, 215) -- Hitbox color (ex. toggle, slider)
	}
})
```
### Setting Up UI
```lua
local main = centrl:int({
	Title = 'CrudeHub', -- Title of UI
	Sub = 'Pet Sim x' -- Sub Text
})
```
### Setting Up A Tab
```lua
local Tab = main:IntTab('Main') -- More Features Coming Soon!
```
### Setting Up A Section (required)
```lua
local s1 = Tab:IntSection('Main', {
	Side = 'L' -- Side of section ('L' - Left, 'R' - Right)
})
```
### Setting Up Buttons
```lua
s1:createButton({
	Title = 'Button',
	Callback = function()
	end,
})
```

### Setting Up Toggle
```lua
s1:createToggle({
	Title = 'Toggle',
	Config = true, -- keybind n stuff
	Value = false, -- Starting Value
	Callback = function(v)
	end,
})
```

### Setting Up Slider (kinda complicated)
```lua
s1:createSlider({
	Title = 'Modifiers',
	Sliders = {
		{
			title = 'Strength',
			range = {1,120},
			increment = 1,
			startvalue = 16,
			callback = function(lol)

				game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = lol

			end,
		},
		{
			title = 'Smoothness',
			range = {1,200},
			increment = 1,
			startvalue = 16,
			callback = function(lol)


			end,
		},
	}
})

```
### Setting Up Dropdown
```lua
s2:createDropdown({
	Title = "Mode",
	Options = {'Mode 1', 'Mode 2', 'Mode 3', 'RAGE MODEE'},
	Multi = false, -- Multi Select?
	Callback = function(mode)
		print(mode)
	end,
}) 
```

### ColorPicker 
```lua
s2:createColorpicker({
	Title = 'Pepper Color',
	Color = Color3.fromRGB(255, 0, 4), -- Starter Color
	Callback = function(v)
		print(v)
	end,
})
```
