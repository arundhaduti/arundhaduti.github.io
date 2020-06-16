---
layout: post
title:  "Access dev tools for debugging iPhone/iPad Safari on Windows"
date:   2020-06-13 18:08:23 +0530
categories:
---
Came across this issue on a site where the site is crashing due to some reason on iPhone and wanted to debug. But since the debug tools is no longer on iOS(was there [way back in 2012][old iOS] I guess?), I was looking for an easier way to do it with my iPhone and desktop running Windows.

And unfortunately there aren't many resources online which descibe how this can be done. So while looking around I stumbled upon a github repo [remotedebug-ios-webkit-adapter][debugRepo] which is precisely what I was looking for. I have tested this and works fine.

Below are the steps that I followed:
1. Install [Node][node]
2. Install [Scoop][scoop]

	a. Run this command to install scoop
`Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')`

	b. While installing scoop you may see an error `PowerShell requires an execution policy in [Unrestricted, RemoteSigned, ByPass] to run Scoop.` 
	
	Run the below command to set execution policy(Press Y and enter when prompted) and then run command 2.a again to complete it's installation.
	
	`Set-ExecutionPolicy RemoteSigned -scope CurrentUser`
3. Run the below commands to install ios-webkit-debug-proxy

	`scoop bucket add extras`

	`scoop install ios-webkit-debug-proxy`
4. In cmd run the below command as adminstrator to install latest version of the adapter

	`npm install remotedebug-ios-webkit-adapter -g`
5. Install iTunes and connect your device to PC. (Tap on 'trust' when pop-up displayed on your phone to trust the computer). Make sure Web Inspector is enabled in iOS Settings > Safari > Advanced
6. Run the adapter using below command 

	`remotedebug_ios_webkit_adapter -— port=9000`
7. Now tht the adapter is listening, open chrome and go to this link `chrome://inspect/#devices` and click on 'Configure...' next to Discover network targets and add `localhost:9000`
8. Open the web page you want to debug on safari, you should see it on chrome inspector page under Remote Target - Target (RemoteDebug iOS Webkit Adapter)
9. Click on inspect and you can access the console and network tabs to see if any errors to debug.&nbsp;

&nbsp;



Below is reference url if need more info

[https://github.com/RemoteDebug/remotedebug-ios-webkit-adapter][debugRepo]



[old iOS]: https://www.dummies.com/web-design-development/how-to-use-developer-tools-in-safari-on-ios/
[node]: https://nodejs.org/en/download/
[scoop]: https://scoop.sh/
[debugRepo]: https://github.com/RemoteDebug/remotedebug-ios-webkit-adapter
