-- # SodiumClient
-- Sodium V1 Script
--Printer
print("Sodium Loaded!")
--Script Below
local SodiumClient = Instance.new("ScreenGui")
local FirstFrameLog = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local Title = Instance.new("TextLabel")
local Autofarm = Instance.new("TextButton")
local UICorner_2 = Instance.new("UICorner")
local Loaded = Instance.new("TextLabel")
local Autofarm_2 = Instance.new("TextLabel")

SodiumClient.Name = "SodiumClient"
SodiumClient.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
SodiumClient.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

FirstFrameLog.Name = "FirstFrameLog"
FirstFrameLog.Parent = SodiumClient
FirstFrameLog.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
FirstFrameLog.Position = UDim2.new(0.0569696985, 0, 0.224076286, 0)
FirstFrameLog.Size = UDim2.new(0, 205, 0, 387)

UICorner.Parent = FirstFrameLog

Title.Name = "Title"
Title.Parent = FirstFrameLog
Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Title.BackgroundTransparency = 1.000
Title.Position = UDim2.new(0.146341473, 0, 0, 0)
Title.Size = UDim2.new(0, 144, 0, 36)
Title.Font = Enum.Font.Arcade
Title.Text = "Sodium V1"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.TextScaled = true
Title.TextSize = 14.000
Title.TextWrapped = true

Autofarm.Name = "Autofarm"
Autofarm.Parent = FirstFrameLog
Autofarm.BackgroundColor3 = Color3.fromRGB(57, 57, 57)
Autofarm.Position = UDim2.new(0.048780486, 0, 0.826873362, 0)
Autofarm.Size = UDim2.new(0, 184, 0, 46)
Autofarm.Font = Enum.Font.Arcade
Autofarm.Text = "Autofarm"
Autofarm.TextColor3 = Color3.fromRGB(255, 255, 255)
Autofarm.TextScaled = true
Autofarm.TextSize = 14.000
Autofarm.TextStrokeTransparency = 0.000
Autofarm.TextWrapped = true

UICorner_2.Parent = Autofarm

Loaded.Name = "Loaded"
Loaded.Parent = SodiumClient
Loaded.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Loaded.BackgroundTransparency = 1.000
Loaded.Position = UDim2.new(0, 0, 0.94040525, 0)
Loaded.Size = UDim2.new(0, 200, 0, 50)
Loaded.Font = Enum.Font.Arcade
Loaded.Text = "Sodium Loaded"
Loaded.TextColor3 = Color3.fromRGB(255, 255, 255)
Loaded.TextScaled = true
Loaded.TextSize = 14.000
Loaded.TextWrapped = true

Autofarm_2.Name = "Autofarm"
Autofarm_2.Parent = SodiumClient
Autofarm_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Autofarm_2.BackgroundTransparency = 1.000
Autofarm_2.Position = UDim2.new(0, 0, 0.880810499, 0)
Autofarm_2.Size = UDim2.new(0, 200, 0, 50)
Autofarm_2.Font = Enum.Font.Arcade
Autofarm_2.Text = "Autofarm: OFF"
Autofarm_2.TextColor3 = Color3.fromRGB(255, 255, 255)
Autofarm_2.TextScaled = true
Autofarm_2.TextSize = 14.000
Autofarm_2.TextWrapped = true

-- Scripts:

local function TOENTJK_fake_script()
	local script = Instance.new('LocalScript', FirstFrameLog)

	script.Parent.Active = true
	wait(0)
	script.Parent.Draggable = true
end
coroutine.wrap(TOENTJK_fake_script)()
local function YUFMKE_fake_script()
	local script = Instance.new('LocalScript', Autofarm)

	-- Tables Below(Can be changed!)
	local CoolDown = 5
	local Worked = false
	local plr = game.Players.LocalPlayer -- Plr Varible don't change pls
	-- Varibles for function below don't touch if you know what you're doing.
	local endspawn = game.Workspace.EndStuff.SpawnLocation
	local returnspawn = game.Workspace.EndStuff.ReturnToSpawn
	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Parent.Autofarm.Text = "Autofarm: ON"
		while true do
			wait(CoolDown)
			Worked = true
			if Worked == true then
				print("AutoFarm Loaded..!")
			else
				plr.Character.Parent = nil
				print("AutoFarm Error, Sorry")
			end
			endspawn.CFrame = plr.Character.HumanoidRootPart.CFrame 
			wait(1)
			endspawn.CFrame = CFrame.new(0,0,0)
			wait(CoolDown)
			returnspawn.CFrame = plr.Character.HumanoidRootPart.CFrame 
			wait(1)
			returnspawn.CFrame = CFrame.new(0,0,0)
			print(plr.leaderstats.Wins.Value)
		end
	end)
	
	
end
coroutine.wrap(YUFMKE_fake_script)()
local function PTOZEWY_fake_script()
	local script = Instance.new('LocalScript', Loaded)

	local plr = game.Players.LocalPlayer
	
	script.Parent.Text = "Goodmorning, "..plr.Name..". Sodium Has been loaded for you."
end
coroutine.wrap(PTOZEWY_fake_script)()
