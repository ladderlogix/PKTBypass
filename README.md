# PKTBypass
This bypass the password on packet tracer quiz files

## How I found it
Searching for the string "Please enter your password:". I notice a jz right before it. I patch this in ghidra to a jmp
![image](https://github.com/SGlombicki/PKTBypass/assets/54868891/e8630f1e-8723-413c-afc0-9ac43184aa44)

## How you fix your packet tracer
Go to release and download the exe and replase the PacketTracer.exe file in C:\Program Files\{Version}\bin\ with the patched one
