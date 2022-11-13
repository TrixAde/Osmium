<h1 align="center">Osmium Library Documentation</h1>

```lua
local library = pcall(loadstring("..."))
```

---

<h2 align="center">Window</h2>

## Create a Window

**library:CreateWindow(title: *string*) -> *Window***

```lua
local window = library:CreateWindow("Demo Window")
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

## Hide Window

Change the windows's state to `library.WindowState.Minimized`.

**Window:Hide()**

```lua
window:Hide()
```

## Show Window

Change the windows's state to `library.WindowState.Oppenned`.

**Window:Show()**

```lua
window:Show()
```

---

<h2 align="center">Tab</h2>

## Create a Tab

**Window:CreateTab(name: *string*) -> *Tab***

```lua
local tab = window:CreateTab("Demo Tab")
```

## Create a Text Label

**Tab:CreateLabel(text?: *string*, description?: *string*) -> *TextLabel***

```lua
local label = test:CreateLabel("Demo Text")
```

## Create a Button

**Tab:CreateButton(text: *string*, callback?: *function ()*) -> *Button***

```lua
local button = tab:CreateButton("Click Me", function ()
    print("Clicked")
end)
```

## Create a Toggle

**Tab:CreateToggle(text: *string*, default?: boolean, callback?: *function (boolean)*) -> *Toggle***

```lua
local toggle = tab:CreateToggle("On/Off", false, function (value)
    print("Value changed to", value)
end)
```

## Create a Text Box

**Tab:CreateTextBox(text: *string*, callback?: *function (string)*, placeholder?: *string*) -> *TextBox***

```lua
local textbox = tab:CreateTextBox("Input", function (value)
    print("Value changed to", value)
end, "Placeholder")
```

## Create a Dropdown

**Tab:CreateDropdown(text: *string*, values?: *table*, callback?: *function (string)*) -> *Dropdown***

```lua
local dropdown = tab:CreateDropdown("Select", {
    "A",
    "B",
    "C"
}, function (value)
    print("Value changed to", value)
end)
```

---

<h2 align="center">Text Label</h2>

## Update or Add Title Label

**TextLabel:SetTitle(text?: *string*)**

```lua
label:SetTitle("Title")
```

## Update or Add Title Description

**TextLabel:SetDescription(text?: *string*)**

```lua
label:SetDescription("Description")
```

---

<h2 align="center">Toggle</h2>

## Get Label

**Toggle:GetLabel() -> *string***

## Update Label

**Toggle:SetLabel(label: *string*)**

## Get Value

**Toggle:GetValue() -> *boolean***

## Update Value

**Toggle:SetValue(value: *boolean*)**

---

<h2 align="center">Text Box</h2>

## Get Label

**TextBox:GetLabel() -> *string***

## Update Label

**TextBox:SetLabel(label: *string*)**

## Get Value

**TextBox:GetValue() -> *string***

## Update Value

**TextBox:SetValue(value: *string*)**

---

<h2 align="center">Text Box</h2>

## Get Label

**TextBox:GetLabel() -> *string***

## Update Label

**TextBox:SetLabel(label: *string*)**

## Get Value

**TextBox:GetValue() -> *string***

## Update Value

**TextBox:SetValue(value: *string*)**

---

<h2 align="center">Dropdown</h2>

## Add Value

**Dropdown:Add(value: *string*)**

```lua
dropdown:Add("D")
```

## Remove a Value

**Dropdown:Remove(value: *string*)**

```lua
dropdown:Remove("D")
```

## Get Possibles Values

**Dropdown:Values() -> *table***

```lua
dropdown:Values()
```
