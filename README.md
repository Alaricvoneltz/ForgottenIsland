# Cara Menggunakan Library

## Panggil library (Ganti dengan loadstring jika di-host online, atau paste langsung)
local AlaricLib = -- [Masukkan script library di atas di sini atau loadstring]

## Buat Jendela Utama
local Window = AlaricLib:CreateWindow("Alaric Hub")

## Buat Tab 1: Menu Utama
local Tab1 = Window:CreateTab("Utama")

Tab1:CreateButton("Tekan Tombol", function()
    print("Tombol berhasil ditekan!")
end)

Tab1:CreateToggle("Auto Farm", function(state)
    print("Status Auto Farm:", state)
end)

Tab1:CreateNumberInput("Masukkan Kecepatan (Angka)", function(val)
    print("Nilai angka:", val)
end)

Tab1:CreateTextInput("Masukkan Pesan Teks", function(text)
    print("Pesan diketik:", text)
end)

Tab1:CreateDropdown("Pilih Senjata", {"Pedang", "Panah", "Tombak"}, function(selected)
    print("Senjata dipilih:", selected)
end)

## Buat Tab 2: Pengaturan
local Tab2 = Window:CreateTab("Pengaturan")
Tab2:CreateButton("Reset Karakter", function()
    game.Players.LocalPlayer.Character:BreakJoints()
end)
