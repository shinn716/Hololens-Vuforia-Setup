# Hololens2-Vuforia-Setup
## Environment
 - **Windows SDK (10.0.22000)**  
 https://developer.microsoft.com/zh-tw/windows/downloads/windows-sdk/ 
 - Visual Studio 2019 (Extra adds UWP development/Desktop development with C++/Game development with Unity)  
 - Unity Version: 2020.3.11f1   
 - Vuforia Version: 10.2.5
 - MRTK Version: 2.7.2  
 __Recommend__  
 - Mixed Reality Feature Tool (Fast to setup MRTK)  
 https://www.microsoft.com/en-us/download/details.aspx?id=102778
  
## Install Vuforia into Unity
1. Import Assets from  
   https://assetstore.unity.com/packages/templates/packs/vuforia-hololens-1-2-sample-for-unity-2020-3-lts-101553  
3. Unity Build Settings -> UWP  
  
## Build And Depoly to hololens 
1. Build Settings / Player Settings / Capabilites /  
Check **PicturesLibrary**, **VideosLibrary**, **WebCam**, **Microphone**, **SpatialPerception** 
2. Build Settings / UWP / Build (Nothing to change) 
3. Build path ... / HololensDemo.sln (Open with Visual Studio 2019)  
4. Deploy Select Devices (Debug / ARM / Devices) / Run 

## Pair Developer Mode
1. 首先先將藍芽與開發的PC配對  
<img src="https://github.com/shinn716/Hololens-Vuforia-Setup/blob/main/images/Snipaste_2021-10-20_09-02-34.png"  alt="Cover" width="50%" /></a>  
2. Settings/Update&Security/ForDevelopers  
   所有選項都開啟(UseDeveloperFeatures/DevicesDiscovery/DevicePortal)  
<img src="https://github.com/shinn716/Hololens-Vuforia-Setup/blob/main/images/20211019_225739_HoloLens.jpg"  alt="Cover" width="50%" /></a>  
3. 回到 Visual Studio, 進行 Depoly, 第一次進行Depoly時, 會出現輸入 PIN 選單  
4. 需要回到 Hololens2 Settings/Update&Security/ForDevelopers DevicesDiscovery 選項, 按下Pair
5. 輸入 PIN  
6. 完成就可以進行 Depoly  
   
## Using the Windows Device Portal  
 https://docs.microsoft.com/en-us/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal  

## Live-streaming / Video Capture  
<img src="https://github.com/shinn716/Hololens-Vuforia-Setup/blob/main/images/Snipaste_2021-10-20_09-01-14.png" alt="Cover" width="50%"/></a>  
https://www.microsoft.com/store/productId/9NBLGGH4QWNX  
  
## Issue  
1. Certificate could not be opened: WSATestCertificate.pfx.  
如果更動 WSATestCertificate.pfx 可能會發生以上 error.  
解決辦法:  
<img src="https://github.com/shinn716/Hololens-Vuforia-Setup/blob/main/images/Snipaste_2021-10-20_08-38-38.png" /></a>  
<img src="https://github.com/shinn716/Hololens-Vuforia-Setup/blob/main/images/Snipaste_2021-10-20_09-06-01.png" alt="Cover" width="50%" /></a>  
2. Unable to active Windows Store app  
<img src="https://github.com/shinn716/Hololens-Vuforia-Setup/blob/main/images/Snipaste_2021-10-14_16-06-18.png" alt="Cover" width="50%" /></a>  
解決辦法:  
更動APP名稱, 在重新Depoly  
3. Hololens 無法連到 Windows Store, Error Code: 0x80131500
解決辦法:  
重置 Hololens, 開始地區選擇US.  
  
## Reference
 - UNITY MRTK Setup  
 https://www.youtube.com/watch?v=wSPXTRYxq9A
 - MRTK for Unity  
 https://github.com/microsoft/MixedRealityToolkit-Unity
 - Hololens+Vuforia setup in unity  
 https://www.youtube.com/watch?v=o0ybVu9SB7g  
 - Vuforia offical
 https://library.vuforia.com/articles/Solution/Working-with-the-HoloLens-sample-in-Unity.html  
   
# Others
## Install MRTK into Unity (Only use MRTK)
1. Unity Build Settings -> UWP
2. Player Settings / XR management -> Mixer Reality or OpenXR (Need to import ***Mixed Reality OpenXR Plugin*** from ***Mixed Reality Feature Tool***)
3. Import MRTK (Version 2.7.2) Foundation/Example/Extension or import example from ***Mixed Reality Feature Tool***.  
