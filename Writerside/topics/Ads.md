# Ads

Unity Ads is a mobile advertising for iOS & Android that delivers market leading revenue from your player base, while increasing engagement and retention.

To start using it:

1. Navigate to Window > Services > Ads
2. Click the switch on the right to turn it on, then answer a few options, like platforms and age of targeted audience

There are two code samples

* **Simple**: simple full screen interstitial ads (for example for appear between game levels)
* **Rewarded**: shows an ad with a result callback, you can use it to give your players rewards for watching ads

An example function

```C#
Using UnityEngine.Advertisements;

...

public void showAdd() {
  if (Advertisement.IsReady()) {
    Advertisement.Show();
  }
}
```