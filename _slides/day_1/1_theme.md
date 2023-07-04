# Theme

---
### Theme Widget

Allows to refresh Theme

Theme is defined through MaterialApp.

Contains ThemeData

---
### Theme Widget

Can be used to refresh the theme further down the app

```dart
Theme(
  // Find and extend the parent theme using `copyWith`. See the next
  // section for more info on `Theme.of`.
  data: Theme.of(context).copyWith(splashColor: Colors.yellow),
  child: const FloatingActionButton(
    onPressed: null,
    child: Icon(Icons.add),
  ),
);
```

---
### Using the theme

```dart
ColoredBox(
  color: Theme.of(context).colorScheme.secondary,
  child: Text(
    'Text with a background color',
    style: Theme.of(context).textTheme.titleLarge,
  ),
),
```

---
### ThemeData

Going through every option in ThemeData and see what impact and semantic meaning it has

---
### ThemeData: colorScheme

A set of 30 colors based on the Material spec that can be used to configure the color properties of most components.


- Primary colors are used for key components across the UI, such as the FAB, prominent buttons, and active states.
- Secondary colors are used for less prominent components in the UI, such as filter chips, while expanding the opportunity for color expression.
- Tertiary colors are used for contrasting accents that can be used to balance primary and secondary colors or bring heightened attention to an element, such as an input field. The tertiary colors are left for makers to use at their discretion and are intended to support broader color expression in products.

---
### ThemeData: ColorScheme

Many of the colors have matching 'on' colors

The remaining colors of the scheme are comprised of neutral colors used for backgrounds and surfaces, as well as specific colors for errors, dividers and shadows.

---
### ThemeData: ColorScheme Factory Constructors

- fromSeed: Generate a ColorScheme derived from the given seedColor.
- fromSwatch: Create a color scheme from a MaterialColor swatch.
- light: Create a ColorScheme based on a purple primary color that matches the baseline Material color scheme.
- dark: Create the recommended dark color scheme that matches the baseline Material color scheme.
- highContrastDark, highContrastLight: high contrast version of the light/dark colorschemes.

> you can override the colorscheme using the copyWith() method

---
### ThemeData: TextTheme

The textTheme contains all typograhic theme customization according to the material Design spec.

> More on that in the fonts chapter

---
### ThemeData: InputDecoration

> A tour of the docs

---
### ThemeData: MaterialState

Material state properties represent values that depend on a widget's material "state". The state is encoded as a set of MaterialState values, like MaterialState.focused, MaterialState.hovered, MaterialState.pressed. 

---
### ThemeData: nested themes

__actionIconTheme__
This is a custom theme that you can use to override specific Icons with other widgets through builders

```dart
actionIconTheme: ActionIconThemeData(
  backButtonIconBuilder: (BuildContext context) => Icon(Icons.chevron_left),
),
```

__appBarTheme__
A theme for customizing the color, elevation, brightness, iconTheme and textTheme of AppBars.

__badgeTheme__
A theme for customizing the colors and placement of badges


---
### ThemeData: nested themes

__bannerTheme__
A theme that allows you to edit the style of a MaterialBanner

__bottomAppBarTheme__
A theme for customizing the shape, elevation, and color of a BottomAppBar.
final

__bottomNavigationBarTheme__
A theme for customizing the appearance and layout of BottomNavigationBar widgets.
final

__bottomSheetTheme__
A theme for customizing the color, elevation, and shape of a bottom sheet.

---
### ThemeData: nested themes

__buttonBarTheme__
A theme for customizing the appearance and layout of ButtonBar widgets.

__buttonTheme__
Defines the default configuration of button widgets, like DropdownButton and ButtonBar.

__cardTheme__
The colors and styles used to render Card.

__chipTheme__
The colors and styles used to render Chips.

__checkBoxTheme__
A theme for customizing the appearance and layout of Checkbox widgets.

---
### ThemeData nested themes

__dataTableTheme__
A theme for customizing the appearance and layout of DataTable widgets.

__datePickerTheme__
A theme for customizing the appearance and layout of DatePickerDialog widgets.

__dialogTheme__
A theme for customizing the shape of a dialog.

__dividerTheme__
A theme for customizing the color, thickness, and indents of Dividers, VerticalDividers, etc.

---
### ThemeData nested themes

__drawerTheme__
A theme for customizing the appearance and layout of Drawer widgets.

__dropDownMenuTheme__
A theme for customizing the appearance and layout of DropdownMenu widgets.

__elevatedButtonTheme__
A theme for customizing the appearance and internal layout of ElevatedButtons.

__expansionTileTheme__
A theme for customizing the visual properties of ExpansionTiles.

---
### ThemeData nested themes

__filledButtonTheme__
A theme for customizing the appearance and internal layout of FilledButtons.

__floatingActionButtonTheme__
A theme for customizing the shape, elevation, and color of a FloatingActionButton.

__iconButtonTheme__
A theme for customizing the appearance and internal layout of IconButtons.

__listTileTheme__
A theme for customizing the appearance of ListTile widgets.

---
### ThemeData: nested themes

__menuBarTheme__
A theme for customizing the color, shape, elevation, and other MenuStyle aspects of the menu bar created by the MenuBar widget.

__menuButtonTheme__
A theme for customizing the color, shape, elevation, and text style of cascading menu buttons created by SubmenuButton or MenuItemButton.

__menuTheme__
A theme for customizing the color, shape, elevation, and other MenuStyle attributes of menus created by the SubmenuButton widget.

__navigationBarTheme__
A theme for customizing the background color, text style, and icon themes of a NavigationBar.

---
### ThemeData: nested themes

__navigationDrawerTheme__
A theme for customizing the background color, text style, and icon themes of a NavigationDrawer.

__navigationRailTheme__
A theme for customizing the background color, elevation, text style, and icon themes of a NavigationRail.

__outlinedButtonTheme__
A theme for customizing the appearance and internal layout of OutlinedButtons.

__pageTransitionsTheme__
Default MaterialPageRoute transitions per TargetPlatform.

---
### ThemeData: nested themes

__popupMenuTheme__
A theme for customizing the color, shape, elevation, and text style of popup menus.

__progressIndicatorTheme__
A theme for customizing the appearance and layout of ProgressIndicator widgets.

__radioTheme__
A theme for customizing the appearance and layout of Radio widgets.

__scrollbarTheme__
A theme for customizing the colors, thickness, and shape of Scrollbars.

---
### ThemeData: nested themes

__searchBarTheme__
A theme for customizing the appearance and layout of SearchBar widgets.

__searchViewTheme__
A theme for customizing the appearance and layout of search views created by SearchAnchor widgets.

__segmentedButtonTheme__
A theme for customizing the appearance and layout of SegmentedButton widgets.

__sliderTheme__
The colors and shapes used to render Slider.

---
### ThemeData: nested themes

__snackbarTheme__
A theme for customizing colors, shape, elevation, and behavior of a SnackBar.

__switchTheme__
A theme for customizing the appearance and layout of Switch widgets.

__tabBarTheme__
A theme for customizing the size, shape, and color of the tab bar indicator.

__textButtonTheme__
A theme for customizing the appearance and internal layout of TextButtons.

__textSelectionTheme__
A theme for customizing the appearance and layout of widgets with Selectable Text.

---
### ThemeData: nested themes

__timePickerTheme__
A theme for customizing the appearance and layout of time picker widgets.

__toggleButtonsTheme__
Defines the default configuration of ToggleButtons widgets.

__tooltipTheme__
A theme for customizing the visual properties of Tooltips.


