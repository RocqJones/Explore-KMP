# Explore-KMP
Kotlin Multiplatform(KMP) Masterclass - KMM

## Delve into:
- Master iOS &amp; Android app development with KMP
- Jetpack Compose &amp; SwiftUI
- Ktor
- SQLDelight
- Clean Architecture
- MVI

## What is KMP?
Kotlin Multiplatform is a Kotlin-based framework that allows code sharing and frameworks between different platforms.
- JetBrains developed Kotlin Multiplatform, and using it to target mobile platforms is stable and production-ready

![image](https://github.com/RocqJones/Explore-KMP/assets/32324500/6bd11c1b-9916-4f0c-b24c-42201602fdac)

## Supported Platforms.
- Android
- iOs
- Web
- Desktop

## Environment setup.
- [Please follow this link to complete this step.](https://www.jetbrains.com/help/kotlin-multiplatform-dev/multiplatform-setup.html)
-  If you are running on Mac you can verify your environment requirements are successfully set by running
```shell
$ kdoctor
```
- Your response should be as follows. In case you run into an issue with `Cocoapods` for the Apple Silicon Chip [please check this resource and follow the steps](https://stackoverflow.com/questions/64901180/how-to-run-cocoapods-on-apple-silicon-m1/66556339#66556339).
![image](https://github.com/RocqJones/Explore-KMP/assets/32324500/70c224c6-5636-4c8f-86cd-228171adacb6)

## project structure
Each Kotlin Multiplatform project includes three modules:
- **shared** is a Kotlin module that contains the logic common for both Android and iOS applications – the code you share between platforms. It uses Gradle as the build system to help automate your build process.
- **androidApp** is a Kotlin module that builds into an Android application. It uses Gradle as the build system. The `androidApp` module depends on and uses the shared module as a regular Android library.
- **iosApp** is an Xcode project that builds into an iOS application. It depends on and uses the shared module as an iOS framework. The shared module can be used as a regular framework or as a CocoaPods dependency, based on what you've chosen for iOS framework distribution. For now, we focus on regular framework dependency.

- The shared module consists of three source sets: `androidMain`, `commonMain`, and `iosMain`. Source set is a Gradle concept for a number of files logically grouped together where each group has its own dependencies. In Kotlin Multiplatform, different source sets in a shared module can target different platforms
- The common source set uses common Kotlin code, and platform source sets use Kotlin code specific to each target. Kotlin/JVM is used for `androidMain` and Kotlin/Native for `iosMain`:
![image](https://github.com/RocqJones/Explore-KMP/assets/32324500/b51713c6-9174-4ac2-8e73-59509d59fc5a)

- When the shared module is built into an Android library, common Kotlin code is treated as Kotlin/JVM. When it is built into an iOS framework, common Kotlin is treated as Kotlin/Native


## Resources.
1. [Official KMM overview.](https://kotlinlang.org/docs/multiplatform.html)
2. [How to run CocoaPods on Apple Silicon (M1/M2)](https://stackoverflow.com/questions/64901180/how-to-run-cocoapods-on-apple-silicon-m1/66556339#66556339)
