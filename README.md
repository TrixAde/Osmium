<h1 align="center">Osmium Library Documentation</h1>

```lua
local library = pcall(loadstring("..."))
```

---

<h2 align="center">Window</h2>

### Create a Window

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

---

<h2 align="center">Tab</h2>

## Create a Tab

**Window:CreateTab(name: *string*) -> *Tab***

```lua
local tab = window:CreateTab("Demo Tab")
```
---

## Create a Text Label

**Tab:CreateLabel(text?: *string*, description?: *string*) -> *TextLabel***

```lua
local label = test:CreateLabel("Demo Text")
```

<h2 align="center">Update or Add Title Label</h2>

**TextLabel:SetTitle(text?: *string*) -> *TextLabel***

```lua
label:SetTitle("Title")
```

<h2 align="center">Update or Add Title Description</h2>

**TextLabel:SetDescription(text?: *string*) -> *TextLabel***

```lua
label:SetDescription("Description")
```
---

<h2 align="center">Create a Toggle</h2>

**Tab:CreateToggle(text: *string*, default?: boolean, callback?: *function (boolean)*) -> *Toggle***

```lua
local toggle = tab:CreateToggle("On/Off", false, function (value)
    print("Value changed to", value)
end)
```

<h2 align="center">Create a Text Box</h2>

**Tab:CreateTextBox(text: *string*, callback?: *function (string)*, placeholder?: *string*) -> *TextBox***

```lua
local textbox = tab:CreateTextBox("Input", function (value)
    print("Value changed to", value)
end, "Placeholder")
```

<h2 align="center">Create a TextBox</h2>
