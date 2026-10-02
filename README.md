# PocketPet Hamster

A Unity project (6000.5.10f1) with the hamster pet and all 8 animations ready to use: idle, happy, sad, crying, eating, playing, studying, sleeping.

## Get it

Mac Terminal or Windows Git Bash:

```bash
cd ~/Desktop
git clone https://github.com/Zeref538/PocketPet-Hamster.git
```

No Git? On GitHub click the green **Code** button, then **Download ZIP**, and unzip it.

## Open it in Unity

1. Open **Unity Hub**, click **Add**, then **Add project from disk**.
2. Pick the `PocketPet-Hamster` folder.
3. Open `Assets/Scenes/Hamster.unity` and press **Play**.
4. Press keys **1** to **8** to switch animation.

The first open takes a few minutes while Unity builds its cache.

## Use it in your own code

The Animator has one number, `Mood`. Set it to switch animation:

```csharp
GetComponent<Animator>().SetInteger("Mood", 4);   // 4 = eating
```

0 idle, 1 happy, 2 sad, 3 crying, 4 eating, 5 playing, 6 studying, 7 sleeping.

To rebuild the clips after changing frames: menu **PocketPet > Build Hamster**.
