# Material Design

---
### Material Design Concepts

Material Widgets being delivered standard by Flutter.

There are 6 categories:
- Actions
- Communication
- Containment
- Navigation
- Selection
- Text Inputs

<a href="https://docs.flutter.dev/ui/widgets/material">Material Widgets Library</a>

---
### Actions


- common buttons
  - Elevated
  - Filled
  - FilledTonal
  - Outlined
  - Text

> Buttons can take a shape.

- Floating Action Button
  - Can be extended or not
- Segmented Button
- Iconbutton 


---
### Communication

- Badge
  - With Label
  - With Count
  - Just a dot
- Progress Indicators
  - CircularProgressindicator
  - LinearProgressIndicator
Progress indicators can load indefinitely, can load until a certain point or can even change color based on the current value of the loading indicator.

- Snackbar

Snackbars can take in various shapes and can contain actions

---
### Snackbar

```dart
SnackBar(
    action: SnackBarAction(
        label: 'Action',
        onPressed: () {
        // Code to execute.
        },
    ),
    content: const Text('Awesome SnackBar!'),
    duration: const Duration(milliseconds: 1500),
    width: 280.0, // Width of the SnackBar.
    padding: const EdgeInsets.symmetric(
        horizontal: 8.0, // Inner padding for SnackBar content.
    ),
    behavior: SnackBarBehavior.floating,
    shape: RoundedRectangleBorder(
        borderRadius: BorderRadius.circular(10.0),
    ),
),
```

---
### Containment

- Bottomsheet
  - Modal
  - Persistent
- Card
- Dialog
- Divider
- List
  - ListTiles

---
### Navigation
- AppBar
- BottomAppBar
- NavigationBar
- Navigation Drawer
- Navigation rail
- TabBar
  

---
### Selection

- Checkbox
- Chip
- Datepicker
- Menu
- RadioButton
- Slider
- Switch
- Timepicker

---
### Text Inputs

- TextField

Editable through the InputDecoration

Has lots of other configurations:
- Type of keyboard
- ObscureText
- Max length
- max/min lines
- Hints
- Autocorrect
- CursorAnimation 


---
### In practice
<iframe src="https://flutter.github.io/samples/web/material_3_demo/#/" width="50%" height="600px" title="Material 3 Demo App"></iframe>