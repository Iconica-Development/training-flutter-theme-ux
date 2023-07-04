# What can you do?

What can you do as a UX'er

---
### Delivering Assets

Make sure assets are in a logical structure:

```
assets/
    images/
        background.png
        2.0x/
            background.png
        3.0x/
            background.png
    icons/
        icon.png
        2.0x/
            icon.png
    fonts/
        font.ttf
    animations/
        some-animation.riv
```

---
### Delivering Assets

And are defined in the pubspec.yaml

```yaml
flutter:
  assets:
   - assets/images
   - assets/icons
   - assets/fonts
   - assets/animations
  fonts:
    - family: SomeFont
      fonts:
        - asset: assets/fonts/font.ttf
        - asset: assets/fonts/font.ttf
          style: italic

```

---
### Pre-defining theme

Define a dark theme and a light Theme:

```dart
ThemeData getDarkTheme() {
    // ..
}

ThemeData getLightTheme() {
    // ...
}
```

---
### Pre-defining theme

If the app changes theme based on a setting or color:

```dart
ThemeData getDarkTheme({
    required Color primary,
}) {
   // ...
}
```

---
### Repeating colours

If you want to re-use colors for multiple positions in the theme, give them a semantic name.

Also place any colors or values that do not fit in the flutter theme here.

```dart

class MyAppTheme {

    const static Color primaryDarkColor = Colors.red.shade700;
    const static Color errorSevereColor = Color(0xFFFF0000);
    
}

ThemeData getDarkTheme() {
    return ThemeData(
        colorScheme: ColorScheme.fromSeed(MyAppTheme.primaryDarkColor).copyWith(
            errorColor: MyAppTheme.errorSevereColor;
        );
    );
}

```

