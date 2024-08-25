# About the project
Starting a new venture into Maya's C++ API to create new C++ based plugins.

# Prerequisite
### Have C++ Build Tools Setup

# Guide for getting started : Windows
### 1) Download Maya's SDK. https://aps.autodesk.com/developer/overview/maya
### 2) Unpack your Maya SDK
1) Unzip folder into `C:\Users\<username>\devkitBase`
2) Create subfolders `./plug-ins`, `./plugins/plug-ins`, `./plug-ins/scripts`, `./plug-ins/icons`
3) Create Environment variables  
Name: `DEVKIT_LOCATION` Value: `C:\Users\<Username>\devkitBase\`  
Name: `MAYA_LOCATION` Value: `"C:\Program Files\Autodesk\<maya_version>"`
4) Create Path  
Value: `<MayaLocation>\bin`
### 3) Edit Maya .env file `C:\Users\<Username>\Documents\maya\<version_number>\Maya.env`
```
 MAYA_PLUG_IN_PATH=C:\Users\<Username>\devkitBase\plug-ins\plug-ins
 MAYA_SCRIPT_PATH=C:\Users\<Username>\devkitBase\plug-ins\scripts
 XBMLANGPATH=C:\Users\<Username>\devkitBase\plug-ins\icons
 ```

# Setting up Windows Dev for VS Code / Normal Powershell
Auto setup temporary environment for Windows specific build --The windows SDK of Maya uses many cl specific commands.
`C:\Program Files\Microsoft Visual Studio\2022\Community\VC\Auxiliary\Build\vcvarsall.bat` Potential Location of your VCVARSALL file

Instead of using Developer Powershell you can also setup a default function by changing your `$PROFILE` for powershell  
simply typing `notepad $PROFILE` to edit the config in notepad or `nvim $PROFILE` if you have neovim installed. 
```powershell
function set-msvc {
	& "C:\Program Files\Microsoft Visual Studio\2022\Community\VC\Auxiliary\Build\vcvarsall.bat" x64
}
```

`C:\Program Files\Microsoft Visual Studio\2022\Community\MSBuild\Current\Bin\amd64` MSBuild (Build System Optional)

`C:\Program Files\Microsoft Visual Studio\2022\Community\VC\Tools\MSVC\14.41.34120\include` Microsoft MSBuild header files
`C:\Program Files (x86)\Windows Kits\10\Include\10.0.22621.0\ucrt` Microsoft windows ucrt header files
`C:\Program Files (x86)\Windows Kits\10\Include\10.0.22621.0\shared` Micorosft windows shared header files

`C:\Program Files\Microsoft Visual Studio\2022\Community\VC\Tools\MSVC\14.41.34120\lib\x64` Micorosoft MSbuild lib files
`C:\Program Files (x86)\Windows Kits\10\Lib\10.0.22621.0\ucrt\x64` Microsoft windows ucr:t 64bit lib files
`C:\Program Files (x86)\Windows Kits\10\Lib\10.0.22621.0\um\x64` Micorosft windows um 64bit lib files
