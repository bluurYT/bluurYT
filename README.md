if game.PlaceId == 5490351219 then
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("ｵ Desire (Clicker Madness!)", "Ocean")


--Main
local Main = Window:NewTab("Main")
local Section = Main:NewSection("Main")

Section:NewButton("Anti-AFK", "No disconnect!", function()
    local vu = game:GetService("VirtualUser")
    game:GetService("Players").LocalPlayer.Idled:connect(function()
    vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
    wait(1)
    vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
    end)
end)
Section:NewButton("Go VIP", "!", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(518.599976, 15.5010281, -1342.40002, -0.998631716, 0, 0.0522932447, 0, 1, 0, -0.0522932447, 0, -0.998631716)
end)
Section:NewButton("Promo Codes", "Get exclusive items!", function()
    wait(0.5)
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.CodeService.Redeem:InvokeServer("RUSSO")
wait(0.5)
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.CodeService.Redeem:InvokeServer("12KLIKES")
wait(0.5)
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.CodeService.Redeem:InvokeServer("RobleRom")
wait(0.5)
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.CodeService.Redeem:InvokeServer("RazorFishGaming")
wait(0.5)
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.CodeService.Redeem:InvokeServer("Release")
wait(0.5)
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.CodeService.Redeem:InvokeServer("Elsa")
wait(0.5)
end)

local Tab = Window:NewTab("Autofarm")

local Section = Tab:NewSection("Auto Click")

Section:NewToggle("AutoClick", "make bobux go brr", function(state)
    if state then
        getgenv().farmer = true;
while wait() do
    if getgenv().farmer == true then
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.ClickService.Click:FireServer("1")
end
end
    else
        getgenv().farmer = false;
while wait() do
    if getgenv().farmer == true then
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.ClickService.Click:FireServer("1")
end
end
    end
end)

local Section = Tab:NewSection("Boss AutoFarm")

Section:NewToggle("Autofarm Boss", "big xp ez", function(state)
    if state then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(799.182739, 5.85324478, -260.70813, 0.978142142, -0.0021191542, -0.207926601, 0.00217329664, 0.999997616, 3.19531682e-05, 0.207926035, -0.000483140931, 0.978144407)
getgenv().farmer = true;
while wait() do
    if getgenv().farmer == true then
        game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.CursorCannonService.FireBoss:FireServer("Karen Keyboard")
    end
end
    else
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(554.441528, 4.21923256, -353.808472, 0.398127973, -0, -0.917329907, 0, 1, -0, 0.917329907, 0, 0.398127973)
getgenv().farmer = false;
while wait() do
    if getgenv().farmer == true then
        game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.CursorCannonService.FireBoss:FireServer("Karen Keyboard")
    end
end

    end
end)

local Section = Tab:NewSection("Auto Beast Mode")

Section:NewToggle("Auto Beast + click", "very op trust", function(state)
    if state then
        getgenv().farm = true
while wait() do
    if getgenv().farm == true then
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.BeastModeService.Begin:FireServer()

end
end
    else
        getgenv().farm = false
        while wait() do
            if getgenv().farm == true then
        game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.BeastModeService.Begin:FireServer()
        end
               getgenv().farmer = false
        while wait() do
            if getgenv().farmer == true then
        game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.ClickService.Click:FireServer("1")
        end
        end
        end 
    end
end)

local Section = Tab:NewSection("Auto PickUp")
Section:NewToggle("AutoPickUp", "yes", function(state)
    if state then
        getgenv().autopickup = true
while wait() do
    if getgenv().autopickup == true then
        game:GetService("Workspace").ScriptObjects.BasePickup.HumanoidRootPart.CFrame = CFrame.new.LocalPlayer
end
end
    else
        getgenv().autopickup = false
while wait() do
    if getgenv().autopickup == true then
        game:GetService("Workspace").ScriptObjects.BasePickup.HumanoidRootPart.CFrame = CFrame.new(527.820679, 8.61664009, -384.444092, 0.667936862, 1.6815779e-08, 0.744217932, 4.50804265e-08, 1, -6.30549977e-08, -0.744217932, 7.56664207e-08, 0.667936862)
end
end
    end
end)

local Teleports = Window:NewTab("Teleports")

local Teleports = Teleports:NewSection("Teleports")

Teleports:NewButton("Main Island", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(554.441528, 4.21923256, -353.808472, 0.398127973, -0, -0.917329907, 0, 1, -0, 0.917329907, 0, 0.398127973)
end)
Teleports:NewButton("Desert", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2288.66113, 7.36253929, 1087.66602, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Winter", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2195.28003, 6.46062994, 409.998016, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Lava", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1690.38525, 7.77716637, -734.648865, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Ocean", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-258.018005, 9.72535324, 2065.25439, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Candy", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1418.74072, 9.27518654, -2243.14648, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Space", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2394.43408, 7.40711641, 2861.37256, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Forest", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1838.47925, 8.35549545, 3260.10547, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("City", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-888.616638, 7.70115376, 1026.44592, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Blocks", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2997.47729, 11.1703444, -782.602905, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Future", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1142.82349, 9.54701519, 519.403564, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Infinity", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2160.427, 8.20108604, -1764.58118, 0.917312562, 0, 0.398167908, 0, 1, 0, -0.398167908, 0, 0.917312562)
end)
Teleports:NewButton("Moon", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2394.43408, 7.40711641, 1899.26257, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Fire", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2192.76514, 7.77716637, -734.648865, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Storm", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-283.451447, 8.89227104, -2593.82104, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Teleports:NewButton("Dominus", "Teleports to it", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1114.78931, 8.35549545, 2254.00562, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)

local RebirthUpgrades = Window:NewTab("RebirthUpgrades")

local RebirthUpgrades = RebirthUpgrades:NewSection("RebirthUpgrades")

RebirthUpgrades:NewButton("ClickMultiply", "yh", function()
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.UpgradeService.BuyUpgrade:FireServer("ClickMultiply");
end)
RebirthUpgrades:NewButton("CursorDamage", "yh", function()
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.UpgradeService.BuyUpgrade:FireServer("CursorDamage");
end)
RebirthUpgrades:NewButton("Health", "yh", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.UpgradeService.BuyUpgrade:FireServer("Health");
end)
RebirthUpgrades:NewButton("JumpPower", "yh", function()
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.UpgradeService.BuyUpgrade:FireServer("JumpPower");
end)
RebirthUpgrades:NewButton("Pet Storage", "yh", function()
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.UpgradeService.BuyUpgrade:FireServer("PetStorage")
end)
RebirthUpgrades:NewButton("Speed Upgrade", "yh", function()
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.UpgradeService.BuyUpgrade:FireServer("WalkSpeed")
end)

local AutoRebirth = Window:NewTab("AutoRebirth")

local AutoRebirth = AutoRebirth:NewSection("AutoRebirth")

AutoRebirth:NewToggle("1 Rebirth", "yh", function(state)
    if state then
        getgenv().rebirth = true
while wait() do
    if getgenv().rebirth == true then
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer("1")
  end
end
    else
        getgenv().rebirth = false
while wait() do
    if getgenv().rebirth == true then
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer("1")
  end
end
    end
end)
AutoRebirth:NewToggle("Rebirth 10", "yh", function(state)
    if state then
        getgenv().rebirth = true
while wait() do
    if getgenv().rebirth == true then
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer("10")
  end
end

    else
        getgenv().rebirth = false
while wait() do
    if getgenv().rebirth == true then
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer("10")
  end
end
    end
end)

AutoRebirth:NewToggle("Rebirth 100", ":(", function(state)
    if state then
        getgenv().rebirth = true
while wait() do
    if getgenv().rebirth == true then
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer("100")
  end
end

    else
        getgenv().rebirth = false
while wait() do
    if getgenv().rebirth == true then
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer("100")
  end
end

    end
end)

AutoRebirth:NewToggle("Rebirth 1,000", "a", function(state)
    if state then
        getgenv().rebirth = true
while wait() do
    if getgenv().rebirth == true then
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer("1000")
  end
end

    else
        getgenv().rebirth = false
while wait() do
    if getgenv().rebirth == true then
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer("1000")
  end
end

    end
end)

AutoRebirth:NewToggle("Rebirth 10,000", "op", function(state)
    if state then
        getgenv().rebirth = true
        while wait() do
            if getgenv().rebirth == true then
            
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer(10000)
            end
            end
    else

            getgenv().rebirth = false
            while wait() do
                if getgenv().rebirth == true then
                
game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer(10000)
                end
                end
    end
end)

AutoRebirth:NewToggle("Rebirth 100K", "e", function(state)
    if state then
        getgenv().rebirth = true
while wait() do
    if getgenv().rebirth then
        game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer(100000)
    end
end
    else
        getgenv().rebirth = false
        while wait() do
            if getgenv().rebirth then
                game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer(100000)
            end
        end
    end
end)
AutoRebirth:NewToggle("Rebirth 1Mil", "haha", function(state)
    if state then
        
        getgenv().rebirth = true
        while wait() do
            if getgenv().rebirth then
                game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer(1000000)
            end
        end
    else
        getgenv().rebirth = false
while wait() do
    if getgenv().rebirth then
        game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer(1000000)
    end
end

    end
end)
AutoRebirth:NewToggle("Rebirth 10Mil", "ToggleInfo", function(state)
    if state then
        getgenv().rebirth = true
        while wait() do
            if getgenv().rebirth then
                game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer(10000000)
            end
        end
          
    else
        getgenv().rebirth = false
while wait() do
    if getgenv().rebirth then
        game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer(10000000)
    end
end

    end
end)

AutoRebirth:NewToggle("Rebirth 100Mil", "a", function(state)
    if state then
        getgenv().rebirth = true
while wait() do
    if getgenv().rebirth then
        game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer(10000000)
    end
end
    else
        getgenv().rebirth = false
while wait() do
    if getgenv().rebirth then
        game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.RebirthService.BuyRebirths:FireServer(1000000)
    end
end

    end
end)


local OpenEgg = Window:NewTab("OpenEgg")

local OpenEgg = OpenEgg:NewSection("OpenEgg")

OpenEgg:NewButton("Basic", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("basic");
end)
OpenEgg:NewButton("Lava", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("lava");
end)
OpenEgg:NewButton("Desert", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("desert");
end)
OpenEgg:NewButton("Winter", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("winter");
end)
OpenEgg:NewButton("Ocean", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("ocean");
end)
OpenEgg:NewButton("Candy", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("candy");
end)
OpenEgg:NewButton("Space", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("space");
end)
OpenEgg:NewButton("Forest", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("forest");
end)
OpenEgg:NewButton("City", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("city");
end)
OpenEgg:NewButton("Blocks", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("blocks");
end)
OpenEgg:NewButton("Future", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("future");
end)
OpenEgg:NewButton("Infinity", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("infinity");
end)
OpenEgg:NewButton("Moon", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("moon");
end)
OpenEgg:NewButton("Fire", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("fire");
end)
OpenEgg:NewButton("Storm", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("storm");
end)
OpenEgg:NewButton("Dominus", "basic", function()
    game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.EggService.Purchase:FireServer("dominus");
end)





local Misc = Window:NewTab("Misc")

local Misc = Misc:NewSection("Misc")

Misc:NewSlider("WalkSpeed", "SliderInfo", 500, 16, function(s) 
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)

Misc:NewSlider("JumpPower", "SliderInfo", 500, 50, function(s) 
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = s
end)

Misc:NewButton("Click TP Tool", "y", function()

mouse = game.Players.LocalPlayer:GetMouse()
tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "Click Teleport"
tool.Activated:connect(function()
local pos = mouse.Hit+Vector3.new(0,2.5,0)
pos = CFrame.new(pos.X,pos.Y,pos.Z)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos
end)
tool.Parent = game.Players.LocalPlayer.Backpack
end)



local Credits = Window:NewTab("Credits")
local Credits = Credits:NewSection("Made whole script")

Credits:NewLabel("Desire/Rayha")
end
