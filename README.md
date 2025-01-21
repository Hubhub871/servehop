local TeleportService = game:GetService("TeleportService")
local PlaceId = 123456789 -- Substitua com o PlaceId do servidor de destino

game.Players.PlayerAdded:Connect(function(player)
    -- Teleporta o jogador para outro servidor (dentro do mesmo jogo)
    player.CharacterAdded:Connect(function()
        TeleportService:TeleportToPlaceAsync(PlaceId, player)
    end)
end)
