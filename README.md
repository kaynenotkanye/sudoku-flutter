# Sudoku  [![License](https://img.shields.io/badge/License-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## about

A open source Sudoku game application powered by Flutter .

you can build the Sudoku Game just  for you own.

[Download](https://github-production-release-asset-2e65be.s3.amazonaws.com/291502708/946fed00-eb22-11ea-9f3b-e65b96746ed7?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20200830%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20200830T164712Z&X-Amz-Expires=300&X-Amz-Signature=8e3ec35a5237694414a4de94836a2480a439fe2249b8c895447e4e9e7a188a42&X-Amz-SignedHeaders=host&actor_id=1745525&key_id=0&repo_id=291502708&response-content-disposition=attachment%3B%20filename%3Dapp-release.apk&response-content-type=application%2Fvnd.android.package-archive) latest build apk(beta)

## snapshot

![Bootstrap](./document/img/Jietu20200830-234059_jpg.jpg)![Game](./document/img/Jietu20200830-234139_jpg.jpg)

## todo list
- [:white_check_mark:]  full experience of sudoku
- make some funny eggs
- [:bangbang:] Sudoku puzzle Scaner


## environment
- flutter sdk : `>=2.7.0 <3.0.0`

## dependency
- [sudoku_dart](https://github.com/forfuns/sudoku-dart) (sudoku core opensource  lib  )
- [Hive](https://github.com/hivedb/hive)
- [scoped_model](https://github.com/brianegan/scoped_model)
- logger 
- sprintf

## platform support
- android
- iOS
- ~~WEB (no plan support yet)~~

## install
```shell
$> flutter pub get
# options,when you change the lib/state/sudoku_state.dart file,make sure build hive adapter for the project
$> flutter packages pub run build_runner build
```

## run
```shell
$> flutter devices
1 connected device:

iPhone SE (2nd generation) (mobile) • 09684738-362A-468F-80F2-1824A785D324 • ios • com.apple.CoreSimulator.SimRuntime.iOS-13-6 (simulator)

$> flutter run -d 09684738-362A-468F-80F2-1824A785D324
```

## pre-for-build
### android
create a keystore for apk signature

> On Windows
>
> ```shell
> keytool -genkey -v -keystore c:\Users\USER_NAME\key.jks -storetype JKS -keyalg RSA -keysize 2048 -validity 10000 -alias key
> ```
> 

> On Mac/Linux
> ```shell
> keytool -genkey -v -keystore ~/key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias key
> ```

copy `./android/key.properties.example` and rename to `./android/key.properties` that contains a reference to your keystore

more information pls reference official website : https://flutter.dev/docs/deployment/android

### iOS

sign up apple developer

in Xcode,open `./ios/Runner.xcworkspace` to view your app's settings

select the `Runner` project in the Xcode project navigator. then in the main view sidebar,select the `Runner` target and select the `Identity` tab,in the `Signing` section change `Team` and `Bundle Identifier`

more information pls reference official website : https://flutter.dev/docs/deployment/ios

## build
```shell
# iOS
$> flutter build iOS
# android
$> flutter build apk
```

## more flutter features
see official [Flutter](https://flutter.dev/) website

## the end

thanks for visit this repository , wish you can like it and star it :kissing_heart:

