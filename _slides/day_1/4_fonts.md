# Fonts

---
### Import the font files
To work with a font, import the font files into the project. It’s common practice to put font files in a fonts or assets folder at the root of a Flutter project.

For example, to import the Raleway and Roboto Mono font files into a project, the folder structure might look like this:

```sh
awesome_app/
  fonts/
    Raleway-Regular.ttf
    Raleway-Italic.ttf
    RobotoMono-Regular.ttf
    RobotoMono-Bold.ttf
```

---
### Supported font formats
Flutter supports the following font formats:

- .ttc
- .ttf
- .otf

Flutter does not support .woff and .woff2 fonts for all platforms.

---
### Declare the font in the pubspec
Once you’ve identified a font, tell Flutter where to find it. You can do this by including a font definition in the pubspec.yaml file.

```yaml
flutter:
  fonts:
    - family: Raleway
      fonts:
        - asset: fonts/Raleway-Regular.ttf
        - asset: fonts/Raleway-Italic.ttf
          style: italic
    - family: RobotoMono
      fonts:
        - asset: fonts/RobotoMono-Regular.ttf
        - asset: fonts/RobotoMono-Bold.ttf
          weight: 700
```

---
### Font Options: Weight
The weight property specifies the weight of the outlines in the file as an integer multiple of 100, between 100 and 900. These values correspond to the FontWeight and can be used in the fontWeight property of a TextStyle object. For example, if you want to use the RobotoMono-Bold font defined above, you would set fontWeight to FontWeight.w700 in your TextStyle.

Note that defining the weight property does not override the actual weight of the font. You would not be able to access RobotoMono-Bold with FontWeight.w100, even if its weight was set to 100.

---
### Font Options: Style
The style property specifies whether the outlines in the file are italic or normal. These values correspond to the FontStyle and can be used in the fontStyle property of a TextStyle object. For example, if you want to use the Raleway-Italic font defined above, you would set fontStyle to FontStyle.italic in your TextStyle.

Note that defining the style property does not override the actual style of the font; You would not be able to access Raleway-Italic with FontStyle.normal, even if its style was set to normal.

---
### Setting a default Font

```dart
ThemeData(fontFamily: 'Raleway'),
```

---
### Setting A font per Widget

```dart
Text(
  'Roboto Mono sample',
  style: TextStyle(fontFamily: 'RobotoMono'),
)
```
---
### TextTheme in Flutter

<img src="/images/fonts.png">

---
### TextTheme in Flutter

#### Display
Large:      H1
Medium:     H2
Small:      H3
#### Headline
Large:      No Equivelant (H3.5)
Medium:     H4
Small:      H5
#### Title
Large:      H6
Medium:     Subtitle
Small:      Small Subtitle
#### Label
Large:      Button Text
Medium:     No Equivelant
Small:      Overline
#### Body
Large:      Body1
Medium:     Body2 (Default for flutter Text)
Small:      Caption

---
### Creating a TextTheme

```dart
TextTheme createTextTheme() {
    return TextTheme(
        bodyLarge: TextStyle(
            fontSize: 16,
            // for most widgets, color is automatically implied from theme. 
            // Providing it here will override that.
            color: Colors.green,
        ),
    );
}
```