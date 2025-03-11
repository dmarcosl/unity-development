# Analytics

Unity Analytics is a simple but powerful data platform that provides analytics for your Unity game.

Analytics provides the data you need to manage your relationship with your players.

Platforms supported are:

* iOS
* Android
* Tizen
* Windows Phone 8.1
* Windows 8.1 & Windows 10
* Mac, PC, Linux Standalone
* WebGL 5.3 onwards

Enable Analytics is the same way to enable Ads. You must hit Play in the project to validate the connection to Unity Analytics.

The Unity Editor acts as a test environment to validate the Analytics integration. When the Play button is pressed, the Editor sends data to the analytics service. This can test the analytics without having to build and publish the game.

You can check that the project is validated by going to the Analytics Dashboard of the project, Services windows > Analytics > Go To Dashboard. The dashboard is open in a web browser.

In the Analytics Dashboard you can check:

* New installs
* Daily active users (DAU)
* Monthly active users (MAU)
* Total sessions
* Sessions per user
* Time spent in app
* User Segments for Country and Platform
* Player behavior data
* Revenue data
* Demographics data
* Data segmentation
* Heatmaps (visualize Analytics events spatially in your game)

You can create custom events, of any specific in-game action that a user can perform. This allows to track player behavior that Analytics does not track automatically, such as achievement, scene change, entering a store, etc.

There are two ways to do this:

* Using the AnalyticsTracker component on a GameObject
* Calling the Analytics.CustomEvent function in a script

```C#
using System.Collections.Generic;

int totalPotions = 5;
int totalCoins = 100;
string weaponID = "Weapon_102";

Analytics.CustomEvent("gameOver", new Dictionary<string, object>
{
  { "potions", totalPotions },
  { "coins", totalCoins },
  { "activeWeapon", weaponID }
});
```