# How to Build the SpectatorView Plugin for MRTK

## Install Vcpkg

- Open a Command Prompt
- Navigate to a folder in which you would like to store your repositories (ex: c:\git)
- git clone <https://github.com/Microsoft/vcpkg>
- cd vcpkg
- git checkout 068032bc548817a04709970f76268a6d7b1767c7
- .\bootstrap-vcpkg.bat
- .\vcpkg integrate install

>NOTE: The above line requires the Command Prompt to be running as an Administrator.

## Install OpenCV Contrib for UWP

- .\vcpkg install opencv[contrib]:x86-uwp --recurse

>NOTE: Copy the above line exactly (the []s do not indicate an optional value).

## Building the Plugin

- Navigate to your Git repository folder (ex: c:\git)
- git clone <https://github.com/Microsoft/MixedRealityToolkit.git>
- Open the .sln file located in MixedRealityToolkit\SpectatorViewPlugin\SpectatorViewPlugin\SpectatorViewPlugin.sln
- Set the build options to Release and x86, then build the solution.

## Add the DLLs to your Project

Copy the following dlls from the directory MixedRealityToolkit\SpectatorViewPlugin\SpectatorViewPlugin\Release\SpectatorViewPlugin to the directory HoloToolkit-Preview\SpectatorView\Plugins\WSA\x86. If that directory doesn't exist please create it.

- opencv_aruco341.dll
- opencv_calib3d341.dll
- opencv_core341.dll
- opencv_features2d341.dll
- opencv_flann341.dll
- opencv_imgproc341.dll
- zlib1.dll
- SpectatorViewPlugin.dll
