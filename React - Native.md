# Git
```sh
git config credential.helper store
```

# Custom View

https://github.com/react-native-community/react-native-svg

# React Native Maps

`animateToRegion`

# Offset for RefreshControl
# Android
`progressViewOffset={HEADER_MAX_HEIGHT}`
# iOs
```
  contentInset={{
    top: HEADER_MAX_HEIGHT,
  }}
  contentOffset={{
    y: -HEADER_MAX_HEIGHT,
  }}
```
# Dynamically changing number of columns in React Native Flat List
```
key={(this.state.horizontal ? 'h' : 'v')}
```
# Snap Slider

```
https://www.npmjs.com/package/react-native-snap-slider
```

# com.github.facebook.watchman.plist for write: Permission denied
```
sudo chown -R $(username):staff ~/Library/LaunchAgents
```


# Compile-time Error: control may reach end of non-void function with Xcode 10.2
```
1. Open the source file at ${RN_PROJ}/node_modules/realm/src/jsc/jsc_value.hpp.
2. Find the switch-case segment at THERE.
3. Replace the whole switch-case segment with the following code.
    switch (JSValueGetType(ctx, value)) {
        case kJSTypeNull: return "null";
        case kJSTypeNumber: return "number";
        case kJSTypeObject: return "object";
        case kJSTypeString: return "string";
        case kJSTypeBoolean: return "boolean";
        case kJSTypeUndefined: return "undefined";
        case kJSTypeSymbol: return "symbol";
    }
```

# Could not find iPhone 6 simulator
```
version.startsWith('com.apple.CoreSimulator.SimRuntime.iOS') && !version.startsWith('com.apple.CoreSimulator.SimRuntime.tvOS')
```
or
```
if (!version.includes('iOS') && !version.includes('tvOS'))
```
# "config.h" not found
```
1. Close Xcode.
2. Open Terminal, go to your project's root folder and run: cd node_modules/react-native/third-party/glog-0.3.4/
3. Run the configure script: ./configure
4. Open Xcode and try to run your app.
```

# "Build archive error vs Xcode10"
```
Multiple commands produce '/Users/tu/Library/Developer/Xcode/DerivedData/Tituk-fndmfujccqhdareyswrxhslqzyvn/Build/Intermediates.noindex/ArchiveIntermediates/Tituk/IntermediateBuildFilesPath/UninstalledProducts/iphoneos/libyoga.a':

Target 'yoga' has a command with output '/Users/tu/Library/Developer/Xcode/DerivedData/Tituk-fndmfujccqhdareyswrxhslqzyvn/Build/Intermediates.noindex/ArchiveIntermediates/Tituk/IntermediateBuildFilesPath/UninstalledProducts/iphoneos/libyoga.a'
Target 'yoga' has a command with output '/Users/tu/Library/Developer/Xcode/DerivedData/Tituk-fndmfujccqhdareyswrxhslqzyvn/Build/Intermediates.noindex/ArchiveIntermediates/Tituk/IntermediateBuildFilesPath/UninstalledProducts/iphoneos/libyoga.a'
```
```
fix
installer.pods_project.targets.each do |target|
    if target.name == "React"
      target.remove_from_project
    end

    if target.name == "yoga"
      target.remove_from_project
    end
  end
```
