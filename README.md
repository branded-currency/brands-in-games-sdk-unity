# GCOW Marketplace Unity SDK

## Description
This SDK is for including our webview for Mac/Android/iOS applications based on Unity.

## Features
- Displays a Gift Card Marketplace inside your Unity project.

## Quick guide
1. Download a zip archive with the asset and unzip it in a folder of your preference.
2. Open your project on Unity.
3. Go to "Assets" → "Import package" → "Custom package."
<img width="598" alt="3" src="https://user-images.githubusercontent.com/5966172/228291236-30c60abc-e3de-4750-8746-f96eb06899f8.png">

4. Choose the file `gcow-marketplace-sdk.unitypackage` on your disk.
5. Check that you have chosen all the needed files and dependencies and wait while it compiles.
<img width="369" alt="5_1" src="https://user-images.githubusercontent.com/5966172/228291402-de11a511-8eae-4474-997b-aa539101b686.png">

6. Go to "Unity" → "Settings" → "External Tools" and check that you have all the needed options for building an Android or iOS application (Android SDK, Xcode settings if required).
<img width="280" alt="6_1" src="https://user-images.githubusercontent.com/5966172/228291475-aba00271-84da-4611-80b3-c7514a8a1e3d.png">
<img width="1289" alt="6_2" src="https://user-images.githubusercontent.com/5966172/228291533-1a815cb0-4ea0-42a7-80e8-32454f4ada1e.png">

7. For Android: Go to "File" → "Build Settings" → "Player Settings" → "Publishing Settings" and check that you have the required Project Keystore and Project Key, provide your current one if you have it or create a new one.
<img width="648" alt="7_1" src="https://user-images.githubusercontent.com/5966172/228291577-09414733-ed6c-43a2-ae86-a3493917963a.png">
<img width="1183" alt="7_2" src="https://user-images.githubusercontent.com/5966172/228291616-e304bbb8-55af-4f0b-9cd3-ffbc0ee07b6d.png">

8. Now you can go to your scene structure in Unity and "Create empty" object.
<img width="227" alt="8_1" src="https://user-images.githubusercontent.com/5966172/228291739-e53662ca-c2f7-415c-88b3-f5f56dba5e76.png">
<img width="228" alt="8_2" src="https://user-images.githubusercontent.com/5966172/228291794-b601b776-9b13-4d90-a84a-55ae916815ef.png">

9. In the Inspector, choose "Add component" → "Scripts" and choose "Web View Handler."
<img width="284" alt="9" src="https://user-images.githubusercontent.com/5966172/228291817-39df67d5-5468-4bc9-9d07-2a146642bffc.png">

10. Fill in the required parameters `Uid`, `Placement ID`, `Placement Secret` and save your changes.
<img width="504" alt="10" src="https://user-images.githubusercontent.com/5966172/228291838-46d13152-646b-4b12-bffb-78596dc02c26.png">
