## Pixel Experience for OnePlus 9 (lemonade)
Yet another (unofficial) Pixel Experience port for OnePlus 9.

### Download
We host releases on GitHub. Grab them [here](https://github.com/PixelExperience-Lemonade/release/releases).

> [!NOTE]  
> We only build PE Plus Edition (if appliable) as my build machine took at least ~20mins to build one release. Feel free to build for yourself if you do not prefer.

### Goal
- Focus on stability. Introduce *minimized* out-of-tree tweaks:
    - Add [KernelSU](https://github.com/tiann/KernelSU) for out-of-box root experience (Kernel only. You still need to manually install manager).
- No insane patches or weird tweaks that actually introduce unwanted behaviours.
    - Expect stock behaviour of LineageOS

### Why for reinventing wheels
- Existing ROMs (for lemonade) either:
    - Introduce load of features / tweaks in the cost of random reboot / native crash / different behaviour other than AOSP. 
    - Stable, but lack of useful features (KSU, etc.).

I would like to strike the balance between the *TRUE* stability and minimal features that helps get most out of the day. That is why I created this organization and build Pixel Experience for lemonade.

### Q&A
#### Only devices repo? What's the rest?
In either LineageOS or PixelExperience GitHub repo. I only modify minimum repos that are required for building PE. The rest of parts are reused from existing base.

#### Will you also build lemonadep (OnePlus 9 Pro) in the future?
No. Unless someone is owning the device and willing to test.

#### System crashed! E Zygote : java.lang.IllegalArgumentException: Unexpected cancel with surface 12
Do not use [Nevoluton with DEBUG enabled](https://nevo.app/setup). Please use the following command to reset config:
```
setprop persist.log.tag.NotificationService ""
```
Then reboot your phone.
