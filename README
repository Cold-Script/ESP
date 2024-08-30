local function Billboard(child, name, color, title)
    local Billboard = Instance.new("BillboardGui")
    Billboard.Active = true
    Billboard.AlwaysOnTop = true
    Billboard.ClipsDescendants = true
    Billboard.LightInfluence = 1
    Billboard.Size = UDim2.new(10, 0, 2, 0)
    Billboard.ResetOnSpawn = false
    Billboard.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
    Billboard.Parent = child
    Billboard.Name = title
    local Title = Instance.new("TextLabel")
    Title.Font = Enum.Font.ArialBold
    Title.Text = name
    Title.TextScaled = true
    Title.TextSize = 10
    Title.TextColor3 = color
    Title.TextWrapped = true
    Title.BackgroundColor3 = Color3.new(1, 1, 1)
    Title.BackgroundTransparency = 1
    Title.BorderColor3 = Color3.new(0, 0, 0)
    Title.BorderSizePixel = 0
    Title.Size = UDim2.new(1, 0, 1, 0)
    Title.Visible = true
    Title.Parent = Billboard
    local uistroke = Instance.new("UIStroke")
    uistroke.Thickness = 1
    uistroke.Parent = Title
end
local function Highlight(child, name, color, title)
    local Highlight = Instance.new("Highlight")
    Highlight.Parent = child
    Highlight.Adornee = child
    Highlight.OutlineColor = color
    Highlight.FillColor = color
    Highlight.FillTransparency = 0.86
    Highlight.Name = title
    Highlight.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
    if child:IsA("Part") then
        child.Color = Color3.fromRGB(0,0,0)
        child.Transparency = 0
    end
end
function ClearESP(name)
for _, v in pairs(workspace:GetDescendants()) do
                if v.Name == name and v:IsA("Highlight") or v:IsA("BillboardGui") then
                    v:Destroy()
                end
        end
end
----------------------------------------------------------------------------------------------
local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/REDzHUB/RedzLibV5/main/Source.Lua"))()
local v = 1.0
local Window = redzlib:MakeWindow({"ESP v".. v, "by white7777", "testando-redzLibv5.json"})
Window:AddMinimizeButton({
  Button = { Image = "rbxassetid://11010019801", BackgroundTransparency = 0 },
  Corner = { CornerRadius = UDim.new(0, 5) }
})
local Tabs = {
 Main = Window:MakeTab({"Main", "Home"})
}
----------------------------------------------------------------------------------------------
--Door ESP
Tabs.Main:AddToggle({
Name = "Door ESP",
Description = "Door ESP",
Default = false,
Callback = function(v1)
if v1 then
for _,v in pairs(workspace:GetDescendants()) do
if v.Name == "Door" and v.Parent.Name == "Door" then
Billboard(v, "Door", Color3.new(1,1,1), "DoorsESP")
Highlight(v, "Door", Color3.new(1,1,1), "DoorsESP")
end
end
DoorESP = workspace.ChildAdded:Connect(function(child)
for _,v in pairs(child:GetDescendants()) do
if v.Name == "Door" and v.Parent.Name == "Door" then
Billboard(v, "Door", Color3.new(1,1,1), "DoorsESP")
Highlight(v, "Door", Color3.new(1,1,1), "DoorsESP")
end
end
end)
else
DoorESP:Disconnect()
ClearESP("DoorESP")
end
end})
----------------------------------------------------------------------------------------------
