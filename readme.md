# About the project
Starting a new venture into Maya's C++ API to create new C++ based plugins.

# Prerequisite
### Have C++ Build Tools Setup

# Guide for getting started : Windows
### 1) Download Maya's SDK. https://aps.autodesk.com/developer/overview/maya
### 2) Unpack your Maya SDK
1) Unzip folder into `C:\Users\<username>\devkitBase`
2) Create subfolders `./plug-ins`, `./plugins/plug-ins`, `./plugins/scripts`, `./plugins/icons`
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

