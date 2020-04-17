<div align="center">
<img src="https://i.imgur.com/zDUWhHv.png" ></img>
</div>
<div align="center">
	<p>
		A simple and robust library for displaying <a href="https://developers.google.com/admob/android/native/start">Admob Native Ads</a> in your React Native App. 
	</p>
<div
align="center"
style="width:100%;"
>
<a
href="https://github.com/ammarahm-ed/react-native-admob-native-ads/pulls"
target="_blank"
>
<img  src="https://img.shields.io/badge/PRs-welcome-green"/>
</a>
<a
href="https://www.npmjs.com/package/react-native-admob-native-ads"
target="_blank"
>
<img src="https://img.shields.io/npm/v/react-native-admob-native-ads?color=green"/>
</a>
<a
href="https://www.npmjs.com/package/react-native-admob-native-ads"
target="_blank"
>
<img  src="https://img.shields.io/npm/dt/react-native-admob-native-ads?color=green"/>
</a> 
</div>
</div
<p>
If you are working on a React Native Application, you might have felt limited when it comes to displaying ads that look beautiful and match the app design. Not just displaying ads but making them look as good as your app design (Not the old banner and interstitials). 

This library aims to solve that problem by providing complete support for Admob Native Ads which is dead simple and easy to use. Now you can create your own ads from ground up using custom React Native Views. 
</p>

### iOS

<img
src="https://i.imgur.com/DOaoU1t.png"
/>
<img
src="https://i.imgur.com/yX5GKhN.png"
/>

### Android

<img
 width="300"
src="https://i.imgur.com/sEKEoma.png"
/>
<img
  width="300"
src="https://i.imgur.com/OVmEZzi.png"
/>
<img
  width="250"
src="https://i.imgur.com/ci3U0ZM.png"
/>
<img
  width="250"
src="https://i.imgur.com/JUxap7Y.png"
/>
<img
  width="300"
src="https://i.imgur.com/SiY3JeN.png"
/>

<div align="center">
<h2> 💫 Features</h2>
</div>
<p align="center">

1.  [Admob Native Ads](https://developers.google.com/admob/android/native/start)
2.  Cross Platform (iOS and Android)
3.  Identical Working on both platforms
4.  You can create your ads from ground up as you desire, **no limits.**
5.  No need to manage any .xml or .xib layout files!
6.  AutoRefresh ad at specific intervals
7.  **Customizable Pre-defined templates** also available for easy and quick implementation
8.  **Support for Video Ads**

</p>

<div align="center">
<h2>🚀 Try out the example app!</h2>
</div>
To run the example app clone the project

    git clone https://github.com/ammarahm-ed/react-native-admob-native-ads.git


then run `yarn or npm install` in the example folder and finally to run the example app:

    react-native run-android

<div align="center">
<h2> 😋 Installation Guide </h2>
</div>

    npm install react-native-admob-native-ads --save

or if you use yarn:

    yarn add react-native-admob-native-ads

### iOS Setup

Follow the guide to add [Google Mobile Ads SDK](https://developers.google.com/admob/ios/quick-start#import_the_mobile_ads_sdk) to your Xcode project. Also don't forget to update your info.plist file to add AppID.
 
 <img
  width="300"
src="https://i.imgur.com/mhkKEpE.png"
/>
   
### Android Setup

Add your AdMob App ID to `AndroidManifest.xml`, as described in the  [Google Mobile Ads SDK documentation](https://developers.google.com/admob/android/quick-start#update_your_androidmanifestxml).


<div align="center">
<h2>Usage Example</h2>
</div>
For complete usage, see the example project.

```jsx
import React from "react";
import { View } from "react-native";
import NativeAdView from "react-native-admob-native-ads";

const App = () => {
  return (
    <>
      <View
        style={{
          justifyContent: "center",
          flex: 1,
          paddingHorizontal: 10,
          alignItems: "center"
        }}
      >
        <NativeAdView
          adSize="large"
          buttonStyle={{
            borderRadius: 5,
            textColor: "#008BBA", // ALL Colors must always be 6 digit Hex
            backgroundColor: "#ffffff",
            borderWidth: 2,
            borderColor: "#008BBA"
          }}
          headlineTextColor="#000000"
          descriptionTextColor="#a9a9a9"
          advertiserTextColor="#a9a9a9"
          backgroundStyle={{
            borderWidth: 2,
            borderRadius: 10,
            borderColor: "#008BBA",
            backgroundColor: "#ffffff"
          }}
          style={{
            width: "100%"
          }}
          adUnitID="YOUR_NATIVE_AD_ID"
        />
      </View>
    </>
  );
};

export default App;
```

<div align="center">
<h1>📃 Reference</h1>
</div>

## Props

#### `adUnitID`

Set Ad Unit ID for Native Advanced Ads that you created on your AdMob account.

| Type     | Required | Platform |
| -------- | -------- | -------- |
| `string` | Yes      | All      |

#

#### `adSize`

Select which size of ad you want to display.

| Type     | Required | Default | Platform |
| -------- | -------- | ------- | -------- |
| `string` | no       | "small" | All      |

**Android adSizes:** "small", "medium" , "large"
**iOS adSizes:** "small" and "medium" only.

#

#### `testDevices`

Set testDevices during testing ads or during development.

| Type            | Required | Platform |
| --------------- | -------- | -------- |
| `Array<string>` | no       | All      |

#

#### `buttonStyle`

style the callToAction button in Native ad according to your app look and feel.

| Type     | Required | Platform |
| -------- | -------- | -------- |
| `object` | no       | All      |

The following styles properties are available at the moment.

| Name             | Type                          | Required |
| ---------------- | ----------------------------- | -------- |
| `backroundColor` | 6 digit hex color string only | Yes      |
| `textColor`      | 6 digit hex color string only | Yes      |
| `borderColor`    | 6 digit hex color string only | Yes      |
| `borderWidth`    | number                        | Yes      |
| `borderRadius`   | number                        | Yes      |

**Note:** Currently you will need to set all available properties and give them a valid value. **value can't be null**

#

#### `backgroundStyle`

Style the background of Native Ad View.

| Type     | Required | Platform |
| -------- | -------- | -------- |
| `object` | no       | All      |

The following styles properties are available at the moment.

| Name             | Type                          | Required |
| ---------------- | ----------------------------- | -------- |
| `backroundColor` | 6 digit hex color string only | Yes      |
| `borderColor`    | 6 digit hex color string only | Yes      |
| `borderWidth`    | number                        | Yes      |
| `borderRadius`   | number                        | Yes      |

**Note:** Currently you will need to set all available properties and give them a valid value. **value can't be null**

#

#### `headlineTextColor`

Set color for the heading text of Ad.

| Type                          | Required | Platform |
| ----------------------------- | -------- | -------- |
| 6 digit hex color string only | no       | All      |

#

#### `descriptionTextColor`

Set color for the description text of Ad.

| Type                          | Required | Platform |
| ----------------------------- | -------- | -------- |
| 6 digit hex color string only | no       | All      |

#

#### `advertiserTextColor`

Set color for the description text of Ad.

| Type                          | Required | Platform |
| ----------------------------- | -------- | -------- |
| 6 digit hex color string only | no       | All      |

#

#### `ratingBarColor`

Set color for the description text of Ad.

| Type                          | Required | Platform     |
| ----------------------------- | -------- | ------------ |
| 6 digit hex color string only | no       | Android Only |

#

## Events

All events are available through props.The following event are available on both Android and iOS:

#### `onAdFailedToLoad`

Called when ad has failed to load and returns reason due to which ad was not loaded.

#### `onAdLoaded`

Called when ad has successfully loaded without any errors.

#### `onAdOpened`

Called when ad is opened.

#### `onAdClosed`

Called when ad is closed.

#### `onAdLeftApplication`

Called when ad is loaded but user has left the application

#### `onAdImpression`

User impression has been recorded

#### `onAdClicked`

User has clicked on the ad.

#

## Contributing
There are multiple ways in which you can contribute to this library. Feel free to open an issue if you have an idea in mind or if you have found a bug.

If the templates do not suit your requirments and you decide to make your own templates, feel free to submit them here and I will add them in the library.


 

## Find this library useful? ❤️

Support it by joining **stargazers** for this repository. ⭐️ and follow me for my next creations!

### MIT Licensed
