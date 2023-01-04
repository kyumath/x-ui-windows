# x-ui-windows
binary executable release for win64

forked from 

https://github.com/HexaSoftwareTech/x-ui

------------------------------------------------------------------
# how to run :

just download from "release" and double click on xui-main.exe

- open browser [http://127.0.0.1:54321]
- user = admin
- pass = admin

note:

- allow xui-main.exe in windows firewall
- allow xray-windows-amd64.exe in windows firewall 

other usefull commands:

- xui-main.exe /?
- xui-main.exe -h
- xui-main.exe setting -show
- xui-main.exe setting -port 12345
- xui-main.exe setting -reset

------------------------------------------------------------------
# how to compile form source :

- download mingw[w64devkit] and extract to C:\
- add "C:\w64devkit\bin" to path
- download and install Go 1.19.3
- add "C:\Program Files\Go\bin" to path
- download and extract xui-windows source
- cd to xui-windows directory and run :
- go build -o main.exe main.go
- rename main.exe to xui-main.exe
- run xui-main.exe

enjoy with 127.0.0.1:54321
- user:admin
- pass:admin

you may need:
- allow xui-main.exe in windows firewall
- allow xray-windows-amd64.exe in windows firewall

reset setting by:
- xui-main.exe setting -reset

--------------------------------------------------------------------
# changelog
some minor changes applied in these file to get things ready for windows.
- \web\service\server.go
- \web\service\setting.go
- \web\entity\entity.go

---------------------------------------------------------------------
# known issue:
- resetting xraycore from web panel isnt working (you should manually close app to restart core)
- tcp/udp count set to 1 (linux api isnt available on windows)


