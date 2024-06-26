## Pixel OS for OnePlus 9 (lemonade)
Yet another (unofficial) Pixel OS port for OnePlus 9.

### Download
We host releases on GitHub. Grab them [here](https://github.com/PixelOS-Lemonade/release/releases).

### Goal
- Focus on stability. Minimized out-of-tree tweaks by default:
    - We revert libart strip commit [here](https://github.com/PixelOS-Lemonade/platform_art/commit/858b1d6baf74a0eb5a2de36ce6b0a7ddba62ea8e) to provide backward compability for some apps. This should not break existing apps.
    - Need [KernelSU](https://github.com/tiann/KernelSU)? Download prebuilt kernel from [here](https://github.com/PixelOS-Lemonade/kernel_oneplus_sm8350_kernelsu/actions)!
- No insane patches or weird tweaks that actually introduce unwanted behaviours.
    - Expect stock behaviour of LineageOS

### Why for reinventing wheels
- Existing ROMs (for lemonade) either:
    - Introduce load of features / tweaks in the cost of random reboot / native crash / different behaviour other than AOSP. 
    - Stable, but lack of useful features (KSU, etc.).

I would like to strike the balance between the *TRUE* stability and minimal features that helps get most out of the day. That is why I created this organization and build Pixel OS for lemonade.

### Q&A
#### Only devices repo? What's the rest?
In either LineageOS or Pixel OS GitHub repo. I only modify minimum repos that are required for building Pixel OS. The rest of parts are reused from existing base.

#### Will you also build lemonadep (OnePlus 9 Pro) in the future?
No. Unless someone is owning the device and willing to test.

#### System crashed! E Zygote : java.lang.IllegalArgumentException: Unexpected cancel with surface 12
Do not use [Nevoluton with DEBUG enabled](https://nevo.app/setup). Please use the following command to reset config:
```
setprop persist.log.tag.NotificationService ""
```
Then reboot your phone.
