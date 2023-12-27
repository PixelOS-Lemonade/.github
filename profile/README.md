## Pixel Experience for OnePlus 9 (lemonade)
Yet another (unofficial) Pixel Experience port for OnePlus 9.

### Goal
- Focus on stability. Introduce *minimized* out-of-tree tweaks:
    - Add [KernelSU](https://github.com/tiann/KernelSU) for out-of-box root experience.
    - Add IFAA components for supporting biometic payment of Alipay.
    - Cherry-pick [this](https://github.com/LineageOS/android_hardware_interfaces/commit/d45590152e95fe42bd3444e108fd8cd46ce2eae7) commit to support LDAC adaptive streaming.
- No insane patches or weird tweaks that actually introduce unwanted behaviours.
    - Expect stock behaviour of LineageOS

### Why for reinventing wheels
- Existing ROMs (for lemonade) either:
    - Introduce load of features / tweaks in the cost of random reboot / native crash / different behaviour other than AOSP. 
    - Stable, but lack of useful features (KSU, IFAA, etc.).

I would like to strike the balance between the *TRUE* stability and minimal features that helps get most out of the day. That is why I created this organization and build Pixel Experience for lemonade.

### Q&A
#### Only devices repo? What's the rest?
In either LineageOS or PixelExperience GitHub repo. I only modify minimum repos that are required for building PE. The rest of parts are reused from existing base.

#### Will you also build lemonadep (OnePlus 9 Pro) in the future?
No. Unless someone is owning the device and willing to test.