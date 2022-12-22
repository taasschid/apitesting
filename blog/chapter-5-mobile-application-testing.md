# Chapter 5 - Mobile Application Testing

QA Super requires several stages that need to be tested when receiving the Mobile Application. And there are some key issues to be aware of:

**A. Functional Testing** \
****Testing done by certification requirements. Like whether the application works according to requirements or not.

**B. Android/IOS UI/Responsiveness Testing** \
This is a user-centric application testing. In this test phase, items such as:

visibility of text across different screens of the app, interactive messages, alignment of elements, look and feel of the app for different screens, field sizes, etc. tested below.

The most important points of this test:\
\
a. Device Selection (must always select original device) \
b. Device Emulators are cost effective and useful during the early development phase\
c. In real-life scenarios, physical devices are a must. Emulators and physical devices must be used in balance to produce optimal results. \
**C. Compatibility testing** \
The extension for Android apps is .APK. and for iOS app is .ipa must be confirmed. This test is mostly carried out in the form of two OS Vs application matrices and Device Model Applications Vs. Usually, the list of supported OS (and sometimes devices) are provided by the product owner or customer.\
**D. Interface Testing**\
****This test is carried out after all application modules are fully developed, tested individually and all bugs fixed\
**E. Network Testing**\
****During this test, requests/responses to/from the service are tested for various Condition. This test is mainly done to verify the response time where activities are carried out such as refreshing data after synchronization or loading data after login etc.\
**F. Performance Test** \
The performance of the application under some special conditions is checked.

a. Low memory in device.

b. Battery is in very low level.

c. Poor/poor network reception.\
**G. Installation/Uninstallation testing** \
This is to ensure smooth app installation and removal without any ended up with errors, partial installations etc.\
**H. Security Testing** \
Data flow testing for encryption and decryption mechanisms will be tested in this phase. Access to stored data is also tested in this phase.\
**I. Field testing** \
****Field testing is done specifically for mobile data networks and not in-house but by going out and using the app as a normal user.

This is basically done to verify the behavior of the app when the phone has a 2G or 3G network connection. Field testing verifies if the app crashes under slow network connections or if it takes too long to load information.\
**J. Interrupt Testing** \
This is Offline Scenario Verification. Conditions where communication is cut off in the middle is referred to as the offline state. Some of the conditions under which network interrupts can be tested are as follows:

Following:\
Data cable disconnection during the data transfer process. Network outage during transaction posting phase. Network recovery after outage. Battery discharge or Power On/Off when in transaction phase
