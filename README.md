for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(Plr,v.Name)
end
local drop = TeleportPlayer:NewDropdown("Select Player!", "Click To Select", Plr, function(t)
   PlayerTP = t
end)
TeleportPlayer:NewButton("Click To TP", "", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
end)
TeleportPlayer:NewToggle("Auto Tp", "", function(t)
_G.TPPlayer = t
while _G.TPPlayer do wait()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
end
end)
