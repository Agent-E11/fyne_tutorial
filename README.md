## Issues

### No NDK

When running

```
fyne package -os android -appID com.example.myapp -icon app-icon.png
```

I get the error

```
no Android NDK found in $ANDROID_HOME/ndk-bundle nor in $ANDROID_NDK_HOME
```

Solved by:
1. downloading an NDK from [developer.android.com](https://developer.android.com/ndk/downloads)
2. Extracting it to `/home/agent-e11/ndk-bundle/`
3. running `export ANDROID_NDK_HOME=/home/agent-e11/ndk-bundle`

### No arm compiler

When running 

```
fyne package -os android -appID com.example.myapp -icon app-icon.png
```

I get the error

```
no compiler for arm was found in the NDK (tried ). Make sure your NDK version is >= r19c. Use `sdkmanager --update` to update it
```

Unsolved (The ndk version is r26c. sdkmanager is not installed (?))
