print("hello workd")
for i,player in pairs(game.Players:GetPlayers()) do
	print(player.Name.."Is Gai")
end

game.Players.PlayerAdded:Connect(function(player)
	print(player.Name.."Is Gai")
end)


