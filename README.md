# Appium 1.6.4 with App Experience:

# Basic steps to start Appium server:

1)	Install the Appium installer on your Windows/Mac system. Start Appium client will show following launch screen.
https://github.com/sigosmobiletesting/Documents/blob/master/Appium1.jpg
2)	Open the new session window by File => New Session Window…



3)	Get the Appium URL from DeviceAnywhere Studio/Web Studio and copy the Appium URL at Remote Host field


4)	Add desired capabilities in the new session window as per the requirement to launch an Appium session. In below example, we have added capabilities to open our test app


5)	Start the session by “Start Session” button, it will open the Inspector with the visual representation of the state of the application

6)	In the middle part of the Inspector window, you can find XML representation of the app’s hierarchy of the current screen. Selecting any element will highlight the element and navigate it in the XML tree, and Tap and Send Keys can be used to Touch or enter the data respectively.



7)	With the help of Inspector, script can be created by using the suggested XPath or accessibility Id etc. For the above two screens, we have used following capabilities in our test script suggested but the Inspector, though XPath is not recommended but it is working:

driver.findElement(By.xpath("//*[1]//*[2]//*[1]//*[1]//*[1]//*[1]//*[1]//*[1]//*[3]//*[2]")).click();
driver.findElement(MobileBy.AccessibilityId("UI Interface")).click();
