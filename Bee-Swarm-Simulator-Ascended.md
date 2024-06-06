local gui= Instance.new("ScreenGui")
local frame = Instance.new("Frame")
local button = Instance.new("TextButton")

gui.Parent = game.Players.LocalPlayer.PlayerGui
frame.Parent = gui
button.Parent = frame

frame.Position = UDim2.new(0, 610,0, 155)
frame.Size = UDim2.new(0, 100,0, 50)
frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
button.Position = UDim2.new(0, 0,0.5, 0)
button.Size = UDim2.new(0, 100,0, 25)
button.Text = "tool inf use"
button.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
button.TextScaled = true

frame.Draggable = true
frame.Active = true

button.MouseButton1Up:Connect(function()
  for _, child in game.Players.LocalPlayer.Character:GetChildren() do
    if child.ClassName == "Tool" then
      while wait(0.25) do
      child.ToolRemote:FireServer()
      end
    end
  end
end)
