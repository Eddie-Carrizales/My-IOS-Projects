# Pre-work - *Tipper*

**Tipper** is a tip calculator application for iOS.

Submitted by: **Edilberto F. Carrizales Cavazos**

Time spent: **About 20** hours spent in total

## User Stories

The following **required** functionality is complete:

* [✅] User can enter a bill amount, choose a tip percentage, and see the tip and total values.
* [✅] User can select between tip percentages by tapping different values on the segmented control and the tip value is updated accordingly

The following **optional** features are implemented:

* [✅] UI animations
* [ ] Remembering the bill amount across app restarts (if <10mins)
* [✅] Using locale-specific currency and currency thousands separators.
* [ ] Making sure the keyboard is always visible and the bill amount is always the first responder. This way the user doesn't have to tap anywhere to use this app. Just launch the app and start typing.

The following **additional** features are implemented:

- List anything else that you can get done to improve the app functionality!
- [✅] Added a slider which updates as you slide and shows from 0% - 30%
- [✅] Added a Split check functionality allowing the total to be split by any number of people (integers)
- [✅] Added a settings view controller to allow more app settings
- [✅] Added a segmented controller which allows the user to change the theme of the app to 4 different colors
- [✅] Added a picker view which allows the user to change the currency symbol in the app
- [✅] Added a thousands separator for larger numbers
- [✅] Made the keyboard only a numeric keypad to allow easier input and only numbers and decimals
- [✅] Added a "done" and "cancel" button to the top of the keypad to allow for easier way to hide the keyboard
- [✅] Designed an app icon using sketch so that multiple devices could see an app logo
- [✅] Added a nice user user interface with calm colors and easy to understand descriptors
- [✅] Had family members test the app and received feedback which led me to add a "calculate total" button which would update the totals once clicked (to avoid total cost confusion)
- [✅] Added a Split check switch which is a nice intuitive UI addition and works sort of like a boolean to make sure the user actually wants split check
- [✅] When any of the totals is not a calculation they both automatically revert back to zero to avoid user confusion
- [✅] Added user defaults saving capability to the theme color and the currency symbol chosen by the user, this setting will prevail even after app restart

## Video Walkthrough

Here's a walkthrough/Demo of the App:

[](https://imgur.com/ed7AkAX)

GIF created with https://imgur.com

## Notes

Describe any challenges encountered while building the app.
There were a couple of challenges while building the app.
1. Since I did not know anything about Swift and this was a prework I was pretty much learning on my own and experimenting with the code and the different buttons, labels, segmented controllers, text fields, slider, and a picker view.
2. After getting more familiar and finishing the first view controller, I wanted to add the settings screen and thus learned how to add a navigation panel and a second view controller. This posed a challenge since I did not know how to add a second one nor did I know how to connect the first one to the second and move between them. I finally figured out how to do it and added some transitions.
3. The first most challenging step was sending data between each view controller. At first I sending the data through a reference from the second view controller to the first, but this was not working as expected, I also tried another method with protocols, but the documentation found online was getting confusing. I ultimately ended up using singletons and managed to pass the theme and currency symbol information back to the first view controller.
4. The second most challenging step was saving the theme and the currency symbol to user defaults in both view controllers. Initially I struggled but managed to save it in the second view controller where the user choice was being made. After sending the data back to the first view controller I also struggled a lot to save the theme but ultimately managed to make it work.
4. The constrains were also a bit challenging and I learned about a small pyramid symbol at the bottom of the main pane where it would add and update the constrains automatically. However, I still have some warning regarding these constrains that I needed to fix to avoid weird formats on other iphones, the current Iphone I tested the format with was the iphone 13
5. I decided to also test the app directly on my iphone by signing it and downloading it on my iphone and family members and noticed that the format was acting strange to which I found out that darkmode was affecting the style of the app and thus I had to modify the info.plist to have the UIUserStyle always on "light" regardles of user mode (this fixed the issue and app worked great), and even though my app has no dark mode I added 4 different theme colors for the user which I preferred.


## License

    Copyright [2021] [Edilberto F. Carrizales Cavazos]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
