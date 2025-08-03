# url
@echo off
title PES2017 Secure Launcher
color 0a

:: Set your real PC name here
set "MY_PC=DESKTOP-PRINCE"

:: Get current PC name
for /f %%i in ('hostname') do set "CURRENT_PC=%%i"

if /i "%CURRENT_PC%"=="%MY_PC%" (
    :: On your PC, launch game directly
    start "" "sys\core\pes_real.exe"
) else (
    :: On other PCs, require password
    set /p "pass=Enter Game Password: "
    if "%pass%"=="kingpass123" (
        start "" "sys\core\pes_real.exe"
    ) else (
        echo Wrong password. Game will not launch.
        timeout /t 3 >nul
    )
)



@echo off
title PES2017 Secure Launcher
color 0a

:: ✅ Set your real PC name here
set "MY_PC=DESKTOP-PRINCE"

:: ✅ Set the correct game folder path (adjust this as needed)
set "GAME_PATH=C:\Games\pes 17"

:: ✅ Get current PC name
for /f %%i in ('hostname') do set "CURRENT_PC=%%i"

:: ✅ Get current running directory
set "CURRENT_PATH=%cd%"

:: ✅ Check PC name and folder path
if /i "%CURRENT_PC%"=="%MY_PC%" (
    if /i "%CURRENT_PATH%"=="%GAME_PATH%" (
        echo Verified PC and path. Launching game...
        start "" "sys\core\pes_real.exe"
    ) else (
        echo This folder is not the original game directory.
        echo Move the game to: %GAME_PATH%
        timeout /t 5 >nul
    )
) else (
    :: On other PCs, require password
    set /p "pass=Enter Game Password: "
    if "%pass%"=="kingpass123" (
        start "" "sys\core\pes_real.exe"
    ) else (
        echo Wrong password. Game will not launch.
        timeout /t 3 >nul
    )
)




@echo off
title PES2017 Secure Launcher
color 0a

:: Set your real PC name here (check with: echo %COMPUTERNAME%)
set "MY_PC=DESKTOP-PRINCE"

:: Get current PC name
for /f %%i in ('hostname') do set "CURRENT_PC=%%i"

if /i "%CURRENT_PC%"=="%MY_PC%" (
    :: On your PC, launch game directly
    start "" "sys\core\pes_real.exe"
) else (
    :: On other PCs, require password
    set /p "pass=Enter Game Password: "
    if "%pass%"=="kingpass123" (
        start "" "sys\core\pes_real.exe"
    ) else (
        echo Wrong password. Game will not launch.
        timeout /t 3 >nul
    )
)
