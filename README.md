<a href="https://brandsingames.com/">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://brandsingames.com/images/brandsingames-light-logo.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://brandsingames.com/images/brandsingames-dark-logo.svg">
    <img width="300" alt="Brands In Games" src="https://brandsingames.com/images/brandsingames-dark-logo.svg">
  </picture>
</a>

# Brands In Games Monetization SDK for Unity

Driving Acquisition, Retention, and Monetization for Free-to-Play Mobile Games with the <a href="https://brandsingames.com/">Brands In Games</a>!

<img width="270" alt="Brands In Games" src="https://github.com/branded-currency/brands-in-games-sdk-unity/assets/5966172/a5af060b-4835-479f-9888-76e39e45c05e">

## Description
Our Marketplace unlocks a new revenue stream for free-to-play mobile games. 
Your players purchase digital gift cards from 400+ brands and merchants they know and love, 
Amazon, Best Buy, Domino’s Pizza, Ulta Beauty, Fanatics, and more. 
Our Marketplace allows players to earn instant free in-app currency toward the game they are playing, 
allowing them to get back to enjoying your game and creating a revenue stream for publishers that can 
earn them as much as $40 per engaged user per month.

This SDK is for including our webview for Mac/Android/iOS applications based on Unity.

## Features
- Display our Brands In Games inside your Unity mobile game or app.

## Quick guide

### Account creation
- Create a Sandbox Developer Account (www.test-brandsingames.com)
- Add new placement in Brands In Games Developer Portal and copy the given credentials.
- Import our unity package in your project
- Customize the Marketplace with your desired branding and colors.
- Test and move over to our Production Portal
- If you need any support, click the Slack icon inside your Brands In Games Developer Portal and we will assist you in our slack channel. 

### SDK package import
1. Download a zip archive with the asset and unzip it in a folder of your preference.
2. Open your project on Unity.
3. Go to "Assets" → "Import package" → "Custom package."
<img width="598" alt="3" src="https://user-images.githubusercontent.com/5966172/228291236-30c60abc-e3de-4750-8746-f96eb06899f8.png">

4. Choose the file `brands-in-games-sdk.unitypackage` on your disk.
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

10. Fill in the required parameters `Uid`, `Placement ID`, `Placement Client Key` and save your changes. 
You can find your placement ID and Client Key in your placement page on Brands In Games portal. 
For UID any user identifier can be used or leave it empty.

Set `Base Url` to: 
- `https://app.brandsingames.com` for production
- `https://app.test-brandsingames.com` for test
<img width="519" alt="10" src="https://github.com/user-attachments/assets/a0d4e54e-814a-4c4b-a685-43868352af11" />


### SDK launching
1. Create a new button by clicking "+", name it e.g. "ButtonOpenMarketplace" and select.
<img width="425" src="https://github.com/user-attachments/assets/cf36fa1c-e58a-4b1b-8397-f338c817f45d">
<img width="397" src="https://github.com/user-attachments/assets/496b6e83-3be5-42ff-8492-e6e039d688e8">

2. Add On Click handler inside Inspector tab.
<img width="580" src="https://github.com/user-attachments/assets/793be3c4-a505-49a4-9c61-c54c16c7d844">

3. Select "Brands In Games WebView" object on Scene tab inside opened window.
<img width="577" src="https://github.com/user-attachments/assets/e606be65-9008-4750-840f-18e6daa5f93f">

4. Select `WebViewHandler.Start` function as click event handler.
<img width="578" src="https://github.com/user-attachments/assets/7089a94a-7160-4f6c-803f-28ec596b0fb1" />

5. Since you added button, you may need to avoid script auto launching. For this uncheck your object script in Inspector.
<img width="412" src="https://github.com/user-attachments/assets/4c403353-512d-41a8-8f46-27b14cd167fd" />


### Events

- `onOpened` fired when SDK webview opened, before any data loaded inside webview
- `onClosed` fired after SDK webview closed by user

<details>
  <summary>How to create events handler</summary>

  1. Create custom script e.g. `WebviewEventsHandler`
  2. Add property for web view handler `public WebViewHandler webviewRef = null;`
  3. Connect `Brands In Games WebView` to with webviewRef

  <img width="478" alt="" src="https://github.com/user-attachments/assets/b203b17d-1f29-4f74-9cee-ee66235e86c0" />

  <details>
    <summary>Events handler example</summary>

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class WebviewEventsHandler : MonoBehaviour
{
    public WebViewHandler webviewRef = null;

    // Start is called before the first frame update
    void Start()
    {
        if (webviewRef) {
            webviewRef.onOpened += myOnOpenedHandler;
            webviewRef.onClosed += myOnClosedHandler;
        }
    }

    void myOnOpenedHandler()
    {
        Debug.Log("Test onOpened");
    }

    void myOnClosedHandler()
    {
        Debug.Log("Test onClosed");
    }

    // Update is called once per frame
    void Update()
    {
        
    }
}
```

  </details>
</details>