
		local active = true


		if active == false and workspace:FindFirstChild("arte") == nil then
			local arte = Instance.new("BoolValue",workspace)
			arte.Name = "arte"
		elseif active and workspace:FindFirstChild("arte") then
			for i,k in pairs(workspace:GetChildren()) do
				if k.Name == "arte" then
					k:Destroy()
				end
			end
		end
