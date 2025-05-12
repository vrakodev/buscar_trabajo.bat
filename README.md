// by ｖｒａｋｏｄｅｖ

@echo off
:: Habilitar expansión retardada de variables
setlocal enabledelayedexpansion

:: Ruta del escritorio del usuario actual
set "desktopPath=%USERPROFILE%\Desktop"

:: URL de la página
set "url=https://www.infojobs.net/"

:: Crear 5 accesos directos
for /l %%i in (1,1,5) do (
    set "shortcutPath=!desktopPath!\InfoJobs Shortcut %%i.url"
    (
        echo [InternetShortcut]
        echo URL=%url%
    ) > "!shortcutPath!"
)

echo Se han creado 5 accesos directos en el escritorio con la página %url%.
pause
