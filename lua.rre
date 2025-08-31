-- ColorName.lua
-- Script que pone un nombre colorido encima de la cabeza del jugador

game.Players.PlayerAdded:Connect(function(player)
    player.CharacterAdded:Connect(function(char)
        local head = char:WaitForChild("Head")

        -- Elimina etiquetas viejas si las hay
        for _, v in pairs(head:GetChildren()) do
            if v:IsA("BillboardGui") then
                v:Destroy()
            end
        end

        -- Crea la etiqueta
        local billboard = Instance.new("BillboardGui")
        billboard.Size = UDim2.new(0,200,0,50)
        billboard.Adornee = head
        billboard.Parent = head
        billboard.AlwaysOnTop = true

        local text = Instance.new("TextLabel")
        text.Size = UDim2.new(1,0,1,0)
        text.BackgroundTransparency = 1
        text.Text = player.Name
        text.TextColor3 = Color3.fromRGB(255, 215, 0) -- Dorado
        text.Font = Enum.Font.SourceSansBold
        text.TextScaled = true
        text.Parent = billboard
    end)
end)
