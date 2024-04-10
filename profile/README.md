## [Archived] Pixel Experience for OnePlus 9 (lemonade)
Yet another (unofficial) Pixel Experience port for OnePlus 9.

### We are archived
Sadly, Pixel Experience [end up its development in April 10th, 2024](https://blog.pixelexperience.org/2024/04/everything-has-to-come-to-an-end-sometime/), so we decide to archive this repo and no longer provide updates. It had been a good ride.

### Download
We host releases on GitHub. Grab them [here](https://github.com/PixelExperience-Lemonade/release/releases).

> [!NOTE]  
> We only build PE Plus Edition (if appliable) as my build machine took at least ~20mins to build one release. Feel free to build for yourself if you do not prefer.

### Goal
- Focus on stability. No out-of-tree tweaks by default:
    - Need [KernelSU](https://github.com/tiann/KernelSU)? Download prebuilt kernel from [here](https://github.com/PixelExperience-Lemonade/kernel_oneplus_sm8350_kernelsu/actions)!
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
