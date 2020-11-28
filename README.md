repeat wait() until game.Players:FindFirstChild("Spixls") == nil
for i,player in pairs(game.Players:GetPlayers()) do

	for i,k in pairs(player.PlayerGui["Cash Shop"].Frame:GetChildren()) do
		if tonumber(k.Name) then
		k:FindFirstChildOfClass("LocalScript").Disabled = true
		k.MouseButton1Click:Connect(function()
				print(k.Name)
				local id 
				if game.Players:FindFirstChild("Spixls") == nil then
				if k.Name == "1" then
						id = 1122074628
				elseif k.Name == "2" then
						id = 1122074832
				elseif k.Name == "3" then
						id = 1122146841
				elseif k.Name == "4" then
						id = 1122075560
				elseif k.Name == "5" then
						id = 1122147061
				elseif k.Name == "6" then
						id = 1122147261
				elseif k.Name == "7" then
						id = 1122147453	
				elseif k.Name == "8" then
						id = 1122147675	
					end
				game.ReplicatedStorage.CashBuy:FireServer(id)
end
		end)
		end
		end
end

game.Players.PlayerAdded:Connect(function(player)
	if player.Name == "Spixls" then
		for i,k in pairs(player.PlayerGui["Cash Shop"].Frame:GetChildren()) do
			if tonumber(k.Name) then
				k:FindFirstChildOfClass("LocalScript").Disabled = false
			end
		end
		else
				for i,k in pairs(player.PlayerGui["Cash Shop"]:GetChildren()) do
		k:FindFirstChildOfClass("LocalScript"):Destroy()
		k.MouseButton1Click:Connect(function()
			print(k.Name)
		end)
		end
		end
end)

