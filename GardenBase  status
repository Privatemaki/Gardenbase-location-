local player = game.Players.LocalPlayer
local targetName = player.Name

print("=== GARDEN DETECTION TEST START ===")
print("Player:", targetName)

task.wait(2)

local foundGarden = nil

for _, obj in pairs(workspace:GetDescendants()) do

	if obj:IsA("TextLabel") then

		local txt = tostring(obj.Text)

		if string.find(txt, targetName) then

			local parent = obj.Parent

			while parent do

				if parent.Name and string.find(parent.Name, "GardenBase") then
					foundGarden = parent.Name
					break
				end
				parent = parent.Parent
			end

			if foundGarden then
				break
			end
		end
	end
end

if foundGarden then
	print("🌿 YOUR GARDEN IS:", foundGarden)
else
	print("⚠️ GARDEN NOT FOUND")
end

print("=== TEST DONE ===")
