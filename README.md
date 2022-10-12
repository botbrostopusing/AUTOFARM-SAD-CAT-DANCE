--// UI Library \\--
local File = writefile and readfile or false
local Library = false
Success, Library = pcall(function()
    return readfile("uwuware UI.lua")
end)
if Success == false then
    Library = game:HttpGet('https://raw.githubusercontent.com/Just-Egg-Salad/roblox-scripts/main/uwuware')
    if File then
        writefile("uwuware UI.lua", Library)
    end
end
Library = loadstring(Library)()
local Window = Library:CreateWindow("made by puro#4730")
Window:AddToggle({
    text = "autofarm",
    callback = function()
while task.wait(10) and Library.flags.autofarm do
local args = {
    [1] = "Play"
}

game:GetService("ReplicatedStorage").RemoteEvent:FireServer(unpack(args))

        end
	end
})

Library:Init()
