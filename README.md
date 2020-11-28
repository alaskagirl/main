
for i,player in pairs(game.Players:GetPlayers()) do
	for i,k in pairs(player.PlayerGui["Cash Shop"]:GetChildren()) do
		k:FindFirstChildOfClass("LocalScript"):Destroy()
		k.MouseButton1Click:Connect(function()
			print(k.Name)
		end)
	end
end

game.Players.PlayerAdded:Connect(function(player)
for i,k in pairs(player.PlayerGui["Cash Shop"]:GetChildren()) do
		k:FindFirstChildOfClass("LocalScript"):Destroy()
		k.MouseButton1Click:Connect(function()
			print(k.Name)
		end)
	end
end)


