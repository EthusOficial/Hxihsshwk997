local ChatService = game:GetService("Chat")
local Players = game:GetService("Players")

-- Variável para armazenar a mensagem
local mensagemPadrao = "Foram adicionados 150 scripts na aba do Blox Fruits é amanhã 15/12 vao ser adicionados mais scripts na Aba Blue Lock Rivals." -- Alterar a mensagem aqui

-- Função para exibir balões de chat para todos os jogadores
local function showBubbleChatForAll(message)
    for _, player in ipairs(Players:GetPlayers()) do
        if player.Character and player.Character:FindFirstChild("Head") then
            ChatService:Chat(player.Character.Head, message, Enum.ChatColor.White)
        end
    end
end

-- Chama a função usando a mensagem configurada
showBubbleChatForAll(mensagemPadrao)
