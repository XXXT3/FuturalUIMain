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

#Adding UI Elements
Labels and Dividers
``` -- Add a simple text label
UI:AddLabel("General", "Welcome to my script!")

-- Add a divider (optionally with text)
UI:AddDivider("General")
UI:AddDivider("General", "Controls") ```

Buttons
``` -- Add a button with a callback function
UI:AddButton("General", "Activate Power", function()
    print("Power activated!")
    -- Your code here
end) ```

Toggles
``` -- Add a toggle with initial state and callback
local toggle = UI:AddToggle("Settings", "Auto-Farm", false, function(value)
    print("Auto-Farm is now:", value)
    -- Your code here
end)
-- You can update it later
toggle:SetValue(true) ```

Sliders
``` -- Add a slider with min, max, default values and callback
local slider = UI:AddSlider("Settings", "Speed", 0, 100, 50, function(value)
    print("Speed set to:", value)
    -- Your code here
end)
-- Update slider value later
slider:SetValue(75) ``` 

Dropdowns
``` -- Add a dropdown with options and callback
local dropdown = UI:AddDropdown("Settings", "Quality", {"Low", "Medium", "High"}, "Medium", function(option)
    print("Selected quality:", option)
    -- Your code here
end)

-- Change selection later
dropdown:SetValue("High") ```

Text Input
``` -- Add a textbox with placeholder and callback
UI:AddTextbox("Player", "Name", "Enter your name...", "", function(text, enterPressed)
    if enterPressed then
        print("Name set to:", text)
        -- Your code here
    end
end) ```

Color Picker
``` -- Add a color picker with default color and callback
local colorPicker = UI:AddColorPicker("Settings", "UI Color", Color3.fromRGB(0, 170, 255), function(color)
    print("Color changed to:", color)
    -- Your code here
end) ```

# Notifications
Show temporary notifications to the user:

``` -- Parameters: title, content, duration (seconds)
UI:Notify("Success", "Operation completed successfully", 3) ```

# Toggling the UI
You can programmatically show/hide the UI:

``` -- Toggle UI visibility
UI:Toggle() ```

