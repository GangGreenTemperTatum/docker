# SHELL [ "executable", "parameters" ]
# The SHELL instruction allows the default shell used for the shell form of commands to be overridden. 
# The default shell on Linux is ["/bin/sh", "-c"], and on Windows is ["cmd", "/S", "/C"]. The SHELL instruction must be written in JSON form in a Dockerfile.
# Common SHELL instructions for Windows are `cmd` and `powershell`
# SHELL instruction can appear multiple times and overrides based on top-down configuration precedence 

# RUN, CMD & ENTRYPOINT instructions are affected by the SHELL instruction

FROM mcr.microsoft.com/windows/servercore:ltsc2022
# Executed as cmd /S /C echo default
RUN echo default
# Execute as cmd /S /C powershell -command Write-Host default
RUN powershell -command Write-Host default
# Executed as powershell -command Write-Host hello
SHELL [ "powershell", "-command"]
RUN Write-Host hello
# Executed as cmd /S /C echo hello
SHELL ["cmd", "/S", "/C"]
RUN echo hello

# /windowsservercoreshell]$ docker image build -t ganggreentempertatum/windowsservercoreshell:v1.0 . -f Dockerfile
