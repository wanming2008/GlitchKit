# GlitchKit - Glitch on image in Objective-C

![before glitch](https://dl.dropboxusercontent.com/u/980764/images/glitch1.png)

```objc
#import "GlitchKit.h"

// glitch!
[uiImageView glitch];
```

![after glitch](https://dl.dropboxusercontent.com/u/980764/images/glitch2.png)

```objc
// apply custom glitch
[uiImageView glitchWithBlock:^int(int byte, int index, uint length, Byte *bytes) {
  return (byte == 42 && arc4random() % 3 == 1) ? 0 : byte;
}];
```

![after glitch3](https://dl.dropboxusercontent.com/u/980764/images/glitchr3.png)


## GettingStarted

### Installation


```
# in your Podfile
pod 'GlitchKit', git: 'https://github.com/hotchpotch/GlitchKit'
```

