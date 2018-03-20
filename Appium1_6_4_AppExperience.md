# Appium 1.6.4 Inspector with App Experience:

## Prerequisites:
1. Appium 1.6.4 only
2. App Experience Studio 8.6 or later
3. App Experience account - [Get a new account now](http://www.keynote.com/solutions/testing/microsoft-visual-studio-team-foundation-server-integration)
4. App Experience custom Appium 1.6.4 Inspector [Download](https://sigoscloud-my.sharepoint.com/personal/moorthi_subramani_sigos_com/Documents/Forms/All.aspx?slrid=4fd5379e-9042-4000-aa79-74ffbcf67741&RootFolder=%2Fpersonal%2Fmoorthi_subramani_sigos_com%2FDocuments%2FAppiumDesktop&FolderCTID=0x0120002F200F5631F71B4681B71D8A06976BEF)
5. Node.js (version 6.10.x) - [Node.js](https://nodejs.org/en/)

### Steps to start Appium Inspector and find Elements:

1)	Install the Appium installer on your Windows/Mac system. Start Appium client will show following launch screen.


![Image1](https://github.com/sigosmobiletesting/Documents/blob/master/Images/Appium1.jpg)


2)	Open the new session window by File => New Session Window…


![Image2](https://github.com/sigosmobiletesting/Documents/blob/master/Images/Appium2.jpg)

![Image3](https://github.com/sigosmobiletesting/Documents/blob/master/Images/Appium3.jpg)


3)	Get the Appium URL from DeviceAnywhere Studio/Web Studio and copy the Appium URL at Remote Host field (make sure App Experience / Appium traffic not blocked by any proxy)


![Image4](https://github.com/sigosmobiletesting/Documents/blob/master/Images/Appium4.jpg)

![Image5](https://github.com/sigosmobiletesting/Documents/blob/master/Images/Appium5.jpg)


4)	Add desired capabilities in the new session window as per the requirement to launch an Appium session. In below example, we have added capabilities to open our test app


![Image6](https://github.com/sigosmobiletesting/Documents/blob/master/Images/Appium6.jpg)


5)	Start the session by “Start Session” button, it will open the Inspector with the visual representation of the state of the application

![Image7](https://github.com/sigosmobiletesting/Documents/blob/master/Images/Appium7.jpg)


6)	In the middle part of the Inspector window, you can find XML representation of the app’s hierarchy of the current screen. Selecting any element will highlight the element and navigate it in the XML tree, and Tap and Send Keys can be used to Touch or enter the data respectively.


![Image8](https://github.com/sigosmobiletesting/Documents/blob/master/Images/Appium8.jpg)

![Image](https://github.com/sigosmobiletesting/Documents/blob/master/Images/Appium9.jpg)


7)	With the help of Inspector, script can be created by using the suggested XPath or accessibility Id etc. For the above two screens, we have used following capabilities in our test script suggested by the Inspector:

driver.findElement(By.xpath("//*[1]//*[2]//*[1]//*[1]//*[1]//*[1]//*[1]//*[1]//*[3]//*[2]")).click();
driver.findElement(MobileBy.AccessibilityId("UI Interface")).click();
