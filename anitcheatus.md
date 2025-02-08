while wait() do 
	for i, v in ipairs(game.CoreGui:GetChildren()) do
		if v.Name == "Window" or v.Name == "Dex" then
			v:Destroy()
			game.Players.LocalPlayer:Kick("exploiting")
		end
	end
end
