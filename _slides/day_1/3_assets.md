# Assets

---
### Providing Assets

Flutter uses the pubspec.yaml file, located at the root of your project, to identify assets required by an app.

Here is an example:

```yaml
flutter:
  assets:
    - assets/my_icon.png
    - assets/background.png
```

---
### Asset Resolutions

When flutter loads assets, it will look for other assets of different resolutions of the same name in resolution folders:

```
  .../image.png
  .../Mx/image.png
  .../Nx/image.png
  ...etc.
```

In this example, image.png is considered the main asset, while Mx/image.png and Nx/image.png are considered to be variants.

---
### Asset Resolutions

The main asset is assumed to correspond to a resolution of 1.0. For example, consider the following asset layout for an image named my_icon.png:

```
  .../my_icon.png       (mdpi baseline)
  .../1.5x/my_icon.png  (hdpi)
  .../2.0x/my_icon.png  (xhdpi)
  .../3.0x/my_icon.png  (xxhdpi)
  .../4.0x/my_icon.png  (xxxhdpi)
```
On devices with a device pixel ratio of 1.8, the asset .../2.0x/my_icon.png is chosen. 

For a device pixel ratio of 2.7, the asset .../3.0x/my_icon.png is chosen.

---
### App icons

Apple cannot deal with app icons that contain transparancy

There is a package that can automatically create app icons for all platforms:

> https://pub.dev/packages/flutter_launcher_icons
