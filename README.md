# PocketPet Hamster

A **Universal 2D** Unity project (URP with the 2D Renderer, set up the same way as Shadow) with the hamster pet, all 8 animations, a room background and three buttons. Uses **Unity 6000.5.10f1**.

## Get it

Mac Terminal or Windows Git Bash:

```bash
cd ~/Desktop
git clone https://github.com/Zeref538/PocketPet-Hamster.git
```

Already cloned it before? Make your copy match GitHub exactly:

```bash
cd ~/Desktop/PocketPet-Hamster
git fetch origin && git reset --hard origin/main
```

No Git? On GitHub click the green **Code** button, then **Download ZIP**, and unzip it.

## Open it in Unity

1. Open **Unity Hub**, click **Add**, then **Add project from disk**.
2. Pick the `PocketPet-Hamster` folder.
3. Make sure the version shown is **6000.5.10f1**, then open it. The first open takes a few minutes.
4. Open `Assets/Scenes/SampleScene.unity` and press **Play**.
5. Click the buttons on the right: **food** makes it eat, **heart** makes it happy, **controller** makes it play. After 3 seconds it goes back to idle.

## What is where

- `Assets/Sprites/Hamster/`: 33 frames, feet pinned to one spot so it animates in place
- `Assets/Animations/Hamster/`: the 8 clips and `Hamster.controller`
- `Assets/Sprites/Rooms/`: `room_day` (used) and `room_night`
- `Assets/Sprites/UI/`: buttons, icons and the happy, love, food and water bars

## Use it in your own code

The Animator has one number, `Mood`. Set it to switch animation:

```csharp
GetComponent<Animator>().SetInteger("Mood", 4);   // 4 = eating
```

0 idle, 1 happy, 2 sad, 3 crying, 4 eating, 5 playing, 6 studying, 7 sleeping.

To rebuild the clips and scene after changing frames: menu **PocketPet > Build Hamster**.
