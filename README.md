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
