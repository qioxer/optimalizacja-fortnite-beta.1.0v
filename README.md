# 🎮 Fortnite Optimizer - FPS Boost! 🚀

🔧 Skrypt batch optymalizujący Fortnite! Zwiększa FPS, redukuje lagi i przyspiesza grę. 😎

## ⚡ Funkcje:
✅ Czyszczenie pamięci podręcznej 🧹  
✅ Wyłączanie zbędnych procesów 🚫  
✅ Optymalizacja rejestru ⚙️  
✅ Defragmentacja plików 🗂️  
✅ Naprawa plików Fortnite 🔍  

## 🚀 Jak używać?
1️⃣ Pobierz `.bat`  
2️⃣ Uruchom jako administrator  
3️⃣ Wybierz opcję i gotowe!  

🎯 **Więcej informacji i wsparcie znajdziesz na naszym Discordzie!**  
🔗 **Dołącz teraz:** [Discord Server](https://discord.gg/237vh7pt) 💬🔥  

## 🖥️ Kod źródłowy:
```batch
@echo off
chcp 65001 > nul
color 0A
title Fortnite Optimizer
:menu
cls
echo ========================================
echo    🎮 FORTNITE MULTI-TOOL OPTIMIZER 🚀
echo ========================================
echo 1. Czyszczenie pamięci podręcznej gry
echo 2. Wyłączenie zbędnych procesów
echo 3. Zoptymalizowanie ustawień rejestru
echo 4. Defragmentacja plików Fortnite
echo 5. Naprawa plików Fortnite
echo 6. Wyjście
echo ========================================
echo.
set /p choice=Wybierz opcję (1-6): 

if "%choice%"=="1" goto clear_cache
if "%choice%"=="2" goto disable_processes
if "%choice%"=="3" goto optimize_registry
if "%choice%"=="4" goto defrag_files
if "%choice%"=="5" goto repair_files
if "%choice%"=="6" exit

echo Nieprawidłowa opcja. Spróbuj ponownie.
pause
goto menu

:clear_cache
cls
echo 🧹 Czyszczenie pamięci podręcznej Fortnite...
del /s /q "%localappdata%\FortniteGame\Saved\Config\WindowsClient" > nul
del /s /q "%localappdata%\FortniteGame\Saved\Logs" > nul
echo ✅ Pamięć podręczna wyczyszczona!
pause
goto menu

:disable_processes
cls
echo 🚫 Wyłączanie zbędnych procesów...
taskkill /F /IM EpicGamesLauncher.exe > nul
taskkill /F /IM OneDrive.exe > nul
taskkill /F /IM XboxGameOverlay.exe > nul
echo ✅ Procesy wyłączone!
pause
goto menu

:optimize_registry
cls
echo ⚙️ Optymalizacja rejestru...
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management" /v LargeSystemCache /t REG_DWORD /d 1 /f > nul
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\PriorityControl" /v Win32PrioritySeparation /t REG_DWORD /d 26 /f > nul
echo ✅ Rejestr zoptymalizowany!
pause
goto menu

:defrag_files
cls
echo 🗂️ Defragmentacja plików Fortnite...
defrag C: /O > nul
echo ✅ Defragmentacja zakończona!
pause
goto menu

:repair_files
cls
echo 🔍 Naprawa plików Fortnite...
start "" "C:\Program Files\Epic Games\Launcher\Portal\Binaries\Win64\EpicGamesLauncher.exe" -Verify
pause
goto menu
```

💡 **Pomysły? Daj znać!** 📝
