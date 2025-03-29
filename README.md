-- Serviço necessário para inserir assets pelo ID
local InsertService = game:GetService("77443461")
local player = game.Players.LocalPlayer

-- Substitua o ID abaixo pelo ID do tool desejado
local toolID = 77443461

-- Insere o item no jogo e coloca na mochila do jogador
local success, tool = pcall(function()
    return InsertService:LoadAsset(toolID)
end)

if success and tool then
    tool.Parent = player.Backpack
    print("Tool adicionado com sucesso!")
else
    warn("Erro ao carregar o tool. Verifique o ID ou as permissões.")
end
