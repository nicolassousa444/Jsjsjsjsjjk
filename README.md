# Jsjsjsjsjjk-- Definindo os mundos
local World1, World2, World3 = false, false, false

-- Verificando qual mundo o jogador está
if game.PlaceId == 2753915549 then
    World1 = true
elseif game.PlaceId == 4442272183 then
    World2 = true
elseif game.PlaceId == 7449423635 then
    World3 = true
else
    game:GetService("Players").LocalPlayer:Kick("Mundo não suportado. Por favor, aguarde...")
end

-- Função para verificar a missão com base no nível
function CheckQuest()
    local MyLevel = game:GetService("Players").LocalPlayer.Data.Level.Value

    -- Inicializando variáveis
    local Mon, LevelQuest, NameQuest, NameMon, CFrameQuest, CFrameMon

    -- Verificando qual missão será atribuída de acordo com o nível
    if World1 then
        if MyLevel >= 1 and MyLevel <= 9 then
            Mon = "Bandit"
            LevelQuest = 1
            NameQuest = "BanditQuest1"
            NameMon = "Bandit"
            CFrameQuest = CFrame.new(1059.37195, 15.4495068, 1550.4231)
            CFrameMon = CFrame.new(1045.962646484375, 27.00250816345215, 1560.8203125)
        elseif MyLevel >= 10 and MyLevel <= 14 then
            Mon = "Monkey"
            LevelQuest = 1
            NameQuest = "JungleQuest"
            NameMon = "Monkey"
            CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838)
            CFrameMon = CFrame.new(-1448.51806640625, 67.85301208496094, 11.46579647064209)
        elseif MyLevel >= 15 and MyLevel <= 29 then
            Mon = "Gorilla"
            LevelQuest = 2
            NameQuest = "JungleQuest"
            NameMon = "Gorilla"
            CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838)
            CFrameMon = CFrame.new(-1129.8836669921875, 40.46354675292969, -525.4237060546875)
        elseif MyLevel >= 30 and MyLevel <= 39 then
            Mon = "Pirate"
            LevelQuest = 1
            NameQuest = "BuggyQuest1"
            NameMon = "Pirate"
            CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498)
            CFrameMon = CFrame.new(-1103.513427734375, 13.752052307128906, 3896.091064453125)
        elseif MyLevel >= 40 and MyLevel <= 59 then
            Mon = "Brute"
            LevelQuest = 2
            NameQuest = "BuggyQuest2"
            NameMon = "Brute"
            CFrameQuest = CFrame.new(-1300, 5, 4000)
            CFrameMon = CFrame.new(-1200, 10, 4200)
        end
    elseif World2 then
        -- Aqui você pode adicionar a lógica para o World2, similar ao World1
        if MyLevel >= 1 and MyLevel <= 9 then
            Mon = "Bandit"
            LevelQuest = 1
            NameQuest = "BanditQuest1"
            NameMon = "Bandit"
            CFrameQuest = CFrame.new(1059.37195, 15.4495068, 1550.4231)
            CFrameMon = CFrame.new(1045.962646484375, 27.00250816345215, 1560.8203125)
        end
    elseif World3 then
        -- Aqui você pode adicionar a lógica para o World3, similar ao World1
        if MyLevel >= 1 and MyLevel <= 9 then
            Mon = "Bandit"
            LevelQuest = 1
            NameQuest = "BanditQuest1"
            NameMon = "Bandit"
            CFrameQuest = CFrame.new(1059.37195, 15.4495068, 1550.4231)
            CFrameMon = CFrame.new(1045.962646484375, 27.00250816345215, 1560.8203125)
        end
    end

    -- Lógica para setar a missão, inimigo e localizações
    if Mon then
        print("Missão: " .. NameQuest)
        print("Inimigo: " .. NameMon)
        print("CFrame da Missão: " .. tostring(CFrameQuest))
        print("CFrame do Inimigo: " .. tostring(CFrameMon))
        -- Aqui você pode adicionar o código para teleportar o jogador ou iniciar a missão
    end
end

-- Chama a função para verificar e definir a missão
CheckQuest()
