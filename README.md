# FuturalUIMain
A modern, futuristic UI library for Roblox with a split layout design similar to Orion/Rayfield. FuturaUI provides a responsive interface that works seamlessly on both PC and mobile devices.

# Features
🎨 Clean, futuristic design
📱 Responsive for both PC and mobile
🔑 Optional key system for script protection
📊 Split layout with sections on the left, content on the right
🎛️ Comprehensive set of UI elements
⚡ Smooth animations and transitions
🔧 Easy-to-use API

# Installation
To use FuturaUI in your script, simply require the module:
``` 
local Rayfield = loadstring(game:HttpGet('https://raw.githubusercontent.com/XXXT3/CyberFuturaUI/refs/heads/main/source.lua?token=GHSAT0AAAAAADBIGSDOUXZWRN4OE7B6GFQ2Z7FVPMA'))()
```

# Full Tutorial
# Creating the UI
Start by creating a new UI instance. You can optionally enable key system protection:

``` 
-- Without key system
local UI = FuturaUI.new("My UI Title")

-- With key system
local UI = FuturaUI.new("My Protected UI", "SecretKey123")
```

# Adding Sections
Sections appear in the left panel and organize your UI elements:
``` UI:AddSection("General")
UI:AddSection("Player")
UI:AddSection("Settings")
UI:AddSection("Credits") ```


