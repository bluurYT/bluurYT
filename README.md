if game.PlaceId == 155615604 then
 local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
 local Window = Library.CreateLib("Prison Life V12", "BloodTheme")

 --MAIN
  local Main = Window:NewTab("Main")
  local MainSection = Main:NewSection("Main")
  MainSection:NewDropdown("Gun Giver", "Gives the localPlayer a gun :)", {"M9", "Remington 870", "AK-47"}, function(v)
    local A_1 = game:GetService("Workspace")["Prison_ITEMS"].giver[v].ITEMPICKUP
    local Event = game:GetService("Workspace").Remote.ItemHandler
    Event:InvokeServer(A_1)
end)
MainSection:NewButton("Fly(E)", "Press E to fly", function()
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
local speed = 5000 

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
if key:lower() == "e" then 
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
    print("Clicked")
end)
MainSection:NewButton("NoClip(Q)", "Press Q to use Noclip", function()
    noclip = false
    game:GetService('RunService').Stepped:connect(function()
    if noclip then
    game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
    end
    end)
    plr = game.Players.LocalPlayer
    mouse = plr:GetMouse()
    mouse.KeyDown:connect(function(key)
    if key == "q" then
    noclip = not noclip
    game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
    end
    end)
    game.StarterGui:SetCore("SendNotification", {
    Title = "Noclip";
    Text = "Loaded.";
    Duration = "10";
    })
    wait(1)
    game.StarterGui:SetCore("SendNotification", {
    Title = "Noclip";
    Text = "Press E To Noclip";
    Duration = "10";
    })
print(s)  
    print("Clicked")
end)
 --PLAYER
 local Player = Window:NewTab("Player")
 local PlayerSection = Player:NewSection("Player")
 PlayerSection:NewSlider("WalkSpeed", "Changes Player's Speed", 500, 16, function(v) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = v
end)
PlayerSection:NewSlider("JumpPower", "Changes Player's JumpPower", 500, 50, function(v) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = v
end)
end

if game.PlaceId == 3956818381 then
    local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
    local Window = Library.CreateLib("Ninja Legends V12", "BloodTheme")

--MAIN
local Main = Window:NewTab("Main")
  local MainSection = Main:NewSection("Main")

MainSection:NewToggle("Auto Swing", "AutoClicker ig?", function(v)
end)
getgenv().autoswing = v
    while true do
        if not getgenv().autoswing then return end
        for _,v in pairs (game.Players.LocalPlayer.BackPack:GetChildren()) do
            if v:FindFirstChild("Katana") then
                game.Players.LocalPlayer.Character.Humanoid:EquipTool(v)
                break
    end
end
    local A_1 = "swingKatana"
    local Event = game:GetService("Players").LocalPlayer.ninjaEvent
    Event:FireServer(A_1)
    wait(0.25)
end
end)
MainSection:NewToggle("Auto Sell","Makes player autosell", function(v)
    getgenv().autosell = v
    while true do
        if not getgenv().autosell then return end
        print(working)
        game:GetService("Workspace").sellAreaCircles{"sellAreaCircles16"}.Cframe = game.LocalPlayer.Character.HumanoidRootPart
        wait(0.1)
        game:GetService("Workspace").sellAreaCircles{"sellAreaCircles16"}Cframe = Cframe.new(0,0,0)
        wait(0.1)
return
   end
end)
end
--Don't steal.
if game.PlaceId == 4753520418 then
    local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
    local Window = Library.CreateLib("The Hood V12", "BloodTheme")
    --Main
    local Main = Window:NewTab("Main")
      local MainSection = Main:NewSection("Main")
    
      --Player
      local Other = Window:NewTab("Other")
     local OtherSection = Other:NewSection("Other")
    
     --Commands(Main)
     MainSection:NewButton("Fly", "Makes local player fly", function()
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
        print("Clicked")
    
    end)
    MainSection:NewButton("SilentAim", "wee", function()
    end)
    -- // Dependencies
    local Aiming = loadstring(game:HttpGet("https://raw.githubusercontent.com/Stefanuk12/ROBLOX/master/Universal/Aiming/Module.lua"))()
    Aiming.TeamCheck(false)
    
    -- // Services
    local Workspace = game:GetService("Workspace")
    local Players = game:GetService("Players")
    local RunService = game:GetService("RunService")
    local UserInputService = game:GetService("UserInputService")
    
    -- // Vars
    local LocalPlayer = Players.LocalPlayer
    local Mouse = LocalPlayer:GetMouse()
    local CurrentCamera = Workspace.CurrentCamera
    
    local DaHoodSettings = {
        SilentAim = true,
        AimLock = true,
        Prediction = 100,
        AimLockKeybind = Enum.KeyCode.K
    }
    getgenv().DaHoodSettings = DaHoodSettings
    
    -- // Overwrite to account downed
    function Aiming.Check()
        -- // Check A
        if not (Aiming.Enabled == true and Aiming.Selected ~= LocalPlayer and Aiming.SelectedPart ~= nil) then
            return false
        end
    
        -- // Check if downed
        local Character = Aiming.Character(Aiming.Selected)
        local KOd = Character:WaitForChild("BodyEffects")["K.O"].Value
        local Grabbed = Character:FindFirstChild("GRABBING_CONSTRAINT") ~= nil
    
        -- // Check B
        if (KOd or Grabbed) then
            return false
        end
    
        -- //
        return true
    end
    
    -- // Hook
    local __index
    __index = hookmetamethod(game, "__index", function(t, k)
        -- // Check if it trying to get our mouse's hit or target and see if we can use it
        if (t:IsA("Mouse") and (k == "Hit" or k == "Target") and Aiming.Check()) then
            -- // Vars
            local SelectedPart = Aiming.SelectedPart
    
            -- // Hit/Target
            if (DaHoodSettings.SilentAim and (k == "Hit" or k == "Target")) then
                -- // Hit to account prediction
                local Hit = SelectedPart.CFrame + (SelectedPart.Velocity * DaHoodSettings.Prediction)
    
                -- // Return modded val
                return (k == "Hit" and Hit or SelectedPart)
            end
        end
    
        -- // Return
        return __index(t, k)
    end)
    
    -- // Aimlock
    RunService:BindToRenderStep("AimLock", 0, function()
        if (DaHoodSettings.AimLock and Aiming.Check() and UserInputService:IsKeyDown(DaHoodSettings.AimLockKeybind)) then
            -- // Vars
            local SelectedPart = Aiming.SelectedPart
    
            -- // Hit to account prediction
            local Hit = SelectedPart.CFrame + (SelectedPart.Velocity * DaHoodSettings.Prediction)
    
            -- // Set the camera to face towards the Hit
            CurrentCamera.CFrame = CFrame.lookAt(CurrentCamera.CFrame.Position, Hit.Position)
        end
    end)
    MainSection:NewButton("Headless", "ClientSided", function()
        --by qjbnbalivemobile1#0946
    
    --Objects
    local ScreenGui = Instance.new("ScreenGui")
    local main = Instance.new("Frame")
    local title = Instance.new("TextLabel")
    local Headless = Instance.new("TextButton")
    local OneLeg = Instance.new("TextButton")
    local close = Instance.new("TextButton")
    local openmain = Instance.new("Frame")
    local open = Instance.new("TextButton")
    
    --Properties:
    ScreenGui.Parent = game.CoreGui
    
    main.Name = "main"
    main.Parent = ScreenGui
    main.BackgroundColor3 = Color3.new(0, 0, 0)
    main.Position = UDim2.new(0.0203577988, 0, 0.641277611, 0)
    main.Size = UDim2.new(0, 332, 0, 211)
    main.Visible = false
    main.Active = true
    main.Draggable = true
    
    title.Name = "title"
    title.Parent = main
    title.BackgroundColor3 = Color3.new(1, 0, 1)
    title.Size = UDim2.new(0, 332, 0, 31)
    title.Font = Enum.Font.GothamBold
    title.Text = "qjbnbalivemobile1#0946"
    title.TextColor3 = Color3.new(0, 0, 0)
    title.TextSize = 17
    
    Headless.Name = "Headless"
    Headless.Parent = main
    Headless.BackgroundColor3 = Color3.new(0.333333, 1, 0)
    Headless.Position = UDim2.new(0.036144577, 0, 0.379146934, 0)
    Headless.Size = UDim2.new(0, 110, 0, 50)
    Headless.Font = Enum.Font.GothamBold
    Headless.Text = "Headless"
    Headless.TextColor3 = Color3.new(0, 0, 0)
    Headless.TextScaled = true
    Headless.TextSize = 10
    Headless.TextWrapped = true
    Headless.MouseButton1Down:connect(function()
    game.Players.LocalPlayer.Character.Head.Transparency = 1
    for i,v in pairs(game.Players.LocalPlayer.Character.Head:GetChildren()) do
    if (v:IsA("Decal")) then
    v:Destroy()
    end
    end
    end)
    
    OneLeg.Name = "One Leg"
    OneLeg.Parent = main
    OneLeg.BackgroundColor3 = Color3.new(0.333333, 1, 0)
    OneLeg.Position = UDim2.new(0.614457846, 0, 0.379146934, 0)
    OneLeg.Size = UDim2.new(0, 110, 0, 50)
    OneLeg.Font = Enum.Font.GothamBold
    OneLeg.Text = "One Leg"
    OneLeg.TextColor3 = Color3.new(0, 0, 0)
    OneLeg.TextScaled = true
    OneLeg.TextSize = 14
    OneLeg.TextWrapped = true
    OneLeg.MouseButton1Down:connect(function()
    game.Players.LocalPlayer.Character['Right Leg']:remove()
    end)
    
    close.Name = "close"
    close.Parent = main
    close.BackgroundColor3 = Color3.new(1, 0, 0)
    close.Position = UDim2.new(0.879518092, 0, 0, 0)
    close.Size = UDim2.new(0, 40, 0, 31)
    close.Font = Enum.Font.GothamBlack
    close.Text = "X"
    close.TextColor3 = Color3.new(0, 0, 0)
    close.TextScaled = true
    close.TextSize = 14
    close.TextWrapped = true
    close.MouseButton1Down:connect(function()
    main.Visible = false
    openmain.Visible = true
    end)
    
    openmain.Name = "openmain"
    openmain.Parent = ScreenGui
    openmain.BackgroundColor3 = Color3.new(1, 1, 1)
    openmain.Position = UDim2.new(.001, 0, .79, 0)
    openmain.Size = UDim2.new(0, 100, 0, 28)
    openmain.Active = true
    openmain.Draggable = true
    
    open.Name = "open"
    open.Parent = openmain
    open.BackgroundColor3 = Color3.new(1, 0, 0)
    open.Size = UDim2.new(0, 100, 0, 28)
    open.Font = Enum.Font.GothamBold
    open.Text = "OPEN"
    open.TextColor3 = Color3.new(0, 0, 0)
    open.TextSize = 18
    open.TextWrapped = true
    open.MouseButton1Down:connect(function()
    openmain.Visible = false
    main.Visible = true
    end)
    
        print("Clicked")
    end)
    MainSection:NewSlider("WalkSpeed", "Changes Player's Speed", 150, 16, function(v) -- 500 (MaxValue) | 0 (MinValue)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = v
    end)
    MainSection:NewSlider("JumpPower", "Changes Player's JumpPower", 230, 50, function(v) -- 500 (MaxValue) | 0 (MinValue)
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = v
    end)
    end
    MainSection:NewButton("AutoStomp", "cherry", function()
    end)
    --Other
    OtherSection:NewButton("Esp", "Korblox", function()
    end)
        OtherSection:NewButton("AutoFarm", "Auto", function()
        end)
        OtherSection:NewButton("AutoStomp", "yes", function()
            
        end)
        OtherSection:NewButton("Korblox", "ButtanInfo", function()
            
        OtherSection:NewButton("AutoPickUpGuns", "ButtanInfo", function()
            OtherSection:NewButton("AutoSell", "yes", function()

