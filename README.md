@echo off
title PES2017 Secure Launcher
color 0a

:: Replace this with your real PC name (get it from CMD > hostname)
set "MY_PC=YOUR_PC_NAME"

:: Get current PC name
for /f %%i in ('hostname') do set "CURRENT_PC=%%i"

:: Debug print (remove later)
echo MY_PC = %MY_PC%
echo CURRENT_PC = %CURRENT_PC%
pause

if /I "%CURRENT_PC%"=="%MY_PC%" (
    echo Welcome, launching PES...
    start "" "Data\launcher\theme\pes_real.exe"
) else (
    set /p pass=Enter password to launch PES: 
    if "%pass%"=="12345" (
        echo Password correct. Launching...
        start "" "Data\launcher\theme\pes_real.exe"
    ) else (
        echo Wrong password. Game will not launch.
        pause
    )
)
