# Hololens2-Vuforia-Setup
## Environment
 - **Windows SDK (10.0.22000)**  
 https://developer.microsoft.com/zh-tw/windows/downloads/windows-sdk/ 
 - Visual Studio 2019 (Extra adds UWP development/Desktop development with C++/Game development with Unity)  
 - Unity Version: 2020.3.11f1, 2019.4.28f1  
 - Vuforia Version: 10.2.5
 - MRTK Version: 2.7.2  
 __Recommend__  
 - Mixed Reality Feature Tool (Fast to setup MRTK)  
 https://www.microsoft.com/en-us/download/details.aspx?id=102778

## Install MRTK / Vuforia into Unity
1. Unity Build Settings -> UWP
2. Player Settings / XR management -> Mixer Reality or OpenXR (Need to import ***Mixed Reality OpenXR Plugin*** from ***Mixed Reality Feature Tool***)
3. Import Vuforia SDK (Version 10.2.5) .unitypackage
4. Import MRTK (Version 2.7.2) Foundation/Example/Extension or import example from ***Mixed Reality Feature Tool***.  
5. Hololens+Vuforia setup in unity  
https://www.youtube.com/watch?v=o0ybVu9SB7g  
6. Vuforia in hololens, follow project setup.  
https://library.vuforia.com/articles/Solution/Working-with-the-HoloLens-sample-in-Unity.html  

## Build And Depoly to hololens 
1. Build Settings / Player Settings / Capabilites /  
Check **PicturesLibrary**, **VideosLibrary**, **WebCam**, **Microphone**, **SpatialPerception** 
2. Build Settings / UWP / Build (Nothing to change) 
3. Build path ... / HololensDemo.sln (Open with Visual Studio 2019)  
4. Deploy Select Devices (Debug / ARM / Devices) / Run 

## Using the Windows Device Portal  
 https://docs.microsoft.com/en-us/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal  

## Live-streaming / Video Capture  
https://www.microsoft.com/store/productId/9NBLGGH4QWNX  

## Others
 - UNITY MRTK Setup  
 https://www.youtube.com/watch?v=wSPXTRYxq9A
 - MRTK for Unity  
 https://github.com/microsoft/MixedRealityToolkit-Unity
