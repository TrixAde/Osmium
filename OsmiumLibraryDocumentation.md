<h1 align="center">Osmium Library Documentation</h1>

```lua
local _, library = pcall(loadstring(game:HttpGet("https://raw.githubusercontent.com/TrixAde/Osmium/main/OsmiumLibrary.lua")))
```

---

<h2 align="center">Window</h2>

### Create a Window

**library:CreateWindow(title: *string*) -> *Window***

```lua
local window = library:CreateWindow("Osmium UI Library")
```

## Get Window State

**Window:GetCurrentState() -> *number***

```lua
local state = window:GetCurrentState()

if state == library.WindowState.Destroyed then
    print("Window closed")
end
```

Possibles values :
- `library.WindowState.Destroyed`: the window is closed
- `library.WindowState.Oppenned`: the window is openned
- `library.WindowState.Minimized`: the window is openned and minimized

## Destroy Window

**Window:Destroy()**

```lua
window:Destroy()
```

---

<h2 align="center">Tab</h2>

## Create a Tab

**Window:CreateTab(name: *string*) -> *Tab***

```lua
local tab = window:CreateTab("Demo Tab")
```
---

<h2 align="center">Create a Text Label</h2>

**Tab:CreateLabel(text?: *string*, description?: *string*) -> *TextLabel***

```lua
local label = tab:CreateLabel("Title Exemple","Description Exemple")
```

<h2 align="center">Update Title</h2>

**TextLabel:SetTitle(text?: *string*) -> *TextLabel***

```lua
label:SetTitle("Title")
```

<h2 align="center">Update Description</h2>

**TextLabel:SetDescription(text?: *string*) -> *TextLabel***

```lua
label:SetDescription("Description")
```
---

<h2 align="center">Create a Toggle</h2>

**Tab:CreateToggle(text: *string*, default?: boolean, callback?: *function (boolean)*) -> *Toggle***

```lua
local toggle = tab:CreateToggle("Toggle Exemple", false, function (value)
    print("Value changed to", value)
end)
```

---

<h2 align="center">Create a Text Box</h2>

**Tab:CreateTextBox(text: *string*, callback?: *function (string)*, placeholder?: *string*) -> *TextBox***

```lua
local textbox = tab:CreateTextbox("TextBox Exemple", function(value)
    print("Value = ", value)
end, "Write Here")
```
---

<h2 align="center">Create a Button</h2>

**Tab:CreateButton(text: *string*, callback?: *function ()*) -> *Button***

```lua
local button = tab:CreateButton("Button Exemple", function()
    print("Clicked")
end)
```

---

<h2 align="center">Create a Slider</h2>

**Tab:CreateSlider(text: *string*, minvalue: *number*, maxvalue: *number*, callback?: *function ()*) -> *Slider***

```lua
local slider = tab:CreateSlider("Slider Exemple",0,100,function(arg)
	print(arg)
end)
```
<h2 align="center">Create a DropDown</h2>

**Tab:CreateDropdown(text: *string*, values?: *table*, callback?: *function ()*) -> *Slider***

```lua
local dropdown = tab:CreateDropdown("DropDown Exemple",{"Button 1","Button 2","Button 3"},function(val)
    print(val)
end)
```
