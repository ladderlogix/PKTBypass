 [![HitCount](https://hits.dwyl.com/sglombicki/PKTBypass.svg?style=flat-square)](http://hits.dwyl.com/sglombicki/PKTBypass)
# Packet Tracer Activity Password Bypass
This bypass the password on packet tracer quiz files. This Can be used to recover cisco packet tracer file passwords.

## How you fix your packet tracer
Go to release and download the exe and replase the PacketTracer.exe file in C:\Program Files\{Version}\bin\ with the patched one

## Is this safe?
Yes you can hex diff your file and mine and will see that only 4 bytes are changed to allow the instruction change. This is also undetectable if used on an assignment.

## How I found it
Searching for the string "Please enter your password:". I notice a jz right before it. I patch this in ghidra to a jmp. This is forcing the check to see if a password is required on this file to always jump to the condition if there is no password on this file. The password on the packet tracer file does not do any encryption. 
![image](https://github.com/SGlombicki/PKTBypass/assets/54868891/e8630f1e-8723-413c-afc0-9ac43184aa44)
