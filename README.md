if game.PlaceId == 4753520418 then
end
--Game
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("ｵ Desire (Candy Clicking Simulator)", "BloodTheme")

--Tabs
local Main = Window:NewTab("Main")
local MainSection = Main:NewSection("Main")
local Teleports = Window:NewTab("Teleports")
local TeleportsSection = Teleports:NewSection("Teleports")
local WalkSpeed = Window:NewTab("WalkSpeed")
local WalkSpeedSection = WalkSpeed:NewSection("WalkSpeed")


TeleportsSection:NewButton("Main", "Makes localPlayer teleport to the island", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(3026.2959, 995.314087, 2074.95508, -0.422592998, -0, -0.906319618, 0, -1, 0, -0.906319618, 0, 0.422592998)
end)
TeleportsSection:NewButton("Gumdrop Paradise", "Makes localPlayer teleport to the island", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(745.430786, 573.144653, 585.344604, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)
TeleportsSection:NewButton("Sweet Island", "Makes localPlayer teleport to the island", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1454.96936, 693.119812, -713.745483, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)
TeleportsSection:NewButton("Chocolate Falls", "Makes localPlayer teleport to the island", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-3405.65918, 699.588013, -2208.21558, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)
TeleportsSection:NewButton("Marshmallow Wonderland", "Makes localPlayer teleport to the island", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5522.9292, 699.588013, -4139.03174, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)
TeleportsSection:NewButton("Cotton Candy Palace", "Makes localPlayer teleport to the island", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1745.6261, 507.397827, 2248.23779, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)
TeleportsSection:NewButton("Burnt Kingdom", "Makes localPlayer teleport to the island", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-4190.39307, 1117.20239, 610.93512, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)
TeleportsSection:NewButton("Cookie Realm", "Makes localPlayer teleport to the island", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2533.25928, 699.588013, -4904.21582, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)
TeleportsSection:NewButton("Dino Reign", "Makes localPlayer teleport to the island", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-4832.00977, 806.230408, -7312.31543, -0.318264127, 0, 0.94800204, 0, 1, 0, -0.94800204, 0, -0.318264127)
end)
WalkSpeedSection:NewSlider("WalkSpeed", "Changes localPlayer's speed", 500, 16, function(v) 
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)
WalkSpeedSection:NewSlider("JumpPower", "Changes localPlayer's ", 500, 16, function(v) 
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = s
end)
MainSection:NewButton("AutoClicker", "Makes localPlayer AutoClick", function()
    getgenv().farmer = true;

while wait() do
    if getgenv().farmer == true then
        game:service'ReplicatedStorage'.Events.ClickEvent:InvokeServer()
    end
end
end)
MainSection:NewButton("Fly", "Makes localPlayer fly", function()
    repeat wait() 
	until game.Players.LocalPlayer and game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:findFirstChild("Head") and game.Players.LocalPlayer.Character:findFirstChild("Humanoid") 
local mouse = game.Players.LocalPlayer:GetMouse() 
repeat wait() until mouse
local plr = game.Players.LocalPlayer 
local torso = plr.Character.Head 
local flying = false
local deb = true 
local ctrl = {f = 0, b = 0, l = 0, r = 0} 
local lastctrl = {f = 0, b = 0, l = 0, r = 0} 
local maxspeed = 400 
local speed = 400

function Fly() 
local bg = Instance.new("BodyGyro", torso) 
bg.P = 9e4 
bg.maxTorque = Vector3.new(9e9, 9e9, 9e9) 
bg.cframe = torso.CFrame 
local bv = Instance.new("BodyVelocity", torso) 
bv.velocity = Vector3.new(0,0.1,0) 
bv.maxForce = Vector3.new(9e9, 9e9, 9e9) 
repeat wait() 
plr.Character.Humanoid.PlatformStand = true 
if ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0 then 
speed = speed+.5+(speed/maxspeed) 
if speed > maxspeed then 
speed = maxspeed 
end 
elseif not (ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0) and speed ~= 0 then 
speed = speed-1 
if speed < 0 then 
speed = 0 
end 
end 
if (ctrl.l + ctrl.r) ~= 0 or (ctrl.f + ctrl.b) ~= 0 then 
bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (ctrl.f+ctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(ctrl.l+ctrl.r,(ctrl.f+ctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed 
lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r} 
elseif (ctrl.l + ctrl.r) == 0 and (ctrl.f + ctrl.b) == 0 and speed ~= 0 then 
bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (lastctrl.f+lastctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(lastctrl.l+lastctrl.r,(lastctrl.f+lastctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed 
else 
bv.velocity = Vector3.new(0,0.1,0) 
end 
bg.cframe = game.Workspace.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*speed/maxspeed),0,0) 
until not flying 
ctrl = {f = 0, b = 0, l = 0, r = 0} 
lastctrl = {f = 0, b = 0, l = 0, r = 0} 
speed = 0 
bg:Destroy() 
bv:Destroy() 
plr.Character.Humanoid.PlatformStand = false 
end 
mouse.KeyDown:connect(function(key) 
if key:lower() == "x" then 
if flying then flying = false 
else 
flying = true 
Fly() 
end 
elseif key:lower() == "w" then 
ctrl.f = 1 
elseif key:lower() == "s" then 
ctrl.b = -1 
elseif key:lower() == "a" then 
ctrl.l = -1 
elseif key:lower() == "d" then 
ctrl.r = 1 
end 
end) 
mouse.KeyUp:connect(function(key) 
if key:lower() == "w" then 
ctrl.f = 0 
elseif key:lower() == "s" then 
ctrl.b = 0 
elseif key:lower() == "a" then 
ctrl.l = 0 
elseif key:lower() == "d" then 
ctrl.r = 0 
end 
end)
Fly()
end)

MainSection:NewButton("AntiAFK", "Makes localPlayer not disconnect", function()
    local vu = game:GetService("VirtualUser")
    game:GetService("Players").LocalPlayer.Idled:connect(function()
    vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
    wait(1)
    vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
    end)
    end)
    MainSection:NewButton("Redeem Twitter codes", "free shit aceept it", function()
        end)
        wait(0.5)
local A_1 = "UPDATE28"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "10KLIKES"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE27"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "4MEVENT"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "GODLY"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE26"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE25"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "HAPPYEASTER"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE24"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "OMEGA"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE21"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "PLUSHIE"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE20"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "TOFU"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "VALENTINES"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "HEARTS"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE18"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "18KFAVORITES"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "5KLIKES"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "NUKE"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "2MEVENT"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "2MEGG"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE16"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE15"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "RELEASE"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "CAM"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "CANDY"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "1kfavorites"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "300Likes"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "Update2"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "Event"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "100kVisits"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "Update3"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "1MVISITS"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE10"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "3KLIKES"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE12"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE13"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
wait(0.5)
local A_1 = "UPDATE14"
local Event = game:GetService("ReplicatedStorage").Events.RedeemCode
Event:InvokeServer(A_1)
