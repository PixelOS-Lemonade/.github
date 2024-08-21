## Pixel OS for OnePlus 9 (lemonade)
Yet another (unofficial) Pixel OS port for OnePlus 9.

### Download
We host releases on OneDrive. Grab them [here](https://github.com/PixelOS-Lemonade/release/releases).

### Goal
- Focus on stability. Introduce only minimized out-of-tree tweaks:
    - We revert libart strip commit [here](https://github.com/PixelOS-Lemonade/art/commit/e17c78dd37ed2464a3178af21d71d99268a2ba1c) to provide backward compability for some apps. This should not break existing apps.
    - `PropImitationHooks` is removed as it will prevents you from passing `Strong Integrity` and breaks `Device Integrity` if builtin fingerprint is banned by Google. You should use [Play Integrity Fix](https://github.com/chiteroman/PlayIntegrityFix/) or [Tricky Store](https://github.com/5ec1cff/TrickyStore) instead!
    - `Stack protector` related kernel configs are enabled [here](https://github.com/PixelOS-Lemonade/kernel_oneplus_sm8350/commit/91802ddaa8931b7d0c1cb40048ab57a9f226f3bb) as `matrix level 5` requires.
    - Need [KernelSU](https://github.com/tiann/KernelSU)? Download prebuilt kernel from [here](https://github.com/PixelOS-Lemonade/kernel_oneplus_sm8350_kernelsu/actions)!
- No insane patches or weird tweaks that actually introduce unwanted behaviours.
    - Expect stock behaviour of LineageOS
    - Firmware is included in the ROMs.

### Why for reinventing wheels
- Existing ROMs (for lemonade) either:
    - Introduce load of features / tweaks in the cost of random reboot / native crash / system freeze / different behaviour other than AOSP. 
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
