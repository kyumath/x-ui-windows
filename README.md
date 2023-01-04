# x-ui-windows
**binary executable for windows 64-bit**

forked from

https://github.com/HexaSoftwareTech/x-ui  (V0.5.4)


------------------------------------------------------------------
# how to run :

- download from "release"
- double click on xui-main.exe
- open browser [http://127.0.0.1:54321]
- user = admin
- pass = admin

**windows firewall:**

- allow xui-main.exe in windows firewall
- allow xray-windows-amd64.exe in windows firewall 

**(optional) Block IR/China/Bittorrent/Ads/P0*n:**

- paste configuration inside xray_core_config.txt into "panel setting" -> "xray configuration" to block these IPs/Sites

**(optional) self-signed certificate:**

- you can use fake cert inside self_certificate to bypass GFW censorship or make your own certificate using openssl.exe
- client must check "allow Insecure" to accept these certificate because its not authorized by Root-CA

**other usefull commands:**

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


